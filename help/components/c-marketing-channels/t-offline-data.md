---
description: 마케팅 채널 보고서에 오프라인 데이터를 추가합니다.
seo-description: 마케팅 채널 보고서에 오프라인 데이터를 추가합니다.
seo-title: 오프라인 데이터 추가
solution: Analytics
subtopic: 마케팅 채널
title: 오프라인 데이터 추가
topic: Reports and Analytics
uuid: bbf4661a-b6b1-4a89-a3cf-ae8dd785d37d
translation-type: tm+mt
source-git-commit: 0dbc8ac9b416ce50f197a884bb71c6cd389cd0bb

---


# 오프라인 데이터 추가

마케팅 채널 보고서에 오프라인 데이터를 추가합니다.

온라인 채널을 이용하면 검색 엔진, 인터넷 광고, 참조 도메인, 이메일 캠페인 등과 같은 소스를 통해 방문하는 방문자의 데이터를 분류할 수 있습니다. 오프라인 채널은 TV 광고, 신문 또는 잡지 광고를 보고 사이트를 방문한 방문자에게 적용됩니다.

**마케팅 채널 보고서에 데이터 소스 통합**

[데이터 소스의 데이터](https://marketing.adobe.com/resources/help/en_US/sc/datasources/c_faq.html)를 마케팅 채널 보고서에 통합하려면 다음에 유의하십시오.

* [transactionID](https://marketing.adobe.com/resources/help/en_US/sc/datasources/c_Transaction_ID.html)와 함께 분석 보고서로 전달된 표준 히트는 정상적으로 마케팅 채널 처리 규칙을 통해 처리됩니다.
* 분석으로 전달되는 모든 `transactionID` 데이터 소스는 표준 히트를 처리한 것과 같은 마케팅 채널에 자동으로 연결됩니다.
* 다른 모든 데이터 소스 데이터는 마케팅 채널 처리 규칙을 통하지 않습니다.

데이터 소스에 대한 자세한 내용은 [데이터 소스](https://marketing.adobe.com/resources/help/en_US/sc/datasources/index.html) 도움말을 참조하십시오.

오프라인 채널 데이터를 분류하려면 데이터 소스에서 데이터를 활성화한 다음 템플릿을 다운로드해서 편집하십시오.

[데이터 소스 사용자 안내서](https://marketing.adobe.com/resources/help/en_US/sc/datasources/index.html)의 "데이터 소스 작업"을 참조하십시오.

**오프라인 데이터 추가**

1. Click **[!UICONTROL Admin]** &gt; **[!UICONTROL Data Sources]**.
1. 데이터 소스 페이지에서 **[!UICONTROL 만들기]를 클릭합니다.**
1. Under **[!UICONTROL 1. Select Category]**, select **[!UICONTROL Offline Channel Data]**.
1. Under **[!UICONTROL 2. Select Type]**, select **[!UICONTROL Offline Channel Data]**.
1. Click **[!UICONTROL Activate.]**
1. 데이터 소스 활성화 마법사가 표시하는 메시지에 따라 오프라인 지표를 보고 지표에 매핑합니다.
1. 템플릿 파일을 편집기(예: Excel)로 다운로드해서 편집합니다.

   [데이터 소스 사용자 안내서](https://marketing.adobe.com/resources/help/en_US/sc/datasources/index.html)의 "데이터 소스 파일 만들기"를 참조하십시오.

1. Upload the file as described in "Uploading a Data Sources File" in the [Data Sources User Guide](https://marketing.adobe.com/resources/help/en_US/sc/datasources/index.html).
