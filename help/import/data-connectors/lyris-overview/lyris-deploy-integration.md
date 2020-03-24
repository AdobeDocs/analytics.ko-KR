---
description: 3단계 배포 프로세스에 대해 설명합니다.
title: 통합 배포
uuid: a3c0ef21-ed9a-44d7-bdce-19b3bd5b8b80
translation-type: ht
source-git-commit: a3aa8feb937e2a1f40c498aa4e143de21cf26b86

---


# 통합 배포{#deploying-the-integration}

3단계 배포 프로세스에 대해 설명합니다.

이 통합 배포는 다음 작업이 필요한 간단한 프로세스입니다.

## 통합 마법사 완료{#completing-the-integration-wizard}

통합 마법사 사용 단계입니다.

통합을 활성화하려면 Data Connectors 인터페이스 내에서 Lyris 통합 마법사를 완료해야 합니다.

1. Adobe Experience Cloud 내에서 Data Connectors(이전 Genesis) 영역으로 이동합니다.

   ![](assets/data_connectors.png)

1. Lyris HQ에서 **[!UICONTROL 통합 추가]** 아래의 **[!UICONTROL 활성화]**&#x200B;를 클릭합니다.

   ![](assets/add_integration.png)

1. **[!UICONTROL 일반 설정]**&#x200B;에서 원하는 보고서 세트를 선택하고 통합 이름을 제공합니다.
1. **[!UICONTROL 사용자 지정 값]** 아래에 Lyris 계정과 관련된 모든 정보를 입력합니다.

   ![](assets/general_settings.png)

1. 드롭다운 메뉴에서 해당하는 예약된 eVar 및 이벤트를 선택합니다.

   ![](assets/variable_mapping.png)

1. 자동화된 3개의 파트너 세그먼트와 별도로 **[!UICONTROL 세그먼트]** 아래에서 고유한 세그먼트를 선택할 수 있습니다.
1. 이 통합을 위해서 Lyris 계정에 몇 개의 데이터 포인트를 다운로드해야 할 수 있습니다. **[!UICONTROL 액세스 요청]**&#x200B;에서 이에 대한 액세스 권한을 부여할 수 있습니다.
1. **[!UICONTROL 데이터 수집]**&#x200B;에서 자동화된 솔루션 또는 수동 솔루션(JavaScript 플러그인)을 선택하여 랜딩 페이지 URL에서 쿼리 문자열 매개 변수를 수집할 수 있습니다. 자동화된 솔루션을 선택한 경우 메시지 ID 및 수신자 ID에 대한 쿼리 문자열 매개 변수를 입력합니다. JavaScript 플러그인은 Adobe 컨설턴트에게 문의하십시오.

   ![](assets/data_collection.png)

1. Lyris 대시보드 및 책갈피를 자동으로 생성하도록 선택할 수 있습니다.

   ![](assets/dashboard_generation.png)

1. 통합 요약을 검토하고 **[!UICONTROL 활성화]**&#x200B;를 클릭합니다.

## Lyris EmailLabs 내의 구성{#configuration-within-the-lyris-emaillabs}

마법사 완료 후 Lyris 내에서 구성할 내용을 설명하는 단계입니다.

1. 통합 마법사를 완료한 후 Lyris Professional 팀과 협력하여 Lyris HQ 계정 통합을 완료하고 테스트를 용이하게 해야 합니다.
1. URL 쿼리 문자열 매개 변수 추가: URL 첨부 문자열이 사용자 인터페이스의 조직 설정 영역에 제대로 입력되었는지 확인합니다. 여기에는 캠페인 수준 ID(hq_m) 및 수신자 수준 ID(hq_v)가 포함되어야 합니다.

   문자열 ID 예시:

   ```
   hq_lid=149&hq_m=96843&hq_l=23&hq_v=7703a51905
   ```

   >[!NOTE]
   >
   >Lyris의 기본 분석 도구를 적용하는 경우 *Click Tracks*&#x200B;는 추가된 모든 필수 변수에 태그를 지정합니다.

## 통합 확인{#verifying-the-integration}

Lyris/Adobe Analytics 통합이 성공했는지 확인하는 단계입니다.

모든 배포 단계가 완료되면 통합이 성공적으로 데이터를 전송하고 있는지 확인할 수 있습니다.

> [!NOTE] 데이터 교환을 시작하려면 며칠이 걸립니다. 통합을 활성화한 후 Lyris에 문의하십시오.

1. Data Connectors 내에서 Lyris 통합으로 이동합니다. **[!UICONTROL 지원]** 탭 > **[!UICONTROL 통합 활동 로그]**&#x200B;에 **[!UICONTROL 지표 데이터를 가져왔습니다]** 및/또는 **[!UICONTROL 분류 데이터를 가져왔습니다]**&#x200B;와 같은 이벤트가 표시되어야 합니다.

   ![](assets/integration_info.png)

1. 이제 해당 지표와 함께 Lyris 메시지 보고서를 봅니다. Adobe Experience Cloud에서 **[!UICONTROL Reports &amp; Analytics]**&#x200B;를 선택합니다.
1. 적절한 보고서 세트를 선택합니다.
1. **[!UICONTROL 사용자 지정 전환]**&#x200B;에서 **[!UICONTROL 메시지 ID 보고서]**&#x200B;를 선택하고 **[!UICONTROL 메시지 ID/메시지 이름]**&#x200B;을 선택합니다.

## 쿼리 문자열 매개 변수 플러그인 코드{#query-string-param-plug-in-code}

Adobe Analytics에서 사용할 Lyris 플러그인 코드를 표시합니다.

> [!NOTE] 아래 코드를 사용하여 작업하기 전에 Adobe Analytics의 관리 도구에서 필요한 eVar를 예약했는지 확인하십시오. 어떤 eVar를 예약했는지 알고 있으면 eVarN을 관련 eVar로 바꿉니다. 예: eVar10.

```
/* 
  * Plugin: getQueryParam 2.3 
  */ 
s.getQueryParam=new Function("p","d","u","" 
+"var s=this,v='',i,t;d=d?d:'';u=u?u:(s.pageURL?s.pageURL:s.wd.locati" 
+"on);if(u=='f')u=s.gtfs().location;while(p){i=p.indexOf(',');i=i<0?p" 
+".length:i;t=s.p_gpv(p.substring(0,i),u+'');if(t){t=t.indexOf('#')>-" 
+"1?t.substring(0,t.indexOf('#')):t;}if(t)v+=v?d+t:t;p=p.substring(i=" 
+"=p.length?i:i+1)}return v"); 
s.p_gpv=new Function("k","u","" 
+"var s=this,v='',i=u.indexOf('?'),q;if(k&&i>-1){q=u.substring(i+1);v" 
+"=s.pt(q,'&','p_gvf',k)}return v"); 
s.p_gvf=new Function("t","k","" 
+"if(t){var s=this,i=t.indexOf('='),p=i<0?t:t.substring(0,i),v=i<0?'T" 
+"rue':t.substring(i+1);if(p.toLowerCase()==k.toLowerCase())return s." 
+"epa(v)}return ''"); 
 
/*in the s_doPlugins function - Replace N with actual eVar number*/ 
s.eVarN=s.getQueryParam("<insert Lyris QS Param>");  
//places query param value from Message ID in eVarN variable s.eVarN=s.getQueryParam("<insert Lyris QS Param>");  
//places query param value from Recepient ID in eVarN variable 
```
