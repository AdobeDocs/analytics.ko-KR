---
title: 거래 ID 데이터 소스
description: 거래 ID 데이터 소스를 사용하는 일반적인 워크플로우에 대해 알아봅니다.
translation-type: tm+mt
source-git-commit: a5c3d9b2cd02dc7e89abb469e2e0e44985a17638

---


# 거래 ID 데이터 소스

거래 ID 데이터 소스를 사용하면 온라인 및 오프라인 데이터를 나란히 볼 수 있을 뿐만 아니라 데이터를 함께 연결할 수 있습니다. Analytics 구현에서 [`transactionID`](/help/implement/vars/page-vars/transactionid.md) 변수를 사용해야 합니다.

값이 들어 있는 온라인 히트를 전송하면 Adobe는 해당 시간에 설정되거나 지속되는 모든 변수의 &quot;스냅숏&quot;을 만듭니다. `transactionID` Data Sources를 통해 업로드된 일치하는 거래 ID가 있으면 오프라인 및 온라인 데이터가 함께 연결됩니다. 어떤 데이터 소스가 먼저 표시되는지는 중요하지 않습니다.

## 거래 ID 데이터 소스의 전체 워크플로우

다음 일반 워크플로우를 사용하여 거래 ID 데이터 소스 사용을 시작합니다.

1. 데이터 소스(&#39;범용&#39; 카테고리 및 &#39;범용 데이터 소스(거래 ID)&#39; 유형)를 만듭니다.
1. 데이터 피드 설정 마법사에 따라 데이터를 업로드하고 데이터 소스 템플릿 파일을 다운로드할 FTP 위치를 가져옵니다.
1. 변수를 포함하도록 구현을 `transactionID` 업데이트합니다.
1. Data Sources 파일을 `.fin` 파일로 FTP 사이트에 업로드합니다.
