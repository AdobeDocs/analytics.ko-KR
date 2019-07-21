---
description: 이 섹션은 데이터 피드 배달에서 발견되는 파일을 설명합니다.
keywords: 데이터 피드; 작업; 컨텐츠; manifest; 파일; 조회; 히트 데이터; 배달 컨텐츠
seo-description: 이 섹션은 데이터 피드 배달에서 발견되는 파일을 설명합니다.
seo-title: 데이터 피드 컨텐츠 - 개요
solution: Analytics
subtopic: 데이터 피드
title: 데이터 피드 컨텐츠 - 개요
topic: Reports & Analytics
uuid: 82 A 86314-4841-4133-A 0 DC -4 E 7 CD 14 FC 1
translation-type: tm+mt
source-git-commit: 7fe23291d8ee9675181065025692108aee3ea9a5

---


# 데이터 피드 컨텐츠 - 개요

이 섹션은 데이터 피드 배달에서 발견되는 파일을 설명합니다.

## 매니페스트 파일 {#section_044BBDE2906D49518F8264CD4832D429}

매니페스트 파일에는 업로드된 데이터 세트의 일부인 각 파일에 대한 다음 정보가 있습니다.

* 파일 이름
* 파일 크기
* MD5 해시
* 파일에 포함된 레코드 수

매니페스트 파일은 Java JAR 매니페스트 파일과 같은 형식을 따릅니다.

The manifest file is always delivered last as a separate `.txt` file, so that its existence indicates that the complete data set for that request period has already been delivered. 매니페스트 파일은 다음에 따라 명명됩니다.

```
<report_suite_id>_YYYY_MM_DD.txt
```

일반적인 매니페스트 파일에는 다음과 비슷한 데이터가 포함됩니다.

```
Datafeed-Manifest-Version: 1.0
 Lookup-Files: 1
 Data-Files: 1
 Total-Records: 611

 Lookup-File: bugzilla_2012-09-09-lookup_data.tar.gz
 MD5-Digest: af6de42d8b945d4ec1cf28360085308
 File-Size: 63750

 Data-File: 01-bugzilla_2012-09-09.tsv.gz
 MD5-Digest: 9c70bf783cb3d0095a4836904b72c991
 File-Size: 122534
 Record-Count: 611
```

모든 매니페스트 파일에는 조회 파일, 데이터 파일의 총 수, 모든 데이터 파일의 총 레코드 수를 나타내는 헤더가 있습니다. 이 헤더 뒤에는 데이터 피드 배달에 포함된 각 파일에 대한 정보를 포함하는 여러 개의 섹션이 옵니다.

Some feeds are configured to receive a `rsid_YYYY-MM-DD.fin` file instead of a `.txt` manifest. The `.fin` indicates that the upload is complete, but it contains no metadata about the upload.

## 조회 파일 {#section_B5863537A48D47D78D0F7274838923C1}

조회 파일에는 히트 데이터가 없습니다. 조회 파일은 히트 데이터, 조회 파일에 대한 열 헤더를 제공하여 데이터 피드에서 발견되는 ID를 실제 값으로 변환하기 위한 보조 파일입니다. 예를 들어 브라우저 열의 "497"이라는 값은 히트가 "Microsoft Internet Explorer 8"에서 왔음을 나타냅니다.

`column_headers.tsv` AND `event_list.tsv` 는 데이터 피드 및 보고서 세트에 따라 다릅니다. `browser.tsv`와 같은 다른 파일은 일반적입니다.

조회 파일은 다음에 따라 명명된 zip 압축 파일로 배달됩니다.

```
<report_suite_id>_<YYYY-mm-dd>-<HHMMSS>-lookup_data.<compression_suffix>
```

* [!DNL column_headers.tsv] ((이 데이터 피드에 대해 사용자 정의됨)
* [!DNL browser.tsv]
* [!DNL browser_type.tsv]
* [!DNL color_depth.tsv]
* [!DNL connection_type.tsv]
* [!DNL country.tsv]
* [!DNL javascript_version.tsv]
* [!DNL languages.tsv]
* [!DNL operating_systems.tsv]
* [!DNL plugins.tsv]
* [!DNL resolution.tsv]
* [!DNL referrer_type.tsv]
* [!DNL search_engines.tsv]
* [!DNL event_lookup.tsv] ((이 데이터 피드에 대해 사용자 정의됨)

## 히트 데이터 파일 {#section_B0745236104E41F2BA625D24AB442636}

Hit data is provided in a [!DNL hit_data.tsv] file. 이 파일의 데이터 양은 배달 형식(시간별 또는 일별, 단일 파일 또는 여러 파일)에 따라 결정됩니다. 이 파일은 히트 데이터만 포함합니다. 열 헤더는 조회 파일과 별도로 배달됩니다. 이 파일의 각 행은 하나의 서버 호출을 포함합니다.

## 배달 컨텐츠 {#section_994B43D1E71A4EFDB2E4183C0929A397}

>[!NOTE]
>
>파일은 ISO -8859-1를 사용하여 인코딩됩니다.

Adobe가 배달하는 실제 파일은 사용자가 구성한 데이터 피드 유형에 따라 달라집니다. 배달되는 파일을 설명하는 다음 테이블에서 데이터 피드에 맞는 구성을 찾으십시오.

파일 이름에 표시된 시간(HHMMSS)은 파일 생산 또는 업로드 시기에 관계 없이 파일 내 데이터에 대한 날짜 범위의 시작을 가리킵니다.

<table id="table_DBF34F39D29D4DA2B2689029CDA24B92"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 배달 형식 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 일별, 단일 파일 </td> 
   <td colname="col2"> <p>하루 동안 데이터가 수집된 후 다음을 포함한 배달을 받게 됩니다. </p> 
    <ul id="ul_D630D73D0DBA440FA704CF31856243C7"> 
     <li id="li_717873DBBF264422A39217E1A8829742">단일 압축 데이터 파일 </li> 
     <li id="li_9F75D42FD56E4CC89C4683D32E59337B">매니페스트 파일 </li> 
    </ul> <p>데이터 파일은 다음 이름으로 배달됩니다. </p> 
    <code>&lt; report_ suite &gt;_ &lt; yyyy-mm-dd &gt;.&lt;compression_suffix&gt;
    </code> <p> <code>&lt;compression_suffix&gt;</code>은(는) <code>tar.gz</code> 또는 <code>zip</code>입니다. </p> <p>데이터 파일의 압축을 해제하면 하루 동안의 모든 데이터를 포함한 단일 <span class="filepath">hit_data.tsv</span> 파일과 위에 설명한 압축된 조회 파일이 들어 있습니다. </p> <p>히트 데이터 파일 크기는 능동적으로 사용되는 변수의 수와 보고서 세트의 트래픽 양에 따라 크게 달라집니다. 하지만 평균적으로 데이터 행은 500B(압축) 또는 2KB(비압축)입니다. 여기에 서버 호출 횟수를 곱하면 데이터 피드의 크기를 대략적으로 예상할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 일별, 여러 파일 </td> 
   <td colname="col2"> <p>하루 동안 데이터가 수집된 후 다음을 포함한 배달을 받게 됩니다. </p> 
    <ul id="ul_4B873D3F6F18467890C36AE8E86F49DA"> 
     <li id="li_227315384B954A5784FA370D9B30E2AF">2GB 단위로 나누어진 하나 이상의 압축 데이터 파일 </li> 
     <li id="li_4169D889CEA3446CB5FAA08FD60AA0D0">매니페스트 파일 </li> 
    </ul> <p>각 데이터 파일은 다음 이름으로 배달됩니다. </p> 
    <code>&lt; index &gt;-&lt; report_ suite &gt;_ &lt; yyyy-mm-dd &gt;.&lt;compression_suffix&gt;
    </code> <p> <code>&lt;index&gt;</code>은(는) <i>1</i>부터 <i>n</i>까지의 증분 파일 색인이고 파일이 <i>n</i>개이며 <code>&lt;compression_suffix&gt;</code>은(는) <code>tar.gz</code> 또는 <code>zip</code>입니다. </p> <p>각 데이터 파일의 압축을 해제하면 약 2GB의 압축되지 않은 데이터를 포함한 단일 <span class="filepath">hit_data.tsv</span> 파일과 위에 설명한 압축 조회 파일이 들어 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간별, 단일 파일 </td> 
   <td colname="col2"> <p>한 시간 동안 데이터가 수집된 후 다음을 포함한 배달을 받게 됩니다. </p> 
    <ul id="ul_29B06981A4F74D2AA1171D733C5FB1F4"> 
     <li id="li_072BBC4BA9B84C61B4E8EFA35F54707B">단일 데이터 파일 </li> 
     <li id="li_E2D05E9DAE814309B6BC91798BB29FBB">매니페스트 파일 </li> 
    </ul> <p>데이터 파일은 다음 이름으로 배달됩니다. </p> 
    <code>&lt; report_ suite &gt;_ &lt; yyyy-mm-dd &gt;-&lt; hhmmss &gt;.&lt;compression_suffix&gt;
    </code> <p> <code>&lt;compression_suffix&gt;</code>은(는) <code>tar.gz</code> 또는 <code>zip</code>입니다. </p> <p>데이터 파일 압축을 해제하면 해당 시간에 대한 모든 데이터를 포함한 단일 <span class="filepath">hit_data.tsv</span> 파일이 있습니다. 위에 설명한 압축된 조회 파일은 매일 첫 시간에 대한 데이터만 포함하여 배달됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 시간별, 여러 파일 </td> 
   <td colname="col2"> <p>한 시간 동안 데이터가 수집된 후 다음을 포함한 배달을 받게 됩니다. </p> 
    <ul id="ul_A739BA12B66547A28BA45E0B9B747B16"> 
     <li id="li_C0DF059D1E6843C8A38E24CA1B59D99C">2GB 단위로 나누어진 하나 이상의 압축 데이터 파일 </li> 
     <li id="li_604266DA9B8A4000905C44C95DA65D14">매니페스트 파일 </li> 
    </ul> <p>각 데이터 파일은 다음 이름으로 배달됩니다. </p> 
    <code>&lt; index &gt;-&lt; report_ suite &gt;_ &lt; yyyy-mm-dd &gt;-&lt; hhmmss &gt;. tsv.&lt;compression_suffix&gt;
    </code> <p><code>&lt;index&gt;</code>은(는) <i>1</i>부터 <i>n</i>까지의 증분 파일 색인이고 파일이 <i>n</i>개이며 <code>&lt;compression_suffix&gt;</code>은(는) <code>gz</code> 또는 <code>zip</code>입니다. </p> <p>각 데이터 파일의 압축을 해제하면 약 2GB의 압축되지 않은 데이터를 포함하는 단일 <span class="filepath">hit_data.tsv</span> 파일이 들어 있습니다. 위에 설명한 압축된 조회 파일은 매일 첫 시간에 대한 데이터만 포함하여 배달됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

