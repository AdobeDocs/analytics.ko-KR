---
title: 개발 환경에 Adobe Analytics 배포
seo-title: 개발 환경에 Adobe Analytics 배포
description: Adobe Experience Platform Launch를 사용하여 개발 환경에 Adobe Analytics를 배포하는 방법을 살펴볼 수 있습니다.
seo-description: Adobe Experience Platform Launch를 사용하여 개발 환경에 Adobe Analytics를 배포하는 방법을 살펴볼 수 있습니다.
translation-type: tm+mt
source-git-commit: 4e7a8bab956503093633deff0a64e8c7af2d5497

---


# 개발 환경에 Analytics 구현 배포

시작 시 속성을 만들고 구성한 후에는 라이브러리를 배포하여 사이트에서 구현할 수 있습니다.

## 전제 조건

[Launch에서 Adobe Analytics에 대한 속성을 만들고 구성합니다](create-analytics-property.md). 도구에 액세스하고 Analytics 구현을 위한 공간을 만듭니다.

## 어댑터 및 환경 만들기

Launch는 코드를 배포하는 데 있어 많은 조직적 워크플로우를 지원합니다. Analytics 구현에 필요한 최소 구성 요소를 만들려면 다음 단계를 수행하십시오. 론치 관리자는 조직 내에서 Adobe 솔루션을 배포하기 위한 올바른 워크플로우를 설정할 수 있습니다.

1. [Adobe Experience Platform Launch](https://launch.adobe.com) 로 이동하여 메시지가 표시되면 로그인합니다.
2. 사이트에서 구현할 론치 속성을 클릭합니다.
3. 어댑터 탭을 클릭한 다음 어댑터 추가를 클릭합니다.
4. " Akamai "로 지정하고 유형 드롭다운에서 Akamai를 선택합니다. 저장을 클릭합니다.
5. 환경 탭으로 이동한 다음 새 환경 만들기를 클릭합니다.
6. 개발을 선택하고, "개발 환경" 로 지정한 다음 드롭다운에서 Akamai 어댑터를 선택합니다. 만들기를 클릭한 다음 닫기를 클릭합니다.
7. 환경 추가를 클릭하고 스테이징을 선택한 다음 이름을 "스테이징 환경" 로 지정한 다음 Akamai 어댑터를 선택합니다. 만들기를 클릭한 다음 닫기를 클릭합니다.
8. 환경 추가를 다시 클릭하고, 제작을 선택하고, 이름을 "프로덕션 환경" 로 지정한 다음 Akamai 어댑터를 선택합니다. 만들기를 클릭한 다음 닫기를 클릭합니다.

## 개발 라이브러리 구축

지금까지 수행된 모든 변경 사항과 구성에도 불구하고 코드가 실제로 게시되지는 않았습니다. 변경 내용 컬렉션으로 대략적으로 번역된 라이브러리를 만들면 사이트에서 사용할 코드를 게시할 수 있습니다.

1. [Adobe Experience Platform Launch](https://launch.adobe.com) 로 이동하여 메시지가 표시되면 로그인합니다.
2. 사이트에서 구현할 론치 속성을 클릭합니다.
3. 게시 탭을 클릭한 다음 새 라이브러리 추가를 클릭합니다.
4. 라이브러리 이름을'초기 변경 내용'으로 지정하고 개발 환경을 선택합니다.
5. Adobe Analytics, ID 서비스 및 코어를 자동으로 나열하는 [변경된 모든 리소스 추가] 를 클릭합니다.
6. 저장을 클릭합니다.
7. 게시 워크플로우 화면에서 새 라이브러리 옆의 드롭다운을 클릭하고 개발용으로 빌드를 클릭합니다. 몇 초 후에 라이브러리의 노란색 점이 녹색으로 바뀌면 빌드가 성공했음을 나타냅니다.
8. 환경 탭으로 이동한 다음 개발 환경을 클릭합니다.
9. ' 론치 설치'에서 코드 블록을 복사하여 조직의 웹 사이트 소유자에게 제공합니다.

## 웹 사이트의 개발 환경에 론치 설치

If you control your website's code, implement the two blocks of code in their respective locations (in the `<head>` tag and just above the closing `</body>` tag) on every page of your site. 이 코드는 일반적으로 사이트의 중요 템플릿에 배치됩니다. 구현 코드만 포함하는 빈 페이지는 다음과 같습니다.

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example page</title>
  <script src="//assets.adobedtm.com/launch-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx-development.min.js"></script>
</head>
<body>
   <p>This is a test page.</p>
   <script type="text/javascript">_satellite.pageBottom();</script>
</body>
</html>
```

## 문제 해결

**빌드 시도가 실패했습니다.**

일반적인 이유는 스테이징이나 프로덕션에 푸시된 다른 라이브러리에 요소가 이미 있기 때문입니다. 처음 라이브러리를 만들 때는 변경된 리소스만 라이브러리에 추가하도록 하십시오.

## 설명서 및 추가 리소스

- [론치 시작](https://docs.adobelaunch.com/getting-started): Launch의 기본 워크플로우 학습
- [론치 관리](https://docs.adobelaunch.com/administration): 어댑터 및 환경에 대한 자세한 내용

## 다음 단계

[Analytics 구현을 확인하고 프로덕션에 게시](validate-publish-prod.md): Adobe Analytics에서 가치 가져오기를 시작합니다.
