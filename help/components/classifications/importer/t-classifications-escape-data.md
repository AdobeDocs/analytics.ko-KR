---
description: 분류 파일에 있는 분류 데이터를 이스케이프 처리하는 방법을 설명하는 절차입니다.
subtopic: Classifications
title: 분류 데이터 이스케이프 처리
feature: 관리 도구
uuid: 724edcc5-4990-4f24-afbb-9aef301791a7
exl-id: 0d3a0e91-5537-43ee-bd28-9907ee6eb331
translation-type: ht
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: ht
source-wordcount: '106'
ht-degree: 100%

---

# 분류 데이터 이스케이프 처리

분류 파일에 있는 분류 데이터를 이스케이프 처리하는 방법을 설명하는 절차입니다.

<!--Meike, please check this page against orginal. It might be missing information. -->

1. 분류 파일 형식이 v2.1인지 확인합니다.

   v2.1이 활성화되어 있으면 다음과 유사한 라인이 표시됩니다.

   >[!NOTE]
   >
   >v2.1의 형식을 지정하려면, **[!UICONTROL 분류 가져오기]** 페이지에서 파일을 내보낼 때 ([!UICONTROL 브라우저 내보내기]나 [!UICONTROL FTP 내보내기]) [!UICONTROL 견적 출력]을 활성화합니다.

1. 큰 따옴표 (`"`)로 특수 문자가 들어 있는 필드를 쌉니다.

이스케이프 처리된 셀에서는 큰 따옴표 문자가 두 개의 큰 따옴표 문자 (`" "`)로 바뀌어 나타날 수 있습니다. 예:

```
My String "of data"
```

이스케이프 처리된 셀:

```
"My String ""of data"""
```
