---
description: Analytics 사용자 계정을 Admin Console에 Enterprise ID 또는 Federated ID로 마이그레이션하는 방법입니다.
title: Enterprise 및 Federated ID에 대한 Analytics 사용자 계정 마이그레이션
uuid: f90bf78a-5603-4bef-b714-13215301187c
translation-type: tm+mt
source-git-commit: 3db8481434f3db43732f0b54a58c6d4a29bce652

---


# Enterprise 및 Federated ID에 대한 Analytics 사용자 계정 마이그레이션{#migrate-analytics-user-accounts-for-enterprise-and-federated-ids}

Analytics 사용자 계정을 Admin Console에 Enterprise ID 또는 Federated ID로 마이그레이션하는 방법입니다.

## 전제 조건 {#prereqs}

Admin Console에서 사용자를 관리하기 위한 전제 조건입니다.

새 도메인 및 디렉터리의 경우 다음 단계를 수행하십시오.

* 디렉터리 설정
* 도메인 설정
* 디렉터리에 도메인 연결

도움이 필요한 경우 [ID 시스템 설정](https://helpx.adobe.com/enterprise/using/set-up-identity.html)을 참조하십시오.

다른 사업 부서의 조직이나 팀에서 이미 디렉터리를 생성한 경우 [디렉터리 신뢰](https://helpx.adobe.com/enterprise/using/set-up-identity.html#Directorytrusting)의 단계에 따라 Analytics을 사용하고 있는 조직에 디렉터리를 설정합니다.

## Enterprise 및 Federated ID에 대한 사용자 계정 마이그레이션 {#task-0cfb3e4400fd4ab58e4d9704528b05fa}

이 절차에서는 다음을 수행합니다.

* **[!UICONTROL Analytics]** &gt; **[!UICONTROL Analytics 사용자 및 자산]**&#x200B;에서 사용자 로그인 목록을 다운로드합니다.

* **[!UICONTROL Admin Console]** &gt; **[!UICONTROL 사용자]**&#x200B;에서 현재 사용자 목록을 다운로드합니다.

* 목록을 비교합니다(Admin Console에서 계정 데이터를 겹쳐 쓰지 않도록 중복되는 항목 검색).
* Enterprise ID 또는 Federated ID 사용자가 포함된 완료된 [!DNL .csv](**[!UICONTROL Admin Console]** &gt; **[!UICONTROL 사용자]**)를 Admin Console에 업로드합니다.

기존 Adobe ID 사용자 계정을 Enterprise ID 또는 Federated ID로 마이그레이션해야 하는 경우, Adobe 고객 지원 센터에 문의하여 [대량 사용자 ID 전환](https://helpx.adobe.com/enterprise/using/bulk-operations.html)을 요청하십시오.

**사용자 계정을 마이그레이션하는 방법**

1. 다음 방법 중 하나를 사용하여 Analytics 사용자 관리에서 Analytics 사용자 로그인 파일([!DNL User Logins List.tab])을 다운로드합니다(이미 마이그레이션한 사용자인지 여부에 따라 다름).
   1. *마이그레이션 전에***[!UICONTROL 관리자]** &gt; **[!UICONTROL 사용자 관리(기존)]** &gt; **[!UICONTROL 사용자 편집]**&#x200B;으로 이동한 뒤 **[!UICONTROL 보고서 다운로드]**&#x200B;를 클릭합니다.

      ![](assets/download-report.png)

      보고서 다운로드 링크는 사용자를 마이그레이션하지 않은 고객에게만 표시됩니다.

   1. *사용자를 이미 마이그레이션한 경우* **[!UICONTROL Analytics]** &gt; **[!UICONTROL Analytics 사용자 및 자산]**&#x200B;으로 이동합니다.

      ![단계 정보](assets/admin-analytics-users-assets.png)

   1. [!DNL Users] 페이지에서 사용자를 선택한 뒤 **[!UICONTROL CSV로 내보내기]**&#x200B;를 클릭합니다.

      ![단계 정보](assets/export-csv-migrate.png)

   1. 다운로드한 [!DNL User List.csv] 파일을 Excel로 엽니다.

      다음 단계에 설명된 [!DNL sample.csv] 파일에 *`Email`*, *`First Name`* 및 *`Last Name`* 값을 복사할 수 있도록 준비하십시오.

      > [!IMPORTANT] CSV 파일의 값은 쉼표로 구분해야 합니다.

      > [!TIP] 이 단계에서는 사용자 목록을 정리하여 유효한 이메일 ID가 있는 사용자만 Enterprise 또는 Federated ID 마이그레이션에 포함할 것을 권장합니다.

1. In the [!UICONTROL Admin Console], download a list of Admin Console users:

   1. [!UICONTROL Admin Console] &gt; **[!UICONTROL 사용자]**&#x200B;로 이동한 다음 [사용자 목록을 CSV로 내보내기](https://helpx.adobe.com/enterprise/using/users.html)를 클릭합니다.

      ![](assets/export-csv.png)

   1. 내보낸 [!DNL .csv] 파일의 기존 Admin Console 사용자를(이 예에서 [!DNL sample.csv]) Analytics [!DNL User Logins List.csv] 파일의 사용자와 비교합니다.

      > [!IMPORTANT] 중복 항목을 찾으면 Analytics [!DNL User Logins List.csv] 파일에서 삭제하십시오. 이 단계는 Admin Console에서 Experience Cloud 사용자 권한을 겹쳐 쓰지 못하게 하고 마이그레이션할 계정 목록을 제공하는 데 도움이 됩니다.

1. Admin Console에서 CSV 템플릿 다운로드:
   1. 사용자 탭에서 **[!UICONTROL CSV로 사용자 추가]**&#x200B;를 클릭한 다음 **[!UICONTROL CSV 템플릿 다운로드]**&#x200B;를 클릭합니다.

      ![단계 정보](assets/add-users-csv.png)

   1. **[!UICONTROL 표준 템플릿]**&#x200B;을 선택합니다.

      이 단계에서는 [!DNL sample.csv] 템플릿 파일을 다운로드합니다.

      ![](assets/download-csv-template.png)

1. [!DNL User Logins List.tab]의 *`Email`*, *`First Name`* 및 *`Last Name`* 열 값을 [!DNL sample.csv] 템플릿의 해당 열에 복사합니다.

   **템플릿 파일 예제**

   ![](assets/sample.png)

1. 템플릿([!DNL sample.csv])에서 다음 필수 필드를 완료하십시오. 

<table id="table_1B5EEFDB5BD8436EB760BE5FFAB1CF02"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 필드 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>이메일 </p> </td> 
   <td colname="col2"> <p><span class="filepath">User Logins List.tab</span>에서 복사됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>이름 </p> </td> 
   <td colname="col2"> <p><span class="filepath">User Logins List.tab</span>에서 복사됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>성 </p> </td> 
   <td colname="col2"> <p><span class="filepath">User Logins List.tab</span>에서 복사됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID 유형 </p> </td> 
   <td colname="col2"> <p><span class="term"> Federated ID</span> 또는 <span class="term"> Enterprise ID</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>도메인 </p> </td> 
   <td colname="col2"> <p>도메인이 <span class="term"> 도메인</span> 및 <span class="term"> 이메일</span> 열이  사전 요구 사항</a>에 설정된 도메인과 일치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>국가 코드 </p> </td> 
   <td colname="col2"> </td> 
  </tr> 
 </tbody> 
</table>

[!DNL .csv] 파일의 필드에 대한 자세한 내용은 [CSV 파일 형식](https://helpx.adobe.com/enterprise/using/users.html)을 참조하십시오.

> [!NOTE] 제품 구성 및 [!UICONTROL 관리자 역할과 같은] 다른 [!UICONTROL 열은] 비어 있을 수 있습니다.

1. Admin Console의 사용자 탭에서 **[!UICONTROL CSV로 사용자 추가]**&#x200B;를 클릭하여 템플릿 파일을 업로드합니다(3단계에서 설명).
1. [Analytics 사용자 계정 마이그레이션](/help/admin/user-management2/user-migration/t-migrate-users.md)에 설명된 대로 Analytics에서 마이그레이션 도구를 실행합니다.
1. **[!UICONTROL 마이그레이션]** &gt; **[!UICONTROL Enterprise ID로 마이그레이션]**&#x200B;을 클릭합니다.

   ![단계 정보](assets/migrate-as-enterprise.png)

   **[!UICONTROL 마이그레이션]**&#x200B;을 클릭하면 사용자가 Admin Console의 Enterprise ID/Federated ID 계정에 연결됩니다. Analytics의 기존 사용자 계정 권한은 **[!UICONTROL Admin Console]** &gt; **[!UICONTROL Analytics]** &gt; **[!UICONTROL 제품 프로필]**&#x200B;에서 Enterprise/Federated ID 로그인에 부여된 권한과 일치합니다. 사용자 ID가 마이그레이션 완료 버킷에 표시됩니다. 기존 [!DNL my.omniture.com] 액세스를 비활성화할 수 있습니다.

   After migrating users, the status under the Migration Status column changes from **[!UICONTROL Not Initiated]** to **[!UICONTROL Migrated]**.

   마이그레이션 도구에 표시되는 Adobe ID 사용자는 이 프로세스에서도 마이그레이션할 수 있습니다. ID 전환이 수행될 때까지는 계속 Adobe ID로 로그인해야 합니다. ID 전환에 대한 지원은 Adobe 고객 지원 센터에 문의하십시오.
