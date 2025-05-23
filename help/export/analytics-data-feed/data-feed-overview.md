---
description: 데이터 피드를 사용하여 Adobe Analytics에서 원시 데이터를 가져오는 방법에 대해 알아봅니다. 데이터 피드 사용을 위한 사전 요구 사항을 확인하고 다음 작업을 수행하십시오.
keywords: 클릭스트림, 데이터 피드, 데이터피드, 데이터 피드
title: Analytics 데이터 피드 개요
feature: Data Feeds
exl-id: 2cfff9ad-cdb5-4ae9-a266-4f3d3d046f0c
source-git-commit: 08e29da4847e8ef70bd4435949e26265d770f557
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 79%

---

# Analytics 데이터 피드 개요

데이터 피드는 Adobe Analytics에서 원시 데이터를 가져오는 강력한 방법입니다. 이러한 원시 데이터는 Adobe 외부의 다른 플랫폼에서 조직의 재량에 따라 사용할 수 있습니다. 데이터는 매 시간이 끝날 때 시간별 배치로 전달되거나, 하루가 끝날 때 일별 배치로 전달됩니다.

## 사전 요구 사항

데이터 피드를 사용하기 전에 다음 요구 사항을 모두 충족하는지 확인하십시오.

* 데이터를 Adobe 데이터 수집 서버에 전송하는 작동 중인 구현. 구현 안내서에서 [구현 유효성 검사 및 퍼블리싱](/help/implement/launch/validate-publish-prod.md)을 참조하십시오.
* 계정이 Analytics 제품 관리자이거나 계정이 데이터 피드에 대해 액세스 권한이 있는 제품 프로필에 속합니다.
* Amazon S3, Google Cloud Platform, Azure RBAC 또는 Azure SAS에 구성된 버킷입니다.
* (이전: 이전 FTP 및 SFTP 대상 유형에만 필요) FTP 사이트 및 자격 증명 준비(FTP 자격 증명은 조직에서 제공)

## 다음 단계

다음 리소스는 데이터 피드를 가져오는 기본 워크플로를 이해하는 데 도움이 됩니다. 기본 워크플로를 이해하면 조직 내의 팀과 함께 원시 데이터를 데이터베이스에 저장하거나 인제스트할 수 있습니다.

* [데이터 피드 모범 사례](/help/export/analytics-data-feed/data-feeds-best-practices.md): 데이터 피드를 만들고 관리하기 위한 모범 사례.
* [데이터 피드 만들기](create-feed.md): 개별 필드를 자세히 설명하는 데이터 피드 작성을 위한 기술 세부 정보
* [데이터 피드 관리](df-manage-feeds.md): 데이터 피드 인터페이스 탐색에 대한 자세한 정보
* [데이터 피드 내용](c-df-contents/datafeeds-contents.md): 압축된 파일 <!-- Is this still the output users can download from the destination? I aske Jun. -->의 내용을 이해합니다.
* [데이터 열 정의](c-df-contents/datafeeds-reference.md): 사용 가능한 모든 열의 포괄적인 목록.

>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [데이터 피드 인터페이스 탐색](https://video.tv.adobe.com/v/3428565?quality=12&learn=on&captions=kor){target="_blank"}을 참조하십시오.

>[!ENDSHADEBOX]



>[!BEGINSHADEBOX]

데모 비디오를 보려면 ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [데이터 피드 ID 찾기](https://video.tv.adobe.com/v/3418482?quality=12&learn=on&captions=kor){target="_blank"}를 참조하십시오.

>[!ENDSHADEBOX]
