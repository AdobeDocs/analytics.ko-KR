---
title: 현재 Adobe Analytics 릴리스 정보
description: 현재 Adobe Analytics 릴리스 정보 보기
feature: Release Notes
exl-id: 97d16d5c-a8b3-48f3-8acb-96033cc691dc
source-git-commit: adbd342948ce3c38107a86613d77a9bf90a7df97
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 90%

---

# 현재 Adobe Analytics 릴리스 정보 (2025년 6월 릴리스)

**마지막 업데이트**: 2025년 6월 24일 수요일

이번 릴리스 정보에는 2025년 6월 18일부터 7월 15일까지의 릴리스 기간이 포함됩니다. Adobe Analytics 릴리스는 기능 배포에 대한 보다 확장 가능한 단계별 접근 방식을 고려하는 [연속 게재 모델](releases.md)에서 작동합니다. 따라서 이들 릴리스 정보는 월별로 여러 차례 업데이트됩니다. 이들 릴리스 정보를 정기적으로 확인하십시오.

## 새로운 기능 또는 개선 사항 {#features}

| 기능 | 설명 | [롤아웃 시작](releases.md) | [일반 가용성](releases.md) |
| ----------- | ---------- | ------- | ---- |
| **새 Report Builder에서 보안 클라우드 대상 지원** | Javascript Report Builder 추가 기능은 이제 다음 클라우드 스토리지 대상으로 보고서 내보내기를 지원합니다.<ul><li>Amazon S3 Role ARN</li><li>Google Cloud 플랫폼</li><li>Azure SAS</li><li>Azure RBAC</li></ul><p>이전에는 FTP 및 이메일 대상만 사용할 수 있었습니다. 보안 문제로 인해 FTP는 더 이상 지원되지 않습니다.</p><p>자세한 내용은 [클라우드 대상으로 내보내 통합 문서 예약](/help/analyze/report-builder/report-builder-export.md)을 참조하십시오.</p><p>이러한 변경 사항 외에 Adobe Analytics에서 위치를 만들 때 [클라우드 가져오기 및 내보내기 위치 구성](/help/components/locations/configure-import-locations.md)에 설명된 대로 [사용 방법] 필드에서 Report Builder에 위치를 사용할 수 있는 옵션을 제공합니다.</p> |  | 2025년 6월 19일 (원래는 6월 18일) |
| **새로운 미리보기 경험** | 세그먼트, 계산된 지표 등을 미리 보는 데 사용되는 미리보기 패널이 이제 도넛 시각화 대신 가로 막대 시각화를 사용합니다. |  | 2025년 6월 18일 |
| **수정된 속성 모델 대화 상자** | 이제 속성 모델 대화 상자에서 컨테이너와 기간을 별도로 정의할 수 있습니다. |  | 2025년 6월 18일 |
| **고객 속성 UI에 대한 탐색이 업데이트되었습니다.** | 이제 Adobe Experience Cloud의 앱 선택기에서 고객 속성 사용자 인터페이스에 바로 액세스할 수 있습니다. |  | TBD |
| **스트리밍 미디어: 일정 데이터 지원** | 이제 과거 라이브 스트리밍 미디어 콘텐츠의 예약된 데이터를 업로드하여 시청자 수를 보다 쉽고 정확하게 추적할 수 있습니다. 다음은 일정 데이터 업로드가 지원되는 라이브 콘텐츠의 예입니다.<ul><li>FAST(무료 광고 지원 TV) 플랫폼</li><li>로컬 스트림</li><li>라이브 스포츠</li></ul>일정 데이터를 업로드하면 업로드 파일에서 지정한 시간 동안 실행된 개별 프로그램의 시청자 수 데이터를 추적할 수 있습니다. 특정 주제나 프로그램 세그먼트에 대한 시청자 수 데이터를 수집할 수도 있습니다. 이러한 기능은 스트리밍 미디어 컬렉션을 어떻게 구현하든 관계없이 사용할 수 있습니다.<p>이전에는 라이브 콘텐츠를 분석할 때 주어진 세션을 특정 프로그램에 정확하게 연결하는 것이 어려웠고, 주어진 세션을 개별 주제나 프로그램 세그먼트에 연결하는 것도 불가능했습니다. 자세히 알아보기 |  | 2025년 8월 15일(원래 2025년 6월 25일) |

## Adobe Analytics의 수정 사항

**A4T**: AN-379045
**Advertising Analytics**: AN-377338
**경고**: AN-377229
**Analysis Workspace**: AN-378891; AN-379589; AN-379604; AN-381270; AN-382264; AN-382414;
**API 1.4**: AN-380188
**API 2.0**: AN-373078; AN-379006; AN-381248
**분류**: AN-379209; AN-379315; AN-379567; AN-379573; AN-379749; AN-379764; AN-379818; AN-380433; AN-381670; AN-381751; AN-381994; AN-382055; AN-382682; AN-383059; AN-383409
**기여도 분석**: AN-369822
**데이터 피드**: AN-365552; AN-367158; AN-378288; AN-379754; AN-380433; AN-380855; AN-380959; AN-381115; AN-381657; AN-381931
**Data Warehouse**: AN-379244
**플랫폼**: AN-375847
**처리 규칙**: AN-375157
**Report Builder**: AN-371395; AN-372174; AN-373815; AN-383194
**서버 호출**: AN-380930
**사용 및 액세스 로그**: AN-372130; AN-382123
**가상 보고서 세트**: AN-382010


## 서비스 종료(EOL) 알림 {#eol}

| EOL 제품 또는 기능 | 추가 또는 업데이트 일자 | 설명 |
| --- | --- | --- |
| **레거시 Report Builder** | 2025년 6월 18일 | 기존 Report Builder 추가 기능은 2026년 6월에 지원이 중단됩니다. 모든 사용자는 기존 통합 문서를 새로운 [Report Builder](https://experienceleague.adobe.com/ko/docs/analytics/analyze/report-builder/rb-overview)로 업그레이드해야 합니다. 새로운 Report Builder는 Adobe Analytics와 Customer Journey Analytics 고객 모두에게 제공됩니다. 이는 [거의 동일한 기능](https://experienceleague.adobe.com/ko/docs/analytics/analyze/report-builder/convert-workbooks#unsupported)과 더불어 여러 가지 편리하고 새로운 기능과 개선된 UI를 제공합니다. 업그레이드 프로세스를 용이하게 하기 위해 새로운 Report Builder에는 간편한 통합 문서 변환 기능이 포함되어 있습니다. 새로운 Report Builder는 Microsoft Store를 통해 다운로드할 수 있는 추가 기능으로만 제공됩니다. 대부분의 조직에서는 사용자에게 추가 기능을 제공하기 전에 내부 승인 절차를 거쳐야 합니다. 이 프로세스에 시간을 할애하고 지금부터 조직과 협력하여 EOL 날짜 전에 통합 문서를 업그레이드할 충분한 시간을 확보하십시오. |
| **레거시 도메인 또는 레거시 SSO를 통한 액세스** | 2025년 4월 10일 | Adobe는 보안을 강화하고 로그인 환경을 간소화하기 위해 사용자가 Adobe Analytics에 액세스하는 방식을 업데이트할 계획입니다. 이러한 업데이트의 일환으로 `my.omniture.com`을 비롯한 기존 도메인 또는 기존 SSO를 통한 액세스는 **2026년 1월 2일**&#x200B;부터 영구 중단됩니다. 이 날짜 이후에는 기존 로그인 자격 증명과 기존 SSO가 더 이상 작동하지 않습니다. 모든 사용자는 Adobe Experience Cloud ID를 사용하여 `experience.adobe.com`을 통해 로그인해야 합니다. Experience Cloud ID와 관련하여 도움이 필요한 경우, 조직의 Adobe Analytics 관리자 또는 [Adobe 고객 지원 센터](https://helpx.adobe.com/kr/contact.html)에 문의하십시오. |
| **Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션** | 2025년 1월 17일 | Adobe I/O JWT 자격 증명을 사용하는 Adobe Analytics API 및 Livestream 고객은 **2025년 6월 30일**&#x200B;까지 Adobe I/O OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 2024년 5월 1일부터는 Adobe I/O를 사용하여 새 JWT 자격 증명을 만들 수 없습니다. JWT를 사용하는 고객은 OAuth 서버 간 자격 증명을 새로 만들거나 기존 JWT 자격 증명을 OAuth 서버 간 자격 증명으로 마이그레이션해야 합니다. 또한 고객은 새 OAuth 서버 간 자격 증명을 사용하려면 클라이언트 애플리케이션을 업데이트해야 합니다. <ul><li>[서비스 계정(JWT) 자격 증명에서 마이그레이션](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration)</li><li>[OAuth를 사용한 신규 및 기존 애플리케이션 구현 안내서](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)<li>[새 OAuth 서버 간 자격 증명 사용](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/implementation)</li><li>[FAQ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/faqs)</li></ul> |
| **Adobe Analytics API (버전 1.4)** | 2024년 7월 17일 | **2026년 8월 12일**&#x200B;에 다음과 같은 Analytics Legacy API 서비스가 종료되며 해당 서비스를 사용하여 빌드한 현재 모든 통합 기능은 더 이상 작동하지 않습니다.<ul><li>Adobe Analytics API (버전 1.4)</li><li>Adobe Analytics WSSE 인증</li></ul><p>Adobe Analytics API(버전 1.4)를 사용하는 통합은 [Adobe Analytics 2.0 API](https://developer.adobe.com/analytics-apis/docs/2.0/)로 마이그레이션되어야 하며 WSSE 통합은 [Adobe Developer Console](https://developer.adobe.com/console)의 OAuth 기반 인증 프로토콜로 마이그레이션되어야 합니다.</p><p>자주 묻는 질문에 대한 답변과 자세한 안내는 [Adobe Analytics 1.4 API EOL FAQ](/help/admin/c-admin-api/c-admin-14-api-eol.md)를 참조하십시오.</p> |



## AppMeasurement

AppMeasurement 릴리스에 대한 최신 업데이트는 [AppMeasurement 릴리스 정보](https://github.com/adobe/appmeasurement/releases)를 참조하십시오.


## 관련 리소스

* [2025년 이전 릴리스 정보](/help/release-notes/2025.md)
* [Customer Journey Analytics 릴리스 정보](https://experienceleague.adobe.com/docs/analytics-platform/using/releases/latest.html)
* [스트리밍 미디어 컬렉션 릴리스 정보](https://experienceleague.adobe.com/docs/media-analytics/using/additional-resources/release-notes.html)
* [Adobe Experience Cloud 제품](https://business.adobe.com/products/adobe-experience-cloud-products.html)의 최신 릴리스 업데이트
