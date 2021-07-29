---
title: 개발 환경에 Adobe Analytics 배포
description: 태그를 사용하여 개발 환경에 Adobe Analytics을 배포하는 방법을 알아봅니다.
exl-id: 324943db-cb0b-40b1-8884-56bb3f608278
source-git-commit: ea6812c8e596773abb8a05bbdb37bc641967c9b8
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 59%

---

# 개발 환경에 Analytics 구현 배포

태그 속성을 만들고 구성했으면 사이트에 라이브러리를 배포하고 코드를 구현할 준비가 된 것입니다.

>[!NOTE]
>Adobe Experience Platform Launch은 Experience Platform에서 데이터 수집 기술 세트로 브랜딩되었습니다. 그 결과 제품 설명서에서 몇 가지 용어 변경 사항이 롤아웃되었습니다. 용어 변경 내용을 통합 참조하려면 다음 [document](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en)을 참조하십시오.

## 사전 요구 사항

[Adobe Analytics ](create-analytics-property.md)에 대한 태그 속성을 만들고 구성합니다. 도구에 액세스하고 Analytics 구현을 위한 공간을 만듭니다.

## 어댑터 및 환경 만들기

태그는 코드를 배포할 때 여러 조직의 워크플로우를 포함합니다. 다음 단계에 따라 Analytics 구현에 필요한 최소 구성 요소를 만듭니다. 태그 관리자는 조직 내에서 Adobe 솔루션을 배포하기 위해 올바른 워크플로우를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [데이터 수집 UI](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 사이트에서 구현할 태그 속성을 클릭합니다.
3. 어댑터 탭을 클릭한 다음 어댑터 추가를 클릭합니다.
4. 이름을 &quot;Akamai&quot;로 지정하고 유형 드롭다운에서 Akamai를 선택합니다. 저장을 클릭합니다.
5. 환경 탭으로 이동한 다음 새 환경 만들기를 클릭합니다.
6. 개발을 선택하고 이름을 &quot;Dev Environment&quot;로 지정한 다음 드롭다운에서 Akamai 어댑터를 선택합니다. 만들기를 클릭한 다음 닫기를 클릭합니다.
7. 환경 추가를 클릭하고 스테이징을 선택한 다음 이름을 &quot;Staging Environment&quot;로 지정한 후 Akamai 어댑터를 선택합니다. 만들기를 클릭한 다음 닫기를 클릭합니다.
8. 환경 추가를 다시 클릭하고 프로덕션을 선택한 다음 이름을 &quot;Production Environment&quot;로 지정한 후 Akamai 어댑터를 선택합니다. 만들기를 클릭한 다음 닫기를 클릭합니다.

## 개발 라이브러리 빌드

지금까지 모든 변경 및 구성 작업을 수행했지만 실제로 어떤 코드도 게시되지 않았습니다. 일련의 변경 사항으로 대략적으로 번역된 라이브러리를 만들면 사이트에서 사용할 코드를 게시할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [데이터 수집 UI](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 사이트에서 구현할 태그 속성을 클릭합니다.
3. 게시 탭을 클릭한 다음 새 라이브러리 추가를 클릭합니다.
4. 라이브러리 이름을 &#39;Initial changes&#39;로 지정하고 개발 환경을 선택합니다.
5. Adobe Analytics, ID 서비스 및 핵심을 자동으로 나열하는 변경된 모든 리소스 추가를 클릭합니다.
6. 저장을 클릭합니다.
7. 게시 워크플로 화면으로 돌아가서 새 라이브러리 옆에 있는 드롭다운을 클릭하고 개발용 빌드를 클릭합니다. 잠시 후에 라이브러리에 있는 노란색 점이 성공적으로 빌드되었음을 나타내는 녹색으로 바뀝니다.
8. 환경 탭으로 이동한 다음 개발 환경을 클릭합니다.
9. 태그 설치 아래에서 코드 블록을 복사하여 조직의 웹 사이트 소유자에게 제공합니다.

## 웹 사이트의 개발 환경에 태그 설치

웹 사이트의 코드를 제어하는 경우 사이트의 모든 페이지에서 해당 위치 (`<head>` 태그와 `</body>` 닫기 태그 바로 위)에 두 개의 코드 블록을 구현합니다. 이 코드는 일반적으로 사이트의 아주 중요한 템플릿에 배치됩니다. 구현 코드가 포함된 빈 페이지 모양은 다음과 같습니다.

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

- [빠른 시작 안내서](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html?lang=en): 태그 구현의 기본 워크플로우를 알아봅니다
- [게시 개요](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=en): 게시 및 환경에 대해 자세히 알아보기

## 다음 단계

[Analytics 구현을 확인하고 프로덕션에 게시](validate-publish-prod.md): Adobe Analytics의 가치 창출을 시작합니다.
