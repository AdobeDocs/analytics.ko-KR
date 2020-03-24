---
description: 가져오기 템플릿 파일은 가져오기를 시작할 수 있도록 만들어졌습니다.
subtopic: Data sources
title: 파일 가져오기 템플릿 생성
topic: Developer and implementation
uuid: bcd90e34-42e6-4cd1-b67e-87586dea25d8
translation-type: ht
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# 파일 가져오기 템플릿 생성

가져오기 템플릿 파일은 가져오기를 시작할 수 있도록 만들어졌습니다.

이 템플릿에서 정의한 열에 제한되지 않습니다. 선택한 데이터 처리 유형에 대해 지표나 정의가 지원된다면 필요에 따라 열을 추가할 수 있습니다. 다음 섹션에서 각 유형에 대해 지원되는 지표와 차원을 볼 수 있습니다. [웹 로그](/help/import/c-data-sources/c-datasrc-types/datasrc-web-log.md), [트래픽](/help/import/c-data-sources/c-datasrc-types/datasrc-traffic.md), [전환](/help/import/c-data-sources/c-datasrc-types/datasrc-conversion.md), [거래 ID](/help/import/c-data-sources/c-datasrc-types/datasrc-transactionid.md), [방문자 ID](/help/import/c-data-sources/c-datasrc-types/datasrc-visitorid.md), [전체 처리](/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md)). 예를 들어 트래픽 데이터 유형의 경우 [트래픽](/help/import/c-data-sources/c-datasrc-types/datasrc-traffic.md)의 지표나 차원에 대해 열을 추가할 수 있습니다.

템플릿이 생성되면 템플릿을 다운로드하고 템플릿에 데이터를 입력한 다음 데이터를 데이터 소스 FTP 사이트로 업로드할 수 있습니다. 데이터 소스 서버가 처리를 완료하면 가져온 데이터를 Analytics 보고서에서 사용할 수 있습니다.

데이터 소스 템플릿은 모든 텍스트 편집기로 열 수 있는 .txt 파일입니다. 하지만 Microsoft Excel이나 다른 스프레드시트 응용 프로그램을 사용하여 템플릿 작업을 하는 것이 더 쉽습니다. 템플릿 내용은 데이터 소스 활성화 마법사에서 선택한 사항에 따라 달라집니다.

자세한 내용은 다음을 참조하십시오. [가져오기 파일 참조](/help/import/c-data-sources/datasrc-template/datasrc-import-file-reference.md).

1. Analytics에 로그인.
1.  Suite 헤더에서 **[!UICONTROL 관리]** > **[!UICONTROL Data Sources]**&#x200B;를 선택합니다.
1. **** 데이터 소스 생성 탭에서 템플릿 카테고리와 유형을 선택합니다. 
1. 활성화 지침/정보를 검토한 후 **[!UICONTROL 활성화]**&#x200B;를 클릭합니다.

   단계 결과 1. 데이터 소스 활성화 마법사에서 템플릿 생성 옵션을 선택합니다.

   | 마법사 페이지 | 필드 | 설명 |
   |--- |--- |--- |
   | 1 |  이름  | Data Sources 관리자에서 Analytics가 표시하는 템플릿 이름. |
   | 1 | 이메일 | 해당 데이터 소스 템플릿 사용에 관련된 모든 알림을 수신하는 이메일 주소. |
   | 1 | 관련 요금 확인란 | 확인란을 선택하면 해당 데이터 소스 템플릿 사용에 따라 발생하는 요금에 동의함을 나타냅니다. |
   | 2 | 지표 선택 | 이 데이터 소스를 사용하여 가져올 지표를 선택합니다. Analytics에서는 3단계에서 선택한 데이터 소스 카테고리와 유형을 기준으로 특정 지표를 권장합니다.  다른 지표를 지정하려면 빈 필드에 이름을 입력한 후 확인란을 선택하여 지표를 활성화합니다. |
   | 3 | 지표 매핑 | Analytics 이벤트를 선택하여 마법사 페이지 2에서 선택한 각각의 가져온 지표를 수신합니다.  이는 이전에 데이터 소스를 통해 수신할 가져온 지표 데이터에 대응하는 이름을 할당한 새로운 미할당 이벤트입니다.  eVar, 제품 또는 추적 코드 변수가 대상 변수이고 업로드한 값이 기존의 캡처 값과 일치하는 경우 업로드한 이벤트는 지표를 기존 값에 추가합니다. 예를 들어 이미 제품 보기 횟수, 체크아웃, 주문을 지표로 가지고 있는 제품 데이터 차원과 함께 &quot;오프라인 주문&quot;을 생성할 수 있습니다.  |
   | 4 | 데이터 차원 선택 | 데이터 차원을 선택하여 이 데이터 소스에서 가져온 지표를 분류합니다. Analytics에서는 3단계에서 선택한 데이터 소스 유형을 기준으로 특정 데이터 차원을 권장합니다. 다른 데이터 차원을 지정하려면 빈 필드에 이름을 입력한 후 확인란을 선택하여 데이터 차원을 활성화합니다. |
   | 5 | 데이터 차원 매핑 | 표준 보고서 또는 eVar를 선택하여 마법사 4페이지에서 선택한 각 가져온 데이터 차원을 수신합니다. |

1. 템플릿 생성 후에는 데이터를 적절한 데이터 소스 템플릿 열로 복사하십시오. 이때 해당 데이터 열에 필요한 데이터 형식을 따라야 합니다.

   단계 결과 1. 원하는 명명 규칙에 따라 데이터 소스 파일을 저장하십시오. 모든 데이터 소스 파일에 대해 일관된 명명 규칙을 사용하는 것이 좋습니다. 확장자를 사용하지 않거나 사용하려면 .txt 또는 .tsv와 같은 일반적인 파일 확장자를 사용하십시오.

