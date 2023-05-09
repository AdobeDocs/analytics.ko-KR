---
title: 데이터 소스 관리
description: 데이터 소스 관리 인터페이스를 탐색합니다.
source-git-commit: e32a7c85e2f0629c04bcd7ed0fa80ec1593bb6e8
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 4%

---

# 데이터 소스 관리

데이터 소스 관리자를 사용하여 데이터 소스를 생성, 편집 또는 비활성화합니다. 이 인터페이스를 사용하여 데이터 소스 FTP 위치에 업로드된 파일의 상태를 추적할 수도 있습니다.

**[!UICONTROL 관리]** > **[!UICONTROL 모든 관리자]** > **[!UICONTROL 데이터 소스]**

오른쪽 상단의 보고서 세트 선택기를 사용하여 조직의 보고서 세트 간을 전환할 수 있습니다.

이 인터페이스에는 세 개의 기본 탭이 있습니다. **[!UICONTROL 관리]**, **[!UICONTROL 만들기]**, 및 **[!UICONTROL 파일 로그]**.

## 관리

다음 **[!UICONTROL 관리]** 탭은 조직이 만든 모든 데이터 소스를 처리합니다. FTP 정보를 보거나, 템플릿 파일에 사용된 변수를 편집하거나, 데이터 소스를 완전히 비활성화할 수 있습니다.

![관리](assets/manage.png)

가장 높은 데이터 소스는 항상 [!UICONTROL 웹 비콘]. 이 데이터 소스는 AppMeasurement를 통한 일반적인 데이터 수집에 사용하는 것입니다. 편집하거나 비활성화할 수 없습니다.

각 데이터 소스에는 다음 옵션이 있습니다.

* **[!UICONTROL 처리 다시 시작]**: 오류로 인해 이전에 중지된 데이터 소스 처리를 다시 시작합니다. 다음 오류가 발생할 때까지 처리가 계속됩니다. 데이터 소스는 선택하는 경우에만 데이터 소스 파일 처리를 중지합니다 **[!UICONTROL 오류 시 처리 중지]**.
* **[!UICONTROL 처리 완료]**: 더 이상 사용되지 않음 - 이 버튼은 [전체 처리 데이터 소스](full-processing-eol.md).
* **[!UICONTROL 오류 시 처리 중지]**: 오류가 발생할 때 처리 서버가 중지되도록 하는 확인란입니다. 선택할 때까지 데이터 소스가 처리를 다시 시작하지 않습니다 **[!UICONTROL 처리 다시 시작]**. 데이터 소스에 파일 오류가 발생하면 오류를 알리는 메시지를 받게 됩니다. Adobe이 오류가 있는 파일을 라는 폴더로 이동합니다. `files_with_errors` at.js 2. 문제를 해결했으면 처리를 위해 파일을 다시 전송합니다.
* **[!UICONTROL 구성]**: 이 데이터 소스에 대한 데이터 소스 만들기 마법사를 통해 사용자에게 연결되는 링크. 이 마법사를 사용하여 데이터 소스의 이름을 변경하거나 템플릿 파일을 다운로드할 때 자동으로 포함된 변수를 다시 구성할 수 있습니다.
* **[!UICONTROL FTP 정보]**: FTP 자격 증명이 표시되는 데이터 소스 만들기 마법사의 마지막 단계로 이동하는 링크입니다.

데이터 소스가 데이터를 수신하면 업로드된 파일에 대한 여러 열이 포함된 테이블이 표시됩니다.

* **[!UICONTROL 처리 큐의 파일]**: 파일 이름입니다.
* **[!UICONTROL 행]**: 파일에 있는 총 행 수입니다.
* **[!UICONTROL 오류]**: 오류가 발생하여 수집할 수 없는 행 수입니다.
* **[!UICONTROL 경고]**: 경고가 포함된 행 수입니다.
* **[!UICONTROL 수신]**: 보고서 세트의 시간대에서 파일을 받은 타임스탬프입니다.
* **[!UICONTROL 상태]**: 파일의 상태(`Success` 또는 `Failed`).

## 만들기

다음 **[!UICONTROL 만들기]** 탭에서는 데이터 소스 만들기 마법사의 시작점을 제공합니다.

![만들기](assets/create.png)

이전 버전의 Adobe Analytics에서는 데이터 소스의 카테고리와 유형이 더 유용했습니다. 그러나 여전히 제한된 사용:

* 데이터 소스 유형은 [관리](#manage) 데이터 소스 자체에 대한 탭 및 [파일 로그](#file-log) 각 개별 파일에 대한 탭.
* 일부 데이터 소스 유형에는 템플릿 파일을 다운로드할 때 변수가 자동으로 포함됩니다. 하지만 사용 가능한 차원 또는 지표가 설정된 차원을 준수하는 한 사용할 수 있습니다 [파일 형식](file-format.md).

이러한 이유 외에도 선택할 수 있는 모든 데이터 소스 카테고리와 유형은 효과적으로 동일합니다. 데이터 소스 사용 목적을 가장 잘 나타내는 카테고리 및 유형을 선택합니다.

그리고 [전체 처리 데이터 소스](full-processing-eol.md)여러 카테고리와 유형을 선택할 수 없습니다. 전체 처리 데이터 소스 유형을 선택하는 경우, **[!UICONTROL 활성화]** 버튼이 회색으로 표시됩니다.

## 파일 로그

다음 **[!UICONTROL 파일 로그]** 탭에서는 지정된 보고서 세트에 대해 업로드된 모든 데이터 소스 파일을 집계한 보기를 제공합니다.

![파일 로그](assets/file-log.png)

특정 데이터 소스를 찾는 데 도움이 되는 검색 창을 사용할 수 있습니다. 이 표에는 다음 열이 표시되어 있습니다.

* **[!UICONTROL 데이터 소스 이름]**: 데이터 소스의 이름입니다.
* **[!UICONTROL 유형]**: 데이터 소스의 유형입니다.
* **[!UICONTROL 파일 이름]**: 업로드된 파일의 이름입니다.
* **[!UICONTROL 행]**: 파일에 있는 총 행 수입니다.
* **[!UICONTROL 오류]**: 오류가 포함된 행 수입니다.
* **[!UICONTROL 경고]**: 더 이상 사용되지 않습니다. 경고가 포함된 행 수입니다.
* **[!UICONTROL 수신]**: Adobe이 파일 처리를 시작한 날짜 및 시간입니다.
* **[!UICONTROL 상태]**: 파일의 상태(`Success` 또는 `Failed`).