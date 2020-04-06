---
description: Adobe에서 데이터 소스에 대한 액세스 권한을 제공하는 방법에 대한 정보.
subtopic: Data sources
title: Data Sources 작동 방식
topic: Developer and implementation
uuid: ee9e6e74-9b00-4733-9a4b-d9f2b954cc7c
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Data Sources 작동 방식

Adobe에서 데이터 소스에 대한 액세스 권한을 제공하는 방법에 대한 정보.

>[!NOTE] 가져온 데이터가 데이터 소스를 통해 전송되면 JavaScript 비콘, ActionSource, 데이터 삽입 API 등과 같은 다른 수단으로 수집한 보고 데이터와 구별할 수 없게 됩니다. 데이터를 가져온 후에는 제거할 수 없습니다.

![](assets/data_sources_overview.png)

다음 두 가지 방법을 사용하여 데이터를 제출할 수 있습니다.

* [FTP](/help/import/c-data-sources/datasrc-how-data-sources-works.md#section_0E70022648F94061AF5B4AD6C7145243)
* [API](/help/import/c-data-sources/datasrc-how-data-sources-works.md#section_65DACC9CE00C437BBFDD02D19C25A4BD)

## FTP {#section_0E70022648F94061AF5B4AD6C7145243}

FTP 파일 전송을 사용하여 데이터 파일을 Data Sources로 가져오는 마케팅 보고서를 통해 FTP 기반 데이터 소스를 만들고 관리할 수 있습니다. 데이터 소스를 만든 후 Adobe는 데이터 소스 파일을 업로드하는 데 사용할 수 있는 FTP 위치를 제공합니다. 업로드되면 Data Sources는 자동으로 이를 찾아 처리합니다. 처리가 완료되면 마케팅 보고서에 데이터를 사용할 수 있습니다.

## API {#section_65DACC9CE00C437BBFDD02D19C25A4BD}

Adobe는 프로그래밍 방식으로 애플리케이션을 Data Sources에 연결할 수 있는 Data Sources API를 제공합니다. 이렇게 하면 중간 FTP 서버가 필요하지 않으며 HTTP, SOAP 및 REST를 통해 데이터를 전송할 수 있습니다.

Data [Sources API 설명서를 참조하십시오](https://github.com/AdobeDocs/analytics-1.4-apis/tree/master/docs/data-sources-api).
