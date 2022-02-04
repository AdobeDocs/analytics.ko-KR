---
title: 현재 Adobe Analytics 릴리스 노트 보기
description: 최신 Analytics 릴리스 노트
source-git-commit: f8c2d98e49ead838781b175aa9f22712d6802a9d
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 98%

---


# 최신 Adobe Analytics 릴리스 노트

## Adobe Analytics의 새로운 기능 {#aa-features}

| 기능 | 설명 | 목표 날짜 |
| ----------- | ---------- | ------- |
| 해당 없음 |  | [일반 가용성](https://experienceleague.adobe.com/docs/analytics/technotes/releases.html?lang=ko-KR) 확인 |

{style=&quot;table-layout:auto&quot;}

## Adobe Analytics 및 Customer Journey Analytics의 수정 사항 {#aa-fixes}

* Analysis Workspace에서 대상 ID가 차원 항목에서 누락되는 문제가 해결되었습니다. (AN-262038; AN-279315)
* 사용자가 작업 영역에서 저장된 [!DNL Target] 프로젝트를 로드할 수 없도록 하는 문제가 해결되었습니다. (AN-277461; AN-275825; AN-266397)
* UI에 비활성화된 기능이 표시되는 문제가 해결되었습니다. (AN-262006)
* 작업 영역에서 날짜 필드를 사용하여 날짜를 변경할 때 발생한 문제가 해결되었습니다. 해당 수정 사항으로 인해 [!UICONTROL 종료 시간]이 오후 11시 59분에서 오전 12시로 변경되었습니다. (AN-277269; AN-277481)
* 새 세그먼트를 이미 로드된 세그먼트에 추가할 때 세그먼트 UI가 중단되는 문제가 해결되었습니다. (AN-260827)
* 사용자가 공유 작업 영역 프로젝트에 액세스할 수 없는 문제가 해결되었습니다. (AN-267529)
* 순환 날짜 범위의 시작 날짜가 종료 날짜보다 늦는 경우 표시되는 오류 메시지가 추가되었습니다. (AN-270488)
* 다양한 데이터 피드 문제가 해결되었습니다. (AN-275876; AN-270512; AN-277284; AN-277290; AN-274893; AN-274606; AN-269651)
* 그래프의 날짜 범위가 표의 데이터 필터를 무시하는 문제가 해결되었습니다. (AN-263999)
* 일광 절약 시간으로 인해 예약된 보고서가 예정보다 일찍 전송되는 문제가 해결되었습니다. (AN-276410; AN-276305)
* 작업 영역에서 프로젝트를 `.csv` 파일로 다운로드할 수 없는 문제가 해결되었습니다. (AN-275834)

### Adobe Analytics의 추가 수정 사항

AN-253294; AN-254976; AN-255377; AN-255561; AN-258550; AN-259336; AN-263935; AN-265094; AN-269441; AN-269486; AN-269855; AN-271166; AN-271588; AN-272088; AN-272249; AN-272859; AN-272873; AN-272885; AN-273229; AN-273913; AN-274237; AN-274472; AN-274491; AN-274619; AN-274766; AN-275248; AN-275259; AN-275271; AN-275315; AN-275388; AN-275418; AN-275597; AN-275643; AN-275650; AN-275651; AN-275675; AN-275682; AN-275704; AN-275711; AN-275796; AN-275834; AN-275923; AN-275941; AN-276044; AN-276125; AN-276157; AN-276397; AN-276597; AN-276789; AN-276834; AN-276861; AN-276870; AN-276963; AN-276975; AN-277000; AN-277044; AN-277093; AN-277200; AN-277215; AN-277271; AN-277281; AN-277362; AN-277419; AN-277492; AN-277498; AN-277533; AN-277619; AN-277675; AN-277681; AN-277767; AN-277805; AN-277810; AN-277818; AN-277875; AN-277933; AN-277988; AN-278105; AN-278115; AN-278122; AN-278192; AN-278407; AN-278437; AN-278559; AN-278604; AN-278610; AN-278709; AN-278835; AN-278849; AN-278881; AN-279067; AN-279103; AN-279111; AN-279219; AN-279237; AN-279312

## [!DNL Analytics] 관리자에 대한 중요 공지 {#aa-notices}

| 공지 | 추가 또는 업데이트 날짜 | 설명 |
| ----------- | ---------- | ---------- |
| 기존 Analytics OAuth/JWT 통합에 대한 허용 목록 EOL 확장 기능 만료 | 2022년 1월 14일 | **2022년 5월 25일**&#x200B;에 [Analytics 1.3 API, 1.4 SOAP API 및 레거시 Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) 허용 목록 확장 기능이 만료될 예정입니다. 이는 레거시 [!DNL Adobe Analytics] OAuth/JWT 자격 증명 추가 시간을 사용하여 클라이언트 통합을 [Adobe IMS 자격 증명](https://developer.adobe.com/console)으로 마이그레이션할 수 있도록 고객에게 제공되었던 기능입니다. 해당 만료는 필요한 IMS 마이그레이션을 완료하지 않은 [!DNL Adobe Analytics Livestream] 및 [!DNL Adobe Campaign] 고객에 영향을 주지만 이에 국한되지는 않습니다. 현재 허용 목록 확장 기능을 통해 기존 [!DNL Analytics] OAuth/JWT 자격 증명을 사용 중인 고객 및 2022년 5월 25일까지 IMS 자격 증명으로 마이그레이션을 완료하지 않은 고객은 Adobe 서비스에 액세스할 수 없게 됩니다. 라이브스트림 고객은 클라이언트 애플리케이션을 IMS 자격 증명으로 마이그레이션하는 방법에 대한 이 [지침](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md)을 참조할 수 있습니다. [!DNL Campaign] 고객은 Adobe 계정 팀에 최신 버전의 [!DNL Campaign]으로의 업그레이드에 대해 문의할 수 있습니다. |
| [!DNL Reports & Analytics]에 대한 EOL | 2022년 1월 4일 | **2023년 12월 31일**&#x200B;부로 Adobe는 및 관련 보고서와 기능에 대한 서비스를 중단할 예정입니다. [!DNL Reports & Analytics] [!DNL Reports & Analytics]가 제공하는 보고서, 시각화 및 기반 기술은 더 이상 Adobe의 기술 표준을 충족하지 않습니다. 대부분의 [!DNL Reports & Analytics] 기능은 [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=ko-KR)에서 사용할 수 있습니다. 2015년 Analysis Workspace가 출시된 이후 [!DNL Reports & Analytics] 기능이 Analysis Workspace로 이전되면서 워크플로 패리티의 한계점에 도달했습니다. [이 공지 사항은 서비스 종료 프로세스에 대해 설명합니다.](https://spark.adobe.com/page/6WnF8JK6IRDhf/) |
| Secure File Transfer Protocol(SFTP) 서비스 업그레이드 | 2022년 1월 13일 | **2022년 5월 2일**, [!DNL Adobe Analytics]는 파일 전송 보안을 개선하기 위해 Secure File Transfer Protocol(SFTP) 서비스를 업그레이드할 예정입니다. 이 변경 사항으로 일부 SFTP 클라이언트 구성은 더 이상 지원되지 않습니다. 또한 **2022년 3월 1일**&#x200B;까지 사용할 수 있는 몇 가지 연결 옵션을 추가할 예정입니다. 이는 SFTP를 사용하여 Adobe Analytics로 전송되거나 Adobe Analytics에서 검색된 데이터에만 영향을 미칩니다. FTP 프로토콜은 영향을 받지 않습니다. 서비스 중단을 방지하려면 SFTP 클라이언트(코드, 도구, 서비스)가 [여기](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html)에 설명된 변경 사항을 준수하는지 확인하십시오. |
| _글로벌 + 중국_ RDC 유형 | 2021년 11월 22일 | _글로벌 + 중국_&#x200B;은 [!UICONTROL 중국 성능 최적화 추가 기능 패키지]를 사용하여 글로벌 고객의 트래픽 라우팅을 간소화하는 새로운 지역 데이터 수집(RDC) 유형입니다. 이전까지는 데이터를 중국 수집 끝점으로 라우팅할지 또는 글로벌 수집 끝점 중 하나로 라우팅할지를 결정해야 했습니다. 이제 이 RDC *유형*&#x200B;을 선택하여 Adobe가 사용자의 지리적 위치를 기반으로 최적의 수집 끝점을 결정하도록 할 수 있습니다. |
| 데이터 소스의 전체 처리를 위한 EOL | 2021년 10월 18일 | **2022년 1월 31일**&#x200B;에 Adobe는 사용자가 오프라인 히트 데이터를 Analytics로 수집할 수 있는 전체 처리를 위한 수명을 종료합니다. 이 기능은 [대량 데이터 삽입 API](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md)를 통해 사용할 수 있습니다. [자세히 알아보기](https://experienceleague.adobe.com/docs/analytics/import/data-sources/data-types-and-categories/datasrc-fullproc-eol.html?lang=ko-KR?lang=ko-KR) |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement {#appm}

AppMeasurement 릴리스(버전 2.22.4)에 대한 최신 업데이트는 [JavaScript용 AppMeasurement 릴리스 정보](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=ko-KR)를 참조하십시오.