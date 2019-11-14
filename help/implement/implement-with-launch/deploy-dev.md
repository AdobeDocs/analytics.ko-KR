---
title: 개발 환경에 Adobe Analytics 배포
description: Adobe Experience Platform Launch를 사용하여 Adobe Analytics를 개발 환경에 배포하는 방법에 대해 알아봅니다.
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 개발 환경에 Analytics 구현 배포

Launch에서 속성을 만들고 구성했으면 사이트에 라이브러리를 배포하고 코드를 구현할 준비가 된 것입니다.

## 전제 조건

[Launch에서 Adobe Analytics에 대한 속성 만들기 및 구성](create-analytics-property.md): 도구에 액세스하고 Analytics 구현을 위한 공간을 만듭니다.

## 어댑터 및 환경 만들기

Launch는 코드를 배포할 때 여러 조직의 워크플로우를 포함합니다. 다음 단계에 따라 Analytics 구현에 필요한 최소 구성 요소를 만듭니다. Launch 관리자는 조직 내에서 Adobe 솔루션을 배포하기 위해 올바른 워크플로우를 설정할 수 있습니다.

1. [Adobe Experience Platform Launch](https://launch.adobe.com)로 이동한 후 메시지가 표시되면 로그인합니다.
2. 사이트에서 구현할 Launch 속성을 클릭합니다.
3. 어댑터 탭을 클릭한 다음 어댑터 추가를 클릭합니다.
4. 이름을 "Akamai"로 지정하고 유형 드롭다운에서 Akamai를 선택합니다. 저장을 클릭합니다.
5. 환경 탭으로 이동한 다음 새 환경 만들기를 클릭합니다.
6. 개발을 선택하고 이름을 "Dev Environment"로 지정한 다음 드롭다운에서 Akamai 어댑터를 선택합니다. 만들기를 클릭한 다음 닫기를 클릭합니다.
7. 환경 추가를 클릭하고 스테이징을 선택한 다음 이름을 "Staging Environment"로 지정한 후 Akamai 어댑터를 선택합니다. 만들기를 클릭한 다음 닫기를 클릭합니다.
8. 환경 추가를 다시 클릭하고 프로덕션을 선택한 다음 이름을 "Production Environment"로 지정한 후 Akamai 어댑터를 선택합니다. 만들기를 클릭한 다음 닫기를 클릭합니다.

## 개발 라이브러리 빌드

지금까지 모든 변경 및 구성 작업을 수행했지만 실제로 어떤 코드도 게시되지 않았습니다. 일련의 변경 사항으로 대략적으로 번역된 라이브러리를 만들면 사이트에서 사용할 코드를 게시할 수 있습니다.

1. [Adobe Experience Platform Launch](https://launch.adobe.com)로 이동한 후 메시지가 표시되면 로그인합니다.
2. 사이트에서 구현할 Launch 속성을 클릭합니다.
3. 게시 탭을 클릭한 다음 새 라이브러리 추가를 클릭합니다.
4. 라이브러리 이름을 'Initial changes'로 지정하고 개발 환경을 선택합니다.
5. Adobe Analytics, ID 서비스 및 핵심을 자동으로 나열하는 변경된 모든 리소스 추가를 클릭합니다.
6. 저장을 클릭합니다.
7. 게시 워크플로우 화면으로 돌아가서 새 라이브러리 옆에 있는 드롭다운을 클릭하고 개발용 빌드를 클릭합니다. 잠시 후에 라이브러리에 있는 노란색 점이 성공적으로 빌드되었음을 나타내는 녹색으로 바뀝니다.
8. 환경 탭으로 이동한 다음 개발 환경을 클릭합니다.
9. Launch 설치 아래에서 코드 블록을 복사하여 조직의 웹 사이트 소유자에게 제공합니다.

## 웹 사이트의 개발 환경에 Launch 설치

웹 사이트의 코드를 제어하는 경우 사이트의 모든 페이지에서 해당 위치(`<head>` 태그와 `</body>` 닫기 태그 바로 위)에 두 개의 코드 블록을 구현합니다. 이 코드는 일반적으로 사이트의 아주 중요한 템플릿에 배치됩니다. 구현 코드가 포함된 빈 페이지 모양은 다음과 같습니다.

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

**빌드 시도에 실패했습니다.**

일반적인 이유는 스테이징 또는 프로덕션으로 푸시된 다른 라이브러리에 요소가 이미 있기 때문입니다. 라이브러리를 처음 만들 때 변경된 리소스만 라이브러리에 추가해야 합니다.

## 문서 및 추가 리소스

- [시작](https://docs.adobelaunch.com/getting-started):Launch의 기본 워크플로우 살펴보기
- [실행 관리](https://docs.adobelaunch.com/administration):어댑터 및 환경에 대한 자세한 내용

## 다음 단계

[Analytics 구현을 확인하고 프로덕션에 게시](validate-publish-prod.md): Adobe Analytics의 가치 창출을 시작합니다.
