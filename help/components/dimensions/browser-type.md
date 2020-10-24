---
title: 브라우저 유형
description: 브라우저를 만든 조직입니다.
translation-type: ht
source-git-commit: d3f92d72207f027d35f81a4ccf70d01569c3557f
workflow-type: ht
source-wordcount: '133'
ht-degree: 100%

---


# 브라우저 유형

브라우저 유형 차원은 방문자가 사용하는 브라우저를 만든 조직을 나열합니다. 이 차원은 방문자가 주로 사용하는 브라우저를 확인하려는 경우 유용합니다. 동일한 브라우저의 서로 다른 버전을 별도의 차원 항목으로 나열하지 않는다는 점에서 &#39;브라우저&#39; 차원보다 높은 가치를 제공합니다.

## 이 차원을 데이터로 채우기

이 차원은 Adobe 내부의 조회 테이블을 참조합니다. 조회 값은 이미지 요청에 있는 `User-Agent` HTTP 헤더를 기반으로 합니다. AppMeasurement 라이브러리를 사용하는 경우(Adobe Experience Platform Launch 등을 통해) 이 차원은 즉시 작동합니다. 

## 차원 항목

차원 항목에는 브라우저를 만드는 조직이 포함됩니다. 일반적인 차원 항목에는 `"Google"`([!DNL Chrome] 작성자), `"Apple"`([!DNL Safari] 작성자), `"Microsoft"`([!DNL Edge] 작성자) 및 `"Mozilla"`([!DNL Firefox] 작성자) 등이 포함됩니다.
