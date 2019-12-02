---
description: 웹 사이트, 모바일 앱을 통해 수집되거나 웹 서비스 API 또는 데이터 소스를 이용하여 업로드되는 데이터는 Adobe의 Data Warehouse에서 처리되고 저장됩니다. 이 원시 클릭스트림 데이터는 Adobe Analytics에서 사용되는 데이터 세트를 이룹니다.
keywords: clickstream;data feed;datafeed;Data Feed
solution: Analytics
title: Analytics 데이터 피드 개요
uuid: 6bdbe90c-e6ed-4bb0-b5be-24fd795adde4
translation-type: tm+mt
source-git-commit: 7db88bce7b3d0f90fa5b50664d7c0c23904348c0

---


# Analytics 데이터 피드 개요

데이터 피드는 Adobe Analytics에서 원시 데이터를 가져오는 강력한 방법입니다. 이 원시 데이터는 Adobe 외부의 다른 플랫폼에서 조직의 재량에 따라 사용할 수 있습니다. 데이터는 매 시간 종료 시 시간별 배치로 전달되거나, 하루의 완료 시 일별 배치로 전달됩니다.

## 전제 조건

데이터 피드를 사용하기 전에 다음 요구 사항을 모두 충족해야 합니다.

* FTP 사이트 및 자격 증명을 바로 사용할 수 있습니다. 데이터 피드는 서버 대상으로만 전송할 수 있습니다. 조직은 일반적으로 FTP 자격 증명을 제공합니다. Adobe는 요청 시 적절한 양의 스토리지를 FTP 위치에 제공할 수 있습니다. 데이터 피드에 대한 FTP 대상을 요청하려면 고객 지원 센터에 문의하십시오.
* Adobe 데이터 수집 서버로 데이터를 전송하는 작업 중인 구현입니다. 구현 [사용 안내서의 Launch에서](../../implement/implement-with-launch/validate-publish-prod.md) 구현 유효성 확인 및 게시를 참조하십시오.
* 계정이 Analytics 제품 관리이거나 계정이 데이터 피드에 액세스할 수 있는 제품 프로필에 속합니다.

## 시작하기 단계

1. Adobe ID 자격 증명을 사용하여 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)에 로그인합니다.
2. 오른쪽 상단에 있는 9제곱 아이콘을 클릭한 다음 컬러 Analytics 로고를 클릭합니다.
3. 상단 탐색 막대에서 관리 &gt; 데이터 피드로 이동합니다.
4. [!UICONTROL 추가를 클릭합니다]. 다음 세 가지 주요 카테고리가 있는 새 페이지가 나타납니다.피드 정보 [!UICONTROL ,]대상 [!UICONTROL 및]데이터 열 [!UICONTROL 정의].
5. 피드 [!UICONTROL 정보 필드를] 채웁니다.
   * 이름:"데이터 피드 테스트"와 같이 원하는 이름입니다.
   * 보고서 세트:원하는 보고서 세트를 선택합니다.
   * 완료 시 이메일:이메일을 입력합니다.
   * 피드 간격:원하는 간격(시간별 또는 일별)을 선택합니다.
   * 처리 지연:지연 없음으로 [!UICONTROL 둘 수 있습니다].
   * 시작 및 종료 날짜:며칠 전과 오늘 중에서 시작 날짜를 선택합니다.
6. 대상 [!UICONTROL 필드를] 채웁니다.
   * 유형:FTP
   * 호스트:원하는 FTP 대상 URL을 입력합니다. 예, `ftp://ftp.omniture.com`.
   * 경로:비워 둘 수 있음
   * 사용자 이름:FTP 사이트에 로그인할 사용자 이름을 입력합니다.
   * 암호 및 암호 확인:FTP 사이트에 로그인할 암호를 입력합니다.
7. 데이터 [!UICONTROL 열 정의를 채웁니다].
   * 드롭다운에서 최신 '모든 Adobe 열' 템플릿을 선택합니다.
   * 압축 형식:Gzip
   * 패키징 유형:여러 파일
   * 매니페스트:파일 없음
8. 오른쪽 [!UICONTROL 상단에 있는] 저장을 클릭합니다.
9. 일단 저장되면 내역 데이터 처리가 시작됩니다. 하루 동안 데이터 처리가 완료되면 파일은 FTP 사이트에 배치됩니다.
10. Windows 탐색기 또는 전용 FTP 클라이언트를 사용하여 FTP 사이트에 로그인합니다.
11. 로컬 시스템에 압축된 데이터 피드 파일을 다운로드합니다.
12. 파일 확장자를 지원하는 프로그램을 사용하여 압축 파일의 압축을 `.tar.gz` 해제합니다.
13. 원하는 스프레드시트나 데이터베이스 애플리케이션에서 파일을 열어 해당 날의 원시 데이터를 볼 수 있습니다. `hit_data.tsv`

## 다음 단계

데이터 피드 획득의 기본 워크플로우를 이해하면 조직 내의 팀과 함께 Raw 데이터를 데이터베이스에 저장하거나 인제스트할 수 있습니다.

[데이터 피드](create-feed.md)만들기:데이터 피드 만들기에 대한 기술 세부 정보개별 필드를 자세히[설명합니다. 데이터 피드](df-manage-feeds.md)관리:데이터 피드 인터페이스[탐색에 대한 자세한 내용](c-df-contents/datafeeds-contents.md):압축된 파일[내의 내용을 파악데이터 열 정의](c-df-contents/datafeeds-reference.md):사용 가능한 모든 열의 포괄적인 목록

## 추가 리소스

데이터 피드 인터페이스 탐색 비디오:

> [!VIDEO](https://www.youtube.com/watch?v=m_fb--gNtR4)
