---
description: '"사용자는 캠페인을 통해 사이트로 클릭하여 들어온 후, 사이트 상의 어느 곳으로 갑니까?"라는 질문에 대답하는 데 유용합니다.'
keywords: Analytics Implementation
solution: Analytics
title: 캠페인 또는 추적 코드에 의한 경로 지정
topic: Developer and implementation
uuid: eb6e3484-1b40-4ec6-8017-ac1003cdf636
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 캠페인 또는 추적 코드에 의한 경로 지정

"사용자는 캠페인을 통해 사이트로 클릭하여 들어온 후, 사이트 상의 어느 곳으로 갑니까?"라는 질문에 대답하는 데 유용합니다.

이 질문에 대답하려면 이 보고서에 사용되는 [!UICONTROL sprop]를 한쪽으로 치워 놓아야 합니다. 그런 다음 데이터를 구조화하여 경로 지정이 활성화되어 있을 때 이해할 수 있는 방법으로 prop에 채워야 합니다.

다음 예의 경우, [!UICONTROL prop1]을 캠페인 경로 지정 prop으로 사용하게 됩니다. 이제 [!UICONTROL 페이지 이름] 변수에 입력하는 값과 동일한 값으로 이 [!UICONTROL sprop]를 채우려고 합니다. 아래를 참조하십시오.

```js
s.prop1=s.pageName;
```

사용자가 캠페인에서 클릭하지 않았다면 여러분이 모든 페이지에서 이렇게 해야 합니다. 사용자가 캠페인에서 클릭했고 캠페인의 랜딩 페이지에 있는 경우, 여러분은 캠페인과 [!UICONTROL pagename]의 연결로 prop을 채웁니다. 아래를 참조하십시오.

```js
 s.prop1=s.campaign + ' : ' + s.pageName;
```

클릭한 캠페인의 이름이 "banner1234"였고 랜딩한 페이지의 이름이 "Home Page"였다면, 해당 prop에서의 값은 "banner1234 : Home Page"가 됩니다. 이후의 모든 페이지에서는 위에서 보듯이 prop에 [!UICONTROL pagename]을 입력합니다.

사용자가 이 캠페인을 클릭하고 이 방문에서 총 4개의 페이지를 보면, 여러분은 다음과 같은 순서에 따라 sprop에서 다음 값을 얻습니다.

```js
"banner1234 : Home Page" > "Page 2" > "Page 3" > "Page 4"
```

이 방법으로 [!UICONTROL prop1]에서 캡처한 데이터를 확보하고 이 prop에서 경로 지정이 활성화되어 있으면, 이제 다양한 경로 지정 보고서 중 하나를 보고 사용자가 캠페인을 통해 클릭한 후 사이트에서 어떻게 경로를 이동하는지를 이해할 수 있습니다.

경로 보고서를 시작할 시작 페이지를 지정할 수 있습니다. 이 경우에는 캠페인 "banner 1234"에서 클릭한 후 사용자가 이동한 곳을 알기 위해 "banner1234 : Home Page"를 선택했습니다. 이 보고서는 많은 경로 보고서 중 하나의 한 가지 예일 뿐입니다.
