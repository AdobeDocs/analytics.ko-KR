---
description: 데이터 소스 템플릿에 대한 정보는 특정 외부 데이터 소스 집합을 데이터 소스로 전송하는 데 적합한 데이터 프레임워크를 제공합니다.
solution: Analytics
subtopic: Data sources
title: Data Sources 템플릿 개요
topic: Developer and implementation
uuid: e768bcff-a996-44c7-a7f2-9a2c651ecad9
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Data Sources 템플릿 개요

데이터 소스 템플릿에 대한 정보는 특정 외부 데이터 소스 집합을 데이터 소스로 전송하는 데 적합한 데이터 프레임워크를 제공합니다.

이 마법사에서 생성한 템플릿 파일은 가져오기를 시작하는 데 활용할 수 있습니다. 이 템플릿에서 정의한 열에 제한되지 않습니다. 선택한 데이터 처리 유형에 대해 지표나 정의가 지원된다면 필요에 따라 열을 추가할 수 있습니다. 

다음 섹션에서 각 유형에 대해 지원되는 지표와 차원을 볼 수 있습니다.

* [웹 로그](/help/import/c-data-sources/c-datasrc-types/datasrc-web-log.md)
* [트래픽](/help/import/c-data-sources/c-datasrc-types/datasrc-traffic.md)(더 이상 지원되지 않음)
* [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md)
* [거래 ID](/help/import/c-data-sources/c-datasrc-types/datasrc-transactionid.md)
* [방문자 ID](/help/import/c-data-sources/c-datasrc-types/datasrc-visitorid.md)
* [전체 처리](/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md)

For example, for a Visitor ID data type, you can add a column for any metric or dimensions listed in [Visitor ID](/help/import/c-data-sources/c-datasrc-types/datasrc-visitorid.md).

템플릿이 생성되면 템플릿을 다운로드하고 템플릿에 데이터를 입력한 다음 데이터를 데이터 소스 FTP 사이트로 업로드할 수 있습니다. 데이터 소스 서버가 처리를 완료하면 가져온 데이터를 마케팅 보고서에서 사용할 수 있습니다.

The Data Source template is a [!DNL .txt] file that you can open with any text editor. 하지만 Microsoft Excel이나 다른 스프레드시트 응용 프로그램을 사용하여 템플릿 작업을 하는 것이 더 쉽습니다. 템플릿 내용은 [!UICONTROL 데이터 소스 활성화 마법사]에서 선택한 사항에 따라 달라집니다.

자세한 내용은 [가져오기 파일 참조](/help/import/c-data-sources/datasrc-template/datasrc-import-file-reference.md).
