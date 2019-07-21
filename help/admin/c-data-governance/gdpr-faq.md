---
description: 'null'
seo-description: 'null'
seo-title: FAQ
title: FAQ
uuid: 1 CD 41253-D 74 F -4 B 92-92 E 6-56 F 9 AFA 3 DF 85
translation-type: tm+mt
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# FAQ

<table id="table_FA37A4B3960C4181B9CCDB569A476936"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 질문 </th> 
   <th colname="col2" class="entry"> 답변 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Adobe Analytics는 고객 (데이터 관리자) 에 의해 확인된 최종 사용자 (데이터 주체) 에 대한 요청을 액세스하고 삭제하는 방법은 무엇입니까?</b> </p> </td> 
   <td colname="col2"> <p>GDPR이 발효되면 Adobe Analytics에서는 보다 자동화된 절차를 사용할 수 있도록 데이터 제어자가 Experience Cloud GDPR API에 제출한 확인된 요청 처리를 지원합니다. Adobe의 GDPR API는 Adobe Experience Cloud 솔루션에 저장된 고객의 데이터에 대해 개별적인 권한 요청(예: 액세스 및 삭제 요청)을 처리하는 데 도움을 주도록 설계되었습니다. 이 API는 귀사가 데이터 주체로부터 받는 데이터 액세스 및 삭제 요청 수에 따라 유연하게 확장됩니다. 또한 고객이 GDPR API를 사용하여 데이터 액세스 및 삭제 요청이 어떻게 이행되는지에 대한 상태를 확인할 수 있습니다. </p> <p>자세한 내용은 <a href="https://www.adobe.io/apis/cloudplatform/gdpr.html" format="html" scope="external">GDPR API 설명서</a>를 참조하십시오 . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>최종 사용자의 GDPR 요청 접수, 접수 및 이행을 담당하는 담당자는 누구입니까?</b> </p> </td> 
   <td colname="col2"> <p>데이터 제어자(즉, Adobe 고객)는 GDPR에 따른 개별 권한 요청에 대한 응답으로 개인 데이터를 데이터 주체에 제공할 유일한 책임이 있습니다. 또한 데이터 관리자는 요청을 받고 요청을 수락하는 유일한 책임을 집니다. 이 책임은 데이터 주체의 신원을 검증한 다음 요청을 이행하며, Adobe Analytics에 저장된 데이터와 연관될 수 있는 데이터 주체의 ID와 Adobe에 연락을 취할 수 있습니다. Adobe는 데이터 처리자로서, 허용된 시간 내에 확인된 요청을 처리할 수 있도록 제어자에게 적합한 지원을 제공해야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Adobe 고객(데이터 제어자)은 GDPR 처리를 위해 Adobe Analytics에서 어느 GDPR 요청이 어느 ID에 매핑되는지 어떻게 알 수 있습니까?</b> </p> </td> 
   <td colname="col2"> <p>데이터 제어자는 데이터 주체의 요청에 대한 ID를 확인하는 방법을 결정합니다. Consider deploying <a href="https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.htm" format="html" scope="external"> Adobe's GDPR ID Retrieval Tag </a>. 개발 팀에서는 GDPR ID 검색 태그를 사용하여 사용자 ID(쿠키 ID)를 캡처한 다음 GDPR API를 사용하여 GDPR 요청 처리를 위해 Adobe Experience Cloud의 관련 솔루션으로 해당 사용자 ID를 전송합니다. </p> <p>GDPR API는 여러 Adobe 솔루션에서 광범위한 고객 ID를 지원할 수 있습니다. 데이터 주체가 식별자 (사용자 지정 변수 - prop 또는 evar) 와 함께 요청을 제출하는 경우, Adobe Analytics는 해당 식별자에 대해 수집된 데이터의 전체 유지 내역을 스캔합니다. Analytics prop 또는 evar에 저장된 사용자 지정 ID를 구성하는 방법에 대한 자세한 내용은 [네임스페이스] 에 있는 분석 설명서를 참조하십시오 (/help/admin/c-data-governance/gdpr-namespace. md).
    </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Adobe Analytics 데이터 거버넌스에서는 GDPR 요청 처리를 어떻게 지원할 수 있습니까?</b> </p> </td> 
   <td colname="col2"> <p>데이터 거버넌스는 Adobe Analytics 내의 새로운 도구로 데이터 제어자는 이 도구를 사용하여 해당 Analytics 데이터에 데이터 제어 및 분류를 적용할 수 있습니다. 이 새 도구를 통해 Adobe 고객은 GDPR 데이터 액세스 및 데이터 삭제 요청 처리를 사용자 지정할 수 있습니다. 데이터 거버넌스 콘솔에서 관리자는 Adobe Analytics에 있는 다양한 데이터 열에 적용해야 하는 설정을 원하는 대로 정의할 수 있습니다. 이러한 레이블이 정의되면 Adobe는 고객이 원하는 레이블 설정에 따라 다운스트림 액세스 또는 삭제 요청을 처리합니다.  법정 대리인과 이러한 레이블 설정에 대해 검토하고 논의하는 것은 데이터 제어자의 책임입니다. Adobe Analytics에서는 GDPR API를 이용하여 요청 완료를 사용자 지정할 수 있도록 클라이언트가 GDPR 발효일(2018년 5월 25일) 전에 데이터 레이블 지정을 올바르게 설정할 것을 권장합니다. </p> <p>데이터 거버넌스 도구에는 다음 데이터 레이블이 포함되어 있습니다. </p> 
    <ul id="ul_F25B00EB020B4A639628FB884D0CB4F9"> 
     <li id="li_C295A396685340369D730D696FE6FC13"> <a href="../../admin/c-data-governance/gdpr-labels.md#section_D7F4E4B60D6D40BEBC86B7004EF42AFF" format="dita" scope="local"> ID 데이터 레이블</a>: 개인을 직접 식별하거나 다른 데이터와 조합하여 식별할 수 있는 데이터를 분류하는 데 사용됩니다. (없음, I1, I2) </li> 
     <li id="li_6D9A25139D3342CA82AAA64BC01AD368"> <a href="../../admin/c-data-governance/gdpr-labels.md#section_533E1406F3F24A01B51D94139B94CAEC" format="dita" scope="local"> 중요 데이터 레이블</a>: 데이터를 해당 법에 따라 '중요'로 정의할 수 있는 데이터로 분류하는 데 사용됩니다. (없음, S1, S2) 현재 Adobe Analytics의 중요 데이터 사용은 적용 가능한 법률에 따라 타당하게 얻은 정확한 지리적 위치 데이터(일부 관할권에서 중요 데이터로 간주될 수 있음)를 제외하고 일반적으로 금지되어 있습니다. </li> 
     <li id="li_C69935AAC36741D8A902D14F75E896D6"> <a href="../../admin/c-data-governance/gdpr-labels.md#section_0C7F9EC4BB414A6D915C69F1D3259F1B" format="dita" scope="local">GDPR 데이터 레이블</a>: GDPR 요청에 사용할 개인 식별자가 포함될 수 있거나 GDPR 삭제 요청의 일부로 제거해야 하는 필드를 정의하는 데 사용됩니다. 이러한 레이블은 경우에 따라 ID 및 중요 데이터 레이블과 겹칠 수 있습니다. </li> 
    </ul> <p>데이터 거버넌스 레이블에 대한 자세한 내용은 <a href="../../admin/c-data-governance/gdpr-labels.md#concept_F4061E29353446B5B0A7CF248D54E6F2" format="dita" scope="local">Analytics 변수에 대한 GDPR 레이블</a>을 참조하십시오 . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Adobe Analytics에서 GDPR을 준비하려면 어디서 시작해야 합니까?</b> </p> </td> 
   <td colname="col2"> <p>GDPR 준비 과정에 대한 단계별 설명은 <a href="../../admin/c-data-governance/an-gdpr-workflow.md#concept_1D1C0C1EAC3B4772AEDF5CC9F0EA604B" format="dita" scope="local">Adobe Analytics GDPR 워크플로우</a>를 참조하십시오 . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>데이터 제어자는 사용자 참여와 관련하여 동의를 어떻게 생각해야 합니까?</b> </p> </td> 
   <td colname="col2"> <p>GDPR은 동의가 필요한 시기 결정 및 사용자에 대한 가치 제안 고려를 비롯하여 사용자의 동의 관리 전략 및 관행을 재고할 수 있는 좋은 기회입니다. 소비자 개인 정보에 대한 가치 제안을 고려하십시오. 이는 전환 및 충성도를 유도하는 데 도움이 될 수 있습니다. </p> <p>동의 관리 공간(예: 도구, 표준, 우수 사례)은 빠르게 발전하고 있으며 이는 계속해서 지켜봐야 할 영역입니다. 사용자 참여에 미치는 영향을 최소화하려면 제어자가 이 공간의 공급업체 및 해당 자문 기관과 협력하고, 동의 및 쿠키에 대한 새로운 EU 법률과 지침을 따라야 합니다. 데이터 수집 활동에 대한 가치 제안을 설정하는 브랜드에 대한 상황별 관련 경험을 이용하여 "경험적 개인 정보"를 고려하는 것은 훌륭한 전략입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>데이터 제어자는 GDPR과 관련하여 데이터 보존에 대해 어떻게 생각해야 합니까?</b> </p> </td> 
   <td colname="col2"> <p>GDPR은 일반적으로 개인 데이터가 수집된 목적을 달성하는 데 필요한 기간보다 오래 해당 데이터를 보존하지 않도록 합니다. </p> <p>2월에 고객 커뮤니케이션에서 자세히 설명했듯이 Adobe는 다른 합의를 하지 않는 한 대부분의 고객에게 25개월의 데이터 보존 계획을 적용합니다(고객 알림 및 승인을 따름). Adobe에서 GDPR 요청을 처리할 수 있으려면 먼저 고객이 데이터 보존 정책을 설정해야 합니다. </p> <p>Adobe Analytics에서는 고객이 데이터 보존 정책을 설정하여 GDPR 요청을 처리하도록 합니다. 각 보고서 세트의 현재 데이터 보존 정책이 새 데이터 거버넌스 관리 UI에 표시됩니다. 고객은 데이터 보존 정책을 조정해야 하는 경우 Adobe 담당자에게 문의해야 합니다. <a href="https://marketing.adobe.com/resources/help/en_US/reference/data-retention-client-table-faq.html" format="html" scope="external">Adobe Analytics 데이터 보존 FAQ</a>를 참조하십시오 . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>고객이 기본 데이터 보존 기간을 줄이거나 연장할 수 있습니까?</b> </p> </td> 
   <td colname="col2"> <p>고객은 고객 지원에 전화를 걸어 25개월 이내에 해당 데이터를 삭제하도록 요청할 수 있습니다. 고객은 익스텐션을 구매하여 25 개월 이상의 데이터 유지 기간을 연장할 수 있습니다.</p><p>
   익스텐션은 1 년 추가 1 년 (최대 8 년) 최대 8 년 (총 10 년) 씩 제공됩니다. 이 확장 프로그램을 이용하기 위해서는 계약 조건을 업데이트해야 하며, 추가 비용이 들 수 있습니다.
 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Adobe Analytics에서 개인 데이터를 내보낼 때 데이터 제어자가 고려해야 하는 개인 정보 고려사항은 무엇입니까?</b> </p> </td> 
   <td colname="col2"> <p>고객이 Adobe Analytics 데이터 피드를 사용하여 Analytics에서 해당 엔터프라이즈 데이터 웨어하우스나 Adobe 외부의 다른 시스템으로 데이터를 내보내는 경우 데이터에 삭제 요청이 적용되는지 확인하는 것은 고객(데이터 제어자)의 책임입니다. 이는 진행 중인 Adobe Analytics 데이터 피드가 Data Workbench 데이터를 채우는 Adobe Data Workbench(Insight)의 온-프레미스 구현에도 적용됩니다. Adobe는 Data Workbench에 사용된 데이터 피드를 비롯하여 특정 유형의 데이터 피드에서 레코드를 찾아서 삭제하는 데 도움이 되는 도구를 제공할 수 있지만, 데이터가 고유한 내부 데이터 보존 및 삭제 정책에 따라 삭제되는지 확인하는 것은 여전히 고객(데이터 제어자)의 책임입니다. </p> <p>직원이 개인 데이터가 포함된 Adobe Analytics 보고서를 다운로드했을 수 있는 경우도 고려하십시오. 이러한 보고서는 보고서에 있을 수 있는 ID를 포함하여 GDPR 또는 기타 개인 정보 관련 삭제 요청을 받으면 업데이트하거나 삭제해야 할 수 있습니다. 고객은 회사의 법률 담당 변호사와 함께 이러한 유형의 문서에 적용해야 하는 보존 기간, 개인 정보 및 보안 요구 사항을 결정해야 합니다. </p> </td> 
  </tr> <tr> 
   <td colname="col1"> <p><b> 수집하면 안 되는 일부 데이터가 실수로 Adobe Analytics에 전송되었습니다. Can we use the GDPR API to cleanup this data?</b> </p> </td><td colname="col2"> <p>GDPR API를 통해 시간 민감도인 GDPR 요청을 처리할 수 있습니다. 이 API를 다른 용도로 사용하는 것은 Adobe에서 지원하지 않으며, Adobe가 다른 Adobe 고객을 위해 우선순위가 높은 사용자 주도 GDPR 요청을 시기적절하게 제공하는 기능에 영향을 줄 수 있습니다. 많은 방문자 그룹에 실수로 제출된 데이터 지우기와 같은 다른 용도로는 GDPR API를 사용하지 말아 주십시오.</p> <p>또한 GDPR 삭제 요청으로 인해 히트가 삭제(업데이트 또는 익명 처리)된 방문자의 상태 정보는 재설정된다는 사실을 알고 있어야 합니다. 따라서 다음번에 방문자가 사용자의 웹 사이트로 돌아가면 새 방문자로 간주됩니다. 방문 수, 레퍼러, 방문한 첫 번째 페이지 등의 정보와 마찬가지로 모든 eVar 속성이 다시 시작됩니다. 이 부작용은 데이터 필드를 지우려는 경우 바람직하지 않으며, GDPR API가 이 사용에 대해 부적절한 이유 중 하나를 강조 표시합니다. </p> <p>계정 관리자 (CSM) 에게 문의하여 엔지니어링 설계자 컨설팅 팀과 협력하여 PII 또는 데이터 문제를 제거하는 데 더 많은 노력을 기울이고 제공할 수 있습니다.</p></td></tr> <tr> 
   <td colname="col1"> <p><b> 법무팀에서는 수년 동안 변수에서 수집한 내용이 더 이상 업데이트된 개인정보 보호정책을 준수하지 않는다고 결정했습니다. GDPR API를 사용하여 이 변수에서 수집한 모든 값을 지울 수 있습니까?</b> </p> </td><td colname="col2"> <p>GDPR API를 통해 시간 민감도인 GDPR 요청을 처리할 수 있습니다. 이 API를 다른 용도로 사용하는 것은 Adobe에서 지원하지 않으며, Adobe가 다른 Adobe 고객을 위해 우선순위가 높은 사용자 주도 GDPR 요청을 시기적절하게 제공하는 기능에 영향을 줄 수 있습니다. 많은 방문자 그룹에 실수로 제출된 데이터 지우기와 같은 다른 용도로는 GDPR API를 사용하지 말아 주십시오.</p> <p>또한 GDPR 삭제 요청으로 인해 히트가 삭제(업데이트 또는 익명 처리)된 방문자의 상태 정보는 재설정된다는 사실을 알고 있어야 합니다. 따라서 다음번에 방문자가 사용자의 웹 사이트로 돌아가면 새 방문자로 간주됩니다. 방문 수, 레퍼러, 방문한 첫 번째 페이지 등의 정보와 마찬가지로 모든 eVar 속성이 다시 시작됩니다. 이 부작용은 데이터 필드를 지우려는 경우 바람직하지 않으며, GDPR API가 이 사용에 대해 부적절한 이유 중 하나를 강조 표시합니다. </p> <p>계정 관리자 (CSM) 에게 문의하여 엔지니어링 설계자 컨설팅 팀과 협력하여 PII 또는 데이터 문제를 제거하는 데 더 많은 노력을 기울이고 제공할 수 있습니다.</p></td>
 </tbody> 
</table>

추가 GDPR 리소스:

* [GDPR 공통 약관](https://landing.adobe.com/dam/uploads/2018/in/adobe_gdpr_commonterms.pdf)
* Experience Cloud GDPR [Care 패키지](https://landing.adobe.com/dam/uploads/2018/in/adobe_gdpr_carepackage.pdf)
* 경험적 개인 정보[ 블로그 게시물](https://theblog.adobe.com/experiential-privacy-an-investment-opportunity-for-the-experience-business/)
