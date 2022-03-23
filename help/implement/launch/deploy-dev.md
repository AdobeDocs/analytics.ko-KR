---
title: 개발 환경에 Adobe Analytics 배포
description: 태그를 사용하여 Adobe Analytics를 개발 환경에 배포하는 방법에 대해 알아봅니다.
feature: Launch Implementation
exl-id: 324943db-cb0b-40b1-8884-56bb3f608278
source-git-commit: f4b495b11bcbd55bc8448f2c9c09268547fb9750
workflow-type: ht
source-wordcount: '592'
ht-degree: 100%

---

# 개발 환경에 Analytics 구현 배포

태그 속성을 만들고 구성했으면 사이트에 라이브러리를 배포하고 코드를 구현할 준비가 된 것입니다.

## 사전 요구 사항

[Adobe Analytics에 대한 태그 속성 만들기 및 구성](create-analytics-property.md): 도구에 액세스하고 Analytics 구현을 위한 공간을 만듭니다.

## 어댑터 및 환경 만들기

태그는 코드를 배포할 때 여러 조직의 워크플로를 포함합니다. 아래 단계에 따라 Analytics 구현에 필요한 최소 구성 요소를 만듭니다. 태그 관리자는 조직 내에서 Adobe 솔루션을 배포하기 위해 올바른 워크플로를 설정할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [데이터 수집 UI](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 사이트에서 구현할 태그 속성을 클릭합니다.
3. **[!UICONTROL 호스트]**&#x200B;를 클릭한 후 **[!UICONTROL 호스트 추가]**&#x200B;를 클릭합니다.
4. 이름을 `"Adobe managed"`로 지정하고 유형 드롭다운에서 **[!UICONTROL Managed by Adobe]**&#x200B;를 선택합니다. [저장]을 클릭합니다.
5. **[!UICONTROL 환경]**&#x200B;으로 이동한 다음 **[!UICONTROL 환경 추가]**&#x200B;를 클릭합니다.
6. **[!UICONTROL 개발]**&#x200B;을 선택하고 이름을 `"Dev Environment"`로 지정한 다음 드롭다운에서 Adobe 관리 호스트를 선택합니다. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
7. 모달 창에 [웹 설치 지침]이 표시됩니다. 나중에 이 창으로 돌아오겠습니다. 이제 **[!UICONTROL 닫기]**&#x200B;를 클릭하십시오.
8. **[!UICONTROL 환경 추가]**&#x200B;를 클릭하고 **[!UICONTROL 스테이징]**&#x200B;을 선택한 다음 이름을 `"Staging Environment"`로 지정한 후 Adobe 관리 호스트를 선택합니다. **[!UICONTROL 만들기]**&#x200B;를 클릭한 다음 설치 지침 모달 창을 닫습니다.
9. **[!UICONTROL 환경 추가]**&#x200B;를 다시 클릭하고 **[!UICONTROL 프로덕션]**&#x200B;을 선택한 다음 이름을 `"Production Environment"`로 지정한 후 Adobe 관리 호스트를 선택합니다. **[!UICONTROL 만들기]**&#x200B;를 클릭한 다음 설치 지침 모달 창을 닫습니다.

## 개발 라이브러리 빌드

지금까지 모든 변경 및 구성 작업을 수행했지만 실제로 어떤 코드도 게시되지 않았습니다. 일련의 변경 사항으로 대략적으로 번역된 라이브러리를 만들면 사이트에서 사용할 코드를 게시할 수 있습니다.

1. AdobeID 자격 증명을 사용하여 [데이터 수집 UI](https://experience.adobe.com/data-collection)에 로그인합니다.
2. 사이트에서 구현할 태그 속성을 클릭합니다.
3. **[!UICONTROL 플로우 게시]** 탭을 클릭한 다음 **[!UICONTROL 라이브러리 추가]**&#x200B;를 클릭합니다. 이 페이지에 대한 자세한 내용은 태그 설명서의 [게시 개요](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=ko-KR)를 참조하십시오.
4. 라이브러리 이름을 `'Initial changes'`로 지정하고 개발 환경을 선택합니다.
5. Adobe Analytics, ID 서비스 및 핵심을 자동으로 나열하는 **[!UICONTROL 변경된 모든 리소스 추가]**&#x200B;를 클릭합니다.
6. **[!UICONTROL 저장]**&#x200B;을 클릭합니다.
7. 게시 워크플로 화면으로 돌아가서 새 라이브러리 옆에 있는 드롭다운을 클릭하고 **[!UICONTROL 개발용 빌드]**&#x200B;를 클릭합니다. 잠시 후에 라이브러리에 있는 노란색 점이 성공적으로 빌드되었음을 나타내는 녹색으로 바뀝니다.
8. **[!UICONTROL 환경]**&#x200B;으로 이동한 다음 개발 환경 오른쪽의 설치 아이콘을 클릭합니다. 이렇게 하면 [웹 설치 지침] 모달 창이 다시 표시됩니다.
9. 코드 블록을 복사하여 조직의 웹 사이트 소유자에게 제공합니다.

## 웹 사이트의 개발 환경에 태그 설치

웹 사이트의 코드를 제어하는 경우 각 코드 블록을 각각의 위치에 구현합니다.

* 메인 태그는 사이트의 `<head>` 태그에 속합니다.
* 태그를 동기적으로 로드하고자 하는 경우 사이트에서 두 번째 코드 블록을 `</body>` 닫기 태그 바로 아래에 포함시켜야 합니다. [웹 설치 지침]에서 **[!UICONTROL 라이브러리를 비동기적으로 로드]** 옵션을 토글하여 라이브러리 태그를 동기적으로 로드할 수 있습니다.

태그 코드는 일반적으로 사이트의 아주 중요한 템플릿에 배치됩니다. 구현 코드가 포함된 빈 페이지 모양은 다음과 같습니다.

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
   <!-- Only include this extra code if you load tags synchronously -->
   <script type="text/javascript">_satellite.pageBottom();</script>
</body>
</html>
```

## 문제 해결

**빌드 시도에 실패했습니다.**

일반적인 이유는 스테이징 또는 프로덕션으로 푸시된 다른 라이브러리에 요소가 이미 있기 때문입니다. 라이브러리를 처음 만들 때 변경된 리소스만 라이브러리에 추가해야 합니다.

## 다음 단계

[Analytics 구현을 확인하고 프로덕션에 게시](validate-publish-prod.md): Adobe Analytics의 가치 창출을 시작합니다.
