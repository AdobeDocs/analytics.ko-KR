---
description: 웹 사이트, 모바일 앱을 통해 수집되거나 웹 서비스 API 또는 데이터 소스를 이용하여 업로드되는 데이터는 Adobe의 Data Warehouse에서 처리되고 저장됩니다. 이 원시 클릭스트림 데이터는 Adobe Analytics에서 사용되는 데이터 세트를 이룹니다.
keywords: 클릭스트림, 데이터 피드, 데이터피드, 데이터 피드
title: Analytics 데이터 피드 개요
feature: Data Feeds
exl-id: 2cfff9ad-cdb5-4ae9-a266-4f3d3d046f0c
source-git-commit: 0916ef4ddc2ca65f01721f4d79d7af825dcf50e3
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 83%

---

# Analytics 데이터 피드 개요

>[!AVAILABILITY]
>
>이 페이지에 설명된 대상 유형 중 일부는 릴리스의 제한된 테스트 단계에 있으며 사용자 환경에서 아직 사용하지 못할 수 있습니다. 기능이 일반적으로 제공되면 이 메모는 제거됩니다. Analytics 릴리스 프로세스에 대한 자세한 내용은 [Adobe Analytics 기능 릴리스](/help/release-notes/releases.md)를 참조하십시오.

데이터 피드는 Adobe Analytics에서 원시 데이터를 가져오는 강력한 방법입니다. 이러한 원시 데이터는 Adobe 외부의 다른 플랫폼에서 조직의 재량에 따라 사용할 수 있습니다. 데이터는 매 시간이 끝날 때 시간별 배치로 전달되거나, 하루가 끝날 때 일별 배치로 전달됩니다.

## 사전 요구 사항

데이터 피드를 사용하기 전에 다음 요구 사항을 모두 충족하는지 확인하십시오.

* 데이터를 Adobe 데이터 수집 서버에 전송하는 작동 중인 구현. 다음을 참조하십시오 [구현의 유효성 검사 및 게시](/help/implement/launch/validate-publish-prod.md) 구현 안내서에서 참조하십시오.
* 계정이 Analytics 제품 관리자이거나 계정이 데이터 피드에 대해 액세스 권한이 있는 제품 프로필에 속합니다.
* Amazon S3, Google Cloud Platform, Azure RBAC 또는 Azure SAS에 구성된 버킷입니다.
* (레거시: 레거시 FTP 및 SFTP 대상 유형에만 필요) FTP 사이트 및 자격 증명(조직에서 제공한 FTP 자격 증명)을 사용할 수 있습니다.

## 권장 데이터 피드 리소스

1. Adobe ID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
2. 오른쪽 상단에 있는 9제곱 아이콘을 클릭한 다음 컬러 Analytics 로고를 클릭합니다.
3. 맨 위 탐색 막대에서 관리자 > 데이터 피드로 이동합니다.
4. [!UICONTROL 추가를 클릭합니다]. [!UICONTROL 피드 정보], [!UICONTROL 대상] 및 [!UICONTROL 데이터 열], 이렇게 세 가지 주요 범주가 있는 새 페이지가 나타납니다.
5. [!UICONTROL 피드 정보] 필드를 채웁니다.
   * 이름: &quot;데이터 피드 테스트&quot;와 같이 원하는 이름을 지정합니다.
   * 보고서 세트: 원하는 보고서 세트를 선택합니다.
   * 완료 시 이메일 보내기: 이메일을 입력합니다.
   * 피드 간격: 원하는 간격(시간별 또는 일별)을 선택합니다.
   * 프로세싱 지연: [!UICONTROL 지연 없음]으로 둘 수 있습니다.
   * 시작 및 종료 날짜: 이전 며칠 중에서 시작 날짜를 선택하고 오늘을 종료 날짜로 선택합니다.
6. [!UICONTROL 대상] 필드를 채웁니다.
   * 유형: FTP
   * 호스트: 원하는 FTP 대상 URL을 입력합니다. (예: `ftp://ftp.omniture.com`)
   * 경로: 비워 둘 수 있습니다.
   * 사용자 이름: FTP 사이트에 로그인할 사용자 이름을 입력합니다.
   * 암호 및 암호 확인: FTP 사이트에 로그인할 암호를 입력합니다.
7. [!UICONTROL 데이터 열 정의]를 채웁니다.
   * 드롭다운 목록에서 최신 &#39;모든 Adobe Columns&#39; 템플릿을 선택합니다.
   * 압축 포맷: Gzip
   * 패키징 타입: 여러 파일
   * 매니페스트: 파일 없음
8. 오른쪽 상단에 있는 [!UICONTROL 저장]을 클릭합니다.
9. 저장되면 이전 데이터 처리가 시작됩니다. 하루 동안 데이터 처리가 완료되면 파일이 FTP 사이트에 배치됩니다.
10. Windows 탐색기 또는 전용 FTP 클라이언트를 사용하여 FTP 사이트에 로그인합니다.
11. 로컬 시스템에 압축된 데이터 피드 파일을 다운로드합니다.
12. `.tar.gz` 파일 확장자를 지원하는 프로그램을 사용하여 압축 파일의 압축을 해제합니다.
13. 원하는 스프레드시트나 데이터베이스 애플리케이션에서 `hit_data.tsv` 파일을 열어 해당 날의 원시 데이터를 확인합니다.

## 다음 단계

데이터 피드를 얻는 기본 워크플로를 이해하면 조직 내의 팀과 함께 원시 데이터를 데이터베이스에 저장하거나 인제스트할 수 있습니다.

* [데이터 피드 모범 사례](/help/export/analytics-data-feed/data-feeds-best-practices.md): 데이터 피드 만들기 및 관리에 대한 우수 사례입니다.
* [데이터 피드 만들기](create-feed.md): 개별 필드를 자세히 설명하는 데이터 피드 작성을 위한 기술 세부 정보
* [데이터 피드 관리](df-manage-feeds.md): 데이터 피드 인터페이스 탐색에 대한 자세한 정보
* [데이터 피드 콘텐츠](c-df-contents/datafeeds-contents.md): 압축 파일의 항목 이해 <!-- Is this still the output users can download from the destination? I aske Jun. -->
* [데이터 열 정의](c-df-contents/datafeeds-reference.md): 사용 가능한 모든 열의 포괄적인 목록.
* 데이터 피드 인터페이스를 탐색하는 비디오:

  >[!VIDEO](https://video.tv.adobe.com/v/25452/?quality=12)

* 데이터 피드 ID 찾는 방법에 대한 비디오

  >[!VIDEO](https://video.tv.adobe.com/v/335747/?quality=12)