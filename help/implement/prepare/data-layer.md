---
title: 데이터 계층 만들기
description: Analytics 구현에서 데이터 계층이 무엇이고 Adobe Analytics에서 이 데이터 계층을 사용하여 변수를 매핑하는 방법을 알아봅니다.
translation-type: ht
source-git-commit: 283fcd5832abe4c09caa332c2ebc3a22029e6707

---


# 데이터 계층 만들기

데이터 계층은 구현에 사용된 모든 변수 값을 포함하는 사이트의 JavaScript 개체의 프레임워크로서, 구현을 보다 세밀하게 제어하고 쉽게 유지 관리할 수 있습니다.

## 전제 조건

[솔루션 디자인 문서 만들기](solution-design.md) - 조직이 추적 요구 사항을 충족시키는 것이 중요합니다. 조직의 개발 팀에 도달하기 전에 솔루션 디자인 문서를 준비하십시오.

## 워크플로우

데이터 계층을 사용하여 Adobe Analytics를 구현하는 절차는 일반적으로 다음과 같습니다.

1. **사이트 개발 팀과 협력하여 데이터 계층 구현**: 사이트 개발 팀은 데이터 계층 개체가 올바른 값으로 채워지는지 확인하는 작업을 주로 수행합니다. 사이트 개발 팀과 함께 이 페이지를 검토하여 팀 간의 기대 내용이 일치하는지 확인합니다.
   > [!NOTE] 다음의 Adobe 권장 데이터 계층 사양은 선택 사항입니다. 이미 데이터 계층이 있거나 Adobe의 사양을 따르지 않기로 선택하는 경우, 따로 따라야 할 사양을 조직이 충족하도록 해야 합니다.
2. **브라우저 콘솔을 사용하여 데이터 계층의 유효성 검사**: 데이터 계층이 만들어지면 브라우저의 개발자 콘솔을 사용하여 데이터 계층이 작동하는지 확인할 수 있습니다. `F12` 키를 사용하면 대부분의 브라우저에서 개발자 콘솔을 열 수 있습니다. 변수 값의 예는 `digitalData.page.pageInfo.pageID`입니다.
3. **Adobe Experience Platform Launch를 사용하여 데이터 계층 개체를 Launch 데이터 요소에 매핑**: Launch에서 데이터 요소를 만들고 데이터 계층에 요약된 JavaScript 속성에 매핑합니다.
4. **Launch에서 Adobe Analytics 확장을 사용하여 데이터 요소를 Analytics 변수에 매핑**: 솔루션 디자인 문서에 따라 각 데이터 요소를 적절한 Analytics 변수에 지정합니다.

## 사양

[고객 경험 디지털 데이터 커뮤니티 그룹](https://www.w3.org/community/custexpdata/)에 의해 요약된 [고객 경험 디지털 데이터 계층](https://www.w3.org/2013/12/ceddl-201312.pdf)을 따르는 것이 좋습니다. 데이터 계층 요소가 Adobe Analytics와 상호 작용하는 방법을 이해하려면 다음 섹션을 사용하십시오.

사용할 권장 데이터 계층 개체는 `digitalData`입니다. 다음 예에서는 값 예와 함께 다소 포괄적인 데이터 계층 JSON 개체를 나열합니다.

```js
digitalData = {
    pageInstanceID: "Example page - production",
    page: {
        pageInfo: {
            pageID: "5093",
            pageName: "Example page",
            destinationURL: "https://example.com/index.html",
            referringURL: "https://example.com/referrer.html",
            sysEnv: "desktop",
            variant: "2",
            version: "1.14",
            breadCrumbs: ["Home","Example group","Example page"],
            author: "J Smith",
            issueDate: "Example date",
            effectiveDate: "Example date",
            expiryData: "Example date",
            language: "en-US",
            geoRegion: "US",
            industryCodes: "Example industry codes",
            publisher: "Example publisher"
        },
        category: {
            primaryCategory: "Example page category",
            subCategory1: "Sub-category example"
        },
        attributes: {
            country: "US",
            language: "en-US"
        }
    },
    product1: {
        productInfo: {
            productID: "4859",
            productName: "Example product",
            description: "Example description",
            productURL: "https://example.com/product.html",
            productImage: "https://example.com/product_image.png",
            productThumbnail: "https://example.com/product_thumbnail.png",
            manufacturer: "Example manufacturer",
            size: "Product size"
        },
        category: {
            primaryCategory: "Example product category",
            subCategory: "Example sub-category"
        }
    },
    cart: {
        cartID: "934856",
        price: {
            basePrice: 200.00,
            voucherCode: "EXAMPLEVOUCHER1",
            voucherDiscount: 0.50,
            currency: "USD",
            taxRate: 0.20,
            shipping: 5.00,
            shippingMethod: "UPS",
            priceWithTax: 120,
            cartTotal: 125
        }
    },
    transaction: {
        transactionID: "694025",
        profile: {
            profileInfo: {
                profileID: "exampleprofile",
                userName: "exampleusername",
                email: "user@example.com"
            },
            address: {
                line1: "123 Vague Street",
                line2: "Apt 1",
                city: "Austin",
                stateProvince: "TX",
                postalCode: "78610",
                country: "USA"
            },
            shippingAddress: {
                line1: "123 Vague Street",
                line2: "Apt 1",
                city: "Austin",
                stateProvince: "TX",
                postalCode: "78610",
                country: "USA"
            }
        }
    },
    event1: {
        category: {
            primaryCategory: "Example event category",
            subCategory: "Example sub-category"
        }
    },
    component1: {
        componentInfo: {
            componentID: "4921",
            componentName: "Example component"
        },
        category: {
            primaryCategory: "Example event category",
            subCategory: "Example sub-category"
        }
    },
    user1: {
        segment: "Premium membership",
        profile1: {
            profileInfo: {
                profileID: "exampleprofile",
                userName: "exampleusername",
                email: "user@example.com",
                language: "en-US",
                returningStatus: "New"
            },
            social: {
                facebook: "examplefacebookid",
                twitter: "exampletwitterhandle"
            }
        }
    },
    privacy: {
        accessCategories1: {
            categoryName: "Default",
            domains: "adobedtm.com"
        }
    },
    version: "1.0"
}
```

각 개체 및 하위 개체에 대해 자세히 알려면 [고객 경험 디지털 데이터 계층](https://www.w3.org/2013/12/ceddl-201312.pdf) 보고서를 사용하십시오. 일부 사이트에서는 모든 개체를 사용하지 않습니다. 예를 들어 뉴스 사이트를 호스팅하는 경우 `digitalData.product` 개체를 사용할 가능성이 없습니다.

데이터 계층은 확장 가능합니다. 조직만의 고유한 요구 사항이 있다면 해당 요구 사항에 맞게 데이터 계층에 개체를 포함할 수 있습니다.

## 데이터 계층 값 설정

데이터 계층은 일반적으로 서버측을 생성하며 사이트 컨텐츠를 작성하는 데 사용되는 것과 동일한 개체를 참조합니다. 조직의 [솔루션 디자인 문서](solution-design.md)에 설정된 추적 요구 사항을 기반으로 사이트의 데이터 계층을 설정하십시오.

## 다음 단계

[데이터 레이어 개체를 데이터 요소에 매핑](../launch/layer-to-elements.md): Adobe Experience Platform Launch에서 사이트의 데이터 레이어를 사용합니다.
