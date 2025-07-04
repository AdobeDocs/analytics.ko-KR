---
title: 늦게 도착하는 히트
description: 데이터 피드에서 늦게 도착하는 히트를 처리하는 방법을 알아봅니다.
feature: Data Feeds
exl-id: c99a702b-2aaa-47a6-958a-1e5ab66961ba
source-git-commit: 81cbb115d50e1f55a67aac8b107749d0a5a5928b
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 85%

---

# 늦게 도착하는 히트

데이터 피드에서 지정된 시간 또는 일수 (예: 타임스탬프가 지정된 히트 또는 데이터 소스) 동안 작업 처리를 완료한 후에 내역 데이터가 도착할 수 있습니다. 늦게 도착하는 히트는 데이터 피드에 내역 데이터를 포함하도록 도움을 주기 위해 Adobe가 제공하는 백엔드 사용자 지정 설정입니다.

## 히트 작업은 얼마나 늦게 도착합니까?

데이터 피드는 일반적으로 데이터를 처리할 때 보고 창 내에서만 데이터를 조회합니다 (일반적으로 가장 최근 시간 또는 일수). 피드에서 해당 보고 기간의 처리를 마친 후에 데이터가 도착하는 경우 해당 데이터는 데이터 피드에 포함되지 않습니다.

이때 늦게 도착하는 히트가 활성화되면 이 데이터를 포함하도록 처리 방법이 변경됩니다. 데이터 피드에서 데이터를 처리할 때마다 데이터 피드는 도착한 모든 히트를 조회하고 FTP 사이트로 전송된 다음번 데이터 피드 파일에 데이터를 배치합니다.

## 늦게 도착하는 히트 활성화

Adobe는 개별 데이터 피드에서 늦게 도착하는 히트를 수동으로 활성화할 수 있습니다. 이 작업을 수행하기 전에 다음 사항을 고려하십시오.

* 늦게 도착하는 히트가 활성화되면 다른 날짜의 데이터가 데이터 피드에 자주 표시됩니다. 데이터 피드를 수집하는 데 사용하는 플랫폼이 동일한 파일 내에서 다른 요일의 데이터를 수용할 수 있는지 확인합니다.
* 데이터 피드 파일이 다시 처리되는 경우 처음 5일 이내에 다시 처리되면 원본 파일에 포함된 늦게 도착하는 히트가 다시 처리된 파일에 포함됩니다. 5일 후에는 늦게 도착하는 히트가 재처리된 파일에 포함되지 않습니다.

기존 반복되는 데이터 피드에 대해 늦게 도착하는 히트를 활성화하려면 서비스 대상 사용자에게 고객 지원 센터에 연락하여 다음 내용을 전달하라고 안내합니다.

* 특정 데이터 피드에 대해 늦게 도착하는 히트를 활성화하려는 경우 참고 사항
* 보고서 세트 ID
* 데이터 피드 이름
