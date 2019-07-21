---
description: 가져오기 템플릿 파일은 가져오기를 시작할 수 있도록 만들어졌습니다.
seo-description: 가져오기 템플릿 파일은 가져오기를 시작할 수 있도록 만들어졌습니다.
seo-title: 가져오기 파일 템플릿 생성
solution: Analytics
subtopic: Data Sources
title: 가져오기 파일 템플릿 생성
topic: 개발자 및 구현
uuid: BCD 90 E 34-42 E 6-4 CD 1-B 67 E -87586 DEA 25 D 8
translation-type: tm+mt
source-git-commit: 76d0ce11d9b560e0df866be9e753804b6fa4bb3d

---


# 가져오기 파일 템플릿 생성

가져오기 템플릿 파일은 가져오기를 시작할 수 있도록 만들어졌습니다.

이 템플릿에서 정의한 열에 제한되지 않습니다. 선택한 데이터 처리 유형에 대해 지표나 정의가 지원된다면 필요에 따라 열을 추가할 수 있습니다. 다음 섹션에서 각 유형에 대해 지원되는 지표와 차원을 볼 수 있습니다. [웹 로그](../../../import/c-data-sources/c-datasrc-types/datasrc-web-log.md#concept_E25D89C8B90A41FEB7DF4E936CACEE2B), [트래픽](../../../import/c-data-sources/c-datasrc-types/datasrc-traffic.md#concept_F50D3AC6A5544D06BB81EF1E279576BC), [전환](../../../import/c-data-sources/c-datasrc-types/datasrc-conversion.md#concept_FA3B6557128649C0B662E95C6B617FA0), [거래 ID](../../../import/c-data-sources/c-datasrc-types/datasrc-transactionid.md#concept_A97302E9EC45468A8F30285FACE8C776), [방문자 ID](../../../import/c-data-sources/c-datasrc-types/datasrc-visitorid.md#concept_1CFAA61D57A84B22A41F7A8E0DFCAAB5), [전체 처리](../../../import/c-data-sources/c-datasrc-types/datasrc-full-processing.md#concept_975B1BB9981D49139B4EE09C78CDE6ED)). For example, for a traffic data type, you can add a column for any metric or dimensions listed in [Traffic](../../../import/c-data-sources/c-datasrc-types/datasrc-traffic.md#concept_F50D3AC6A5544D06BB81EF1E279576BC).

템플릿이 생성되면 템플릿을 다운로드하고 템플릿에 데이터를 입력한 다음 데이터를 데이터 소스 FTP 사이트로 업로드할 수 있습니다. Data Sources 서버에서 처리된 데이터는 Analytics 보고서에서 사용할 수 있습니다.

데이터 소스 템플릿은 모든 텍스트 편집기로 열 수 있는 .txt 파일입니다. 하지만 Microsoft Excel이나 다른 스프레드시트 응용 프로그램을 사용하여 템플릿 작업을 하는 것이 더 쉽습니다. 템플릿 내용은 데이터 소스 활성화 마법사에서 선택한 사항에 따라 달라집니다.

자세한 내용은 다음을 참조하십시오. [가져오기 파일 참조](../../../import/c-data-sources/datasrc-template/datasrc-import-file-reference.md#concept_472095E1D011434D98A21C101A4618BD).

1. Analytics에 로그인.
1. In the Suite header, select **[!UICONTROL Admin]** &gt; **[!UICONTROL Data Sources]**.
1. **[!UICONTROL Data Sources 생성]** 탭에서 템플릿 카테고리와 유형을 선택합니다.
1. Review the Activation Instructions/Information, then click **[!UICONTROL Activate]**.

   단계 결과 1. 데이터 소스 활성화 마법사에서 템플릿 생성 옵션을 선택합니다.

   | 마법사 페이지 | 필드 | 설명 |
   |--- |--- |--- |
   | 1 | 이름 | Analytics가 Data Sources 관리자에 표시하는 템플릿 이름. |
   | 1 | 이메일 | 해당 데이터 소스 템플릿 사용에 관련된 모든 알림을 수신하는 이메일 주소. |
   | 1 | 관련 요금 확인란 | 이 데이터 소스 템플릿 사용과 관련된 요금에 동의함을 나타내는 확인란을 선택합니다. |
   | 2 | 지표 선택 | 이 데이터 소스를 사용하여 가져올 지표를 선택합니다. Analytics 에서는 3 단계에서 선택한 데이터 소스 카테고리와 유형을 기반으로 특정 지표를 권장합니다. 다른 지표를 지정하려면 빈 필드에 이름을 입력한 후 확인란을 선택하여 지표를 활성화합니다. |
   | 3 | 지표 매핑 | Analytics 이벤트를 선택하여 마법사 페이지 2에서 선택한 각 가져온 지표를 받습니다. 이는 이전에 데이터 소스를 통해 수신할 가져온 지표 데이터에 대응하는 이름을 할당한 새로운 미할당 이벤트입니다.  eVar, 제품 또는 추적 코드 변수가 대상 변수이고 업로드한 값이 기존의 캡처 값과 일치하는 경우 업로드한 이벤트는 지표를 기존 값에 추가합니다. 예를 들어 이미 제품 보기 횟수, 체크아웃, 주문을 지표로 가지고 있는 제품 데이터 차원과 함께 "오프라인 주문"을 생성할 수 있습니다.  |
   | 4 | 데이터 차원 선택 | 데이터 차원을 선택하여 이 데이터 소스에서 가져온 지표를 분류합니다. Analytics 에서는 3 단계에서 선택한 데이터 소스 유형을 기반으로 특정 데이터 차원을 권장합니다. 다른 데이터 차원을 지정하려면 빈 필드에 이름을 입력한 후 확인란을 선택하여 데이터 차원을 활성화합니다. |
   | 5 | 데이터 차원 매핑 | 표준 보고서 또는 eVar를 선택하여 마법사 4페이지에서 선택한 각 가져온 데이터 차원을 수신합니다. |

1. 템플릿 생성 후에는 데이터를 적절한 데이터 소스 템플릿 열로 복사하십시오. 이때 해당 데이터 열에 필요한 데이터 형식을 따라야 합니다.

   단계 결과 1. 원하는 명명 규칙에 따라 데이터 소스 파일을 저장하십시오. 모든 데이터 소스 파일에 대해 일관된 명명 규칙을 사용하는 것이 좋습니다. 확장자를 사용하지 않거나 사용하려면 .txt 또는 .tsv와 같은 일반적인 파일 확장자를 사용하십시오. 

