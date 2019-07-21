---
description: 데이터 소스 .txt 템플릿에 대한 정보.
seo-description: 데이터 소스 .txt 템플릿에 대한 정보.
seo-title: 가져오기 파일 참조
solution: Analytics
subtopic: Data Sources
title: 가져오기 파일 참조
topic: 개발자 및 구현
uuid: CC 58 F 8 D 8-CB 6 E -4908-846 F -0 A 41 C 6 DA 805 D
translation-type: tm+mt
source-git-commit: cce2c1c54f21244f856385aeaad811d89f2fda7f

---


# 가져오기 파일 참조

데이터 소스 .txt 템플릿에 대한 정보.

데이터 소스 마법사를 사용하여 가져오기 템플릿을 생성하십시오. 데이터 소스 가져오기 파일에는 다음 데이터가 포함됩니다.

* 파운드 기호(#)는 해당 행을 주석으로 식별합니다.
* 필요에 따라 파일에 주석을 추가할 수 있습니다.
* 템플릿 파일 제목을 열거하는 주석을 사용할 수 있습니다.
* [!UICONTROL 데이터 소스 활성화 마법사]에서 지정된 외부 지표와 데이터 차원 이름을 열거하는 주석을 사용할 수 있습니다.

열 머리글은 데이터 소스 파일의 각 열에 있는 데이터를 식별하는 데 사용됩니다. 열 머리글에는 3가지 종류가 있습니다.

**날짜**: (필수) 파일의 각 데이터 행에 대한 타임스탬프.

**변수**: 데이터 소스의 데이터 차원에 매핑되는 보고 변수의 이름.

**이벤트**: 데이터 소스의 지표에 매핑되는 이벤트의 이름.

데이터 소스 템플릿을 사용하여 업로드하려는 데이터를 포함한 데이터 소스 파일을 생성하십시오. 데이터 소스 파일을 만들 때는 다음에 유의하십시오.

* 실제로 데이터 소스 파일의 각 행은 하나의 데이터 레코드를 포함하며 각 레코드는 일련의 탭 구분 필드로 구성됩니다. 데이터 소스 템플릿의 열 헤더는 이러한 필드의 순서를 정의합니다. 예:

   ```
     #Sample data file for mycorp_report_suite 
     #Imported data for ad impressions applied to Event 6
     Date     Tracking Code      Event 6 
     1/1/2009     NYT8453A      8754
     1/1/2009     WSJ4453B      9492
     1/1/2009     BHG44563      10553
     1/2/2009     NYT8453A      6452
     1/2/2009     WSJ4453B      7237
     1/2/2009     BHG44563      9031
   ```

* 여러 데이터 파일을 업로드하는 경우 데이터 소스는 이를 알파벳 순서로 불러옵니다. 시간순으로 처리해야 하는 파일은 이름을 지정할 때 시간 순서와 일치하도록 이름의 알파벳 순서를 나열해야 합니다. 예:

   ```
   log_2009-01-01_13:00.txt
   log_2009-01-01_13:15.txt
   log_2009-01-01_13:30.txt
   ```

* 데이터 소스 파일의 처리 속도를 높이려면 이벤트(지표) 데이터를 날짜별 단일 행으로 집계하는 것이 좋습니다.

   예를 들어 데이터 소스 파일이 광고 노출 데이터를 이벤트 6에 매핑하는 경우 특정일에 발생한 각 광고 노출에 대해 별도의 데이터 행 항목을 만드는 대신 각 날짜에 대해 총 광고 노출 수를 포함하는 단일 데이터 행을 만드십시오.
* 보고서 세트 생성 날짜 이전의 데이터를 업로드해야 하는 경우 계정 관리자에게 문의하여 보고서를 실행할 수 있는 가장 오래된 날짜를 변경하십시오.

**.FIN 파일**

데이터 소스 파일 작성을 마쳤으면 FTP를 Analytics로 전송할 수 있습니다. 하지만 데이터를 처리하려면 추가 파일이 필요합니다. You will need to upload an empty text file with the same name of your data file, but with a [!DNL .fin] extension.

For example, if you upload a (tab-delimited) data file called [!DNL myproductdata.txt], you would also need to upload an empty text file called [!DNL myproductdata.fin]. [!DNL .fin] 파일이 없으면 데이터가 처리되지 않습니다.
