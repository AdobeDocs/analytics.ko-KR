---
description: 데이터 소스 템플릿에 대한 정보는 특정 외부 데이터 소스 집합을 데이터 소스로 전송하는 데 적합한 데이터 프레임워크를 제공합니다.
seo-description: 데이터 소스 템플릿에 대한 정보는 특정 외부 데이터 소스 집합을 데이터 소스로 전송하는 데 적합한 데이터 프레임워크를 제공합니다.
seo-title: Data Sources 템플릿 개요
solution: Analytics
subtopic: Data Sources
title: Data Sources 템플릿 개요
topic: 개발자 및 구현
uuid: E 768 BCFF-A 996-44 C 7-A 7 F 2-9 A 2 C 651 ECAD 9
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# Data Sources 템플릿 개요

데이터 소스 템플릿에 대한 정보는 특정 외부 데이터 소스 집합을 데이터 소스로 전송하는 데 적합한 데이터 프레임워크를 제공합니다.

이 마법사에서 생성한 템플릿 파일은 가져오기를 시작하는 데 활용할 수 있습니다. 이 템플릿에서 정의한 열에 제한되지 않습니다. 선택한 데이터 처리 유형에 대해 지표나 정의가 지원된다면 필요에 따라 열을 추가할 수 있습니다. 

다음 섹션에서 각 유형에 대해 지원되는 지표와 차원을 볼 수 있습니다.

* [웹 로그](../../../import/c-data-sources/c-datasrc-types/datasrc-web-log.md#concept_E25D89C8B90A41FEB7DF4E936CACEE2B)
* [트래픽](../../../import/c-data-sources/c-datasrc-types/datasrc-traffic.md#concept_F50D3AC6A5544D06BB81EF1E279576BC)(더 이상 지원되지 않음)
* [변환](../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0)
* [거래 ID](../../../import/c-data-sources/c-datasrc-types/datasrc-transactionid.md#concept_A97302E9EC45468A8F30285FACE8C776)
* [Visitor ID](../../../import/c-data-sources/c-datasrc-types/datasrc-visitorid.md#concept_1CFAA61D57A84B22A41F7A8E0DFCAAB5)
* [전체 처리](../../../import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#concept_975B1BB9981D49139B4EE09C78CDE6ED)

For example, for a Visitor ID data type, you can add a column for any metric or dimensions listed in [Visitor ID](../../../import/c-data-sources/c-datasrc-types/datasrc-visitorid.md#concept_1CFAA61D57A84B22A41F7A8E0DFCAAB5).

템플릿이 생성되면 템플릿을 다운로드하고 템플릿에 데이터를 입력한 다음 데이터를 데이터 소스 FTP 사이트로 업로드할 수 있습니다. 데이터 소스 서버가 처리를 완료하면 가져온 데이터를 마케팅 보고서에서 사용할 수 있습니다.

The Data Source template is a [!DNL .txt] file that you can open with any text editor. 하지만 Microsoft Excel이나 다른 스프레드시트 응용 프로그램을 사용하여 템플릿 작업을 하는 것이 더 쉽습니다. 템플릿 내용은 [!UICONTROL 데이터 소스 활성화 마법사]에서 선택한 사항에 따라 달라집니다.

see [가져오기 파일 참조](../../../import/c-data-sources/datasrc-template/datasrc-import-file-reference.md#concept_472095E1D011434D98A21C101A4618BD).
