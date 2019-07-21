---
description: 다이내믹 태그 관리를 사용하여 사이트의 JavaScript 및 페이지 컨텐츠 로드를 결정하는 머리글 및 바닥글 코드를 추가합니다. 사용한 호스팅 옵션에 상관없이 사이트의 모든 페이지에 머리글 코드와 바닥글 코드를 모두 설치해야 합니다.
keywords: Analytics 구현; 구현 방법; 다이내믹 태그 관리; DTM; code; 페이지 코드; 머리글 코드; 바닥글 코드; 포함 코드; 포함 탭; 임베드
seo-description: 다이내믹 태그 관리를 사용하여 사이트의 JavaScript 및 페이지 컨텐츠 로드를 결정하는 머리글 및 바닥글 코드를 추가합니다. 사용한 호스팅 옵션에 상관없이 사이트의 모든 페이지에 머리글 코드와 바닥글 코드를 모두 설치해야 합니다.
seo-title: 머리글 및 바닥글 코드 추가
solution: Analytics
title: 머리글 및 바닥글 코드 추가
topic: 개발자 및 구현
uuid: 23 D 89 AE 0-340 A -4 B 12-91 D 1-953 B 4613 C 98 E
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 머리글 및 바닥글 코드 추가

다이내믹 태그 관리를 사용하여 사이트의 JavaScript 및 페이지 컨텐츠 로드를 결정하는 머리글 및 바닥글 코드를 추가합니다. 사용한 호스팅 옵션에 상관없이 사이트의 모든 페이지에 머리글 코드와 바닥글 코드를 모두 설치해야 합니다.

다이내믹 태그 관리에는 머리글과 바닥글 모두에 코드 조각이 포함되어 있으므로 페이지의 시작이나 끝에서 규칙을 실행할 수 있습니다. 이 기능을 사용하면 페이지 추적을 계속 제어하면서도 테스트 도구 및 기타 기술을 구현할 수 있습니다.

다이내믹 태그 관리는 스테이징 환경에서 변경 사항을 테스트한 후에 프로덕션 환경으로 변경 사항을 푸시하는 데 사용할 수 있는 스테이징 및 프로덕션 포함 코드를 작성합니다.

>[!IMPORTANT]
>
>성공적인 구현을 위해서는 Adobe 도움말에 나타나는 지침을 따라야 합니다. Specifically, you must place the header code in the `<head>` section of your document templates. Also, you must place the footer code just before the closing `</body>` tag. 이러한 포함 코드를 마크업에 배치하거나 비동기 방법을 사용하여 포함 코드를 첨부하거나 또는 어떤 식으로든 포함 코드를 감싸는 방식은 다이내믹 태그 관리에서 지원되는 구현이 *아닙니다*. 포함 코드를 받은 그대로 구현해야 합니다.
>
>지원되지 않는 방식으로 구현하면 예기치 않은 결과가 발생하고 고객 지원 센터 및 엔지니어링 센터에서 구현을 지원할 수 없게 됩니다.

1. 다이내믹 태그 관리 인터페이스에서 [!UICONTROL 포함] 탭을 열고 호스팅 옵션(예: Akamai)을 선택한 다음 스위치를 "On"으로 토글합니다. 

   단계 결과 1. 다이내믹 태그 관리의 포함 탭에 제공된 프로덕션 머리글 코드를 복사하여 사이트 HTML의 [!DNL HEAD] 섹션에 붙여넣습니다.

   ![](assets/dtm-embed.png)

   Place the code as close to the [!DNL <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">] 태그에 가깝게 넣으십시오. 이 코드 조각은 라이브 프로덕션 사이트의 모든 페이지에 넣어야 합니다.

   >[!NOTE]
   >
   >Production embed code reflects only the published items in that [property](../../../implement/c-implement-with-dtm/t-create-web-property.md#task_960467FBB7A54499AC228CB3AA3C4123). 그렇지만 스테이징에 대한 포함 코드는 게시 상태인지 또는 게시 취소 상태인지에 관계없이 연결된 속성의 모든 항목을 반영합니다. 프로덕션 사이트에서 게시 취소된 항목을 테스트하려면 [Akamai 호스팅에 대한 게시 취소 규칙 테스트](../../../implement/c-implement-with-dtm/c-rules/t-test-rules-akamai.md#task_B397167F9E9B4487957AD6CE2AD47259)의 지침에 따라 콘솔에서 스테이징을 로컬로 활성화하십시오.

1. 프로덕션 바닥글 코드를 복사하여 사이트 HTML의 [!DNL BODY] 섹션에 넣습니다.

   Place the code as close to the [!DNL </body>] 태그에 가깝게 넣으십시오.
1. 스테이징 머리글 및 바닥글 코드를 복사한 다음, 스테이징 사이트에서 위의 절차를 반복합니다.

   >[!NOTE]
   >
   >The difference between production and staging code snippets is the addition of [!DNL -staging] to the filename in the staging version. 바닥글 코드는 스테이징과 프로덕션에서 동일하게 유지됩니다.

