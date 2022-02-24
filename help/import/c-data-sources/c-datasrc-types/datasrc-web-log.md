---
description: 웹 로그 데이터 소스를 통해 표준 웹 서버 로그 파일을 가져올 수 있습니다.
subtopic: Data sources
title: 웹 로그
topic-fix: Developer and implementation
feature: Data Sources
exl-id: 11c4f21a-de07-436e-a05e-ab6769cb3e21
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: ht
source-wordcount: '171'
ht-degree: 100%

---

# 웹 로그

웹 로그 데이터 소스를 통해 표준 웹 서버 로그 파일을 가져올 수 있습니다.

다음의 일반적인 웹 서버 로그 유형이 지원됩니다.

| 열 이름 | 설명 |
|--- |--- |
| NCSA 일반 로그 | Apache 기본값 |
| NCSA 확장(통합) | Apache |
| W3C 확장 로그 | IIS 4.0 이상에서 사용됨 |
| Microsoft IIS 로그 | IIS 3.0 이전에서 사용됨 |

데이터 소스가 처리하는 기본 로그 파일 필드에는 IP 주소, 요청 날짜/시간, URL이 포함됩니다. NCSA 확장 형식 등의 일부 경우 데이터 소스는 레퍼러 및 사용자 에이전트 필드도 처리합니다.

페이지 보기 횟수, 방문 횟수, 방문자 수에 대한 표준 마케팅 보고서를 사용하여 웹 로그 데이터를 볼 수 있습니다. 보고서 지표가 기본적으로 쿠키를 기반으로 하고 웹 서버 로그가 IP 주소를 기반으로 하기 때문에, 웹 서버 로그를 특히 해당 용도를 위한 별도의 보고서 세트로 가져오는 것이 좋습니다.

웹 서버 로그 파일에 대한 자세한 정보는 웹 서버 문서를 참조하십시오.
