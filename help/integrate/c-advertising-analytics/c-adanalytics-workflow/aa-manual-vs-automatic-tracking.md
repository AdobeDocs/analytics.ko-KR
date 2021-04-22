---
description: 추적은 Adobe Analytics 구현에 따라 검색 엔진 데이터를 추적하는 방법을 결정합니다. 이 단계는 검색 엔진 데이터를 사용하여 Adobe Analytics 데이터를 적절하게 늘리는 데 필요한 단계입니다.
title: 추적 수동 모드 및 자동 모드
exl-id: 3e2ed26f-dfb2-43ea-8eb6-e332cd10fb29
translation-type: ht
source-git-commit: 549258b0168733c7b0e28cb8b9125e68dffd5df7
workflow-type: ht
source-wordcount: '594'
ht-degree: 100%

---

# 추적: 수동 모드 및 자동 모드

추적은 Adobe Analytics 구현에 따라 검색 엔진 데이터를 추적하는 방법을 결정합니다. 이 단계는 검색 엔진 데이터를 사용하여 Adobe Analytics 데이터를 적절하게 늘리는 데 필요한 단계입니다.

두 가지 추적 모드자동 모드 및 수동 모드가 지원됩니다.

## 자동 모드 추적 {#concept_C4C6107838C947CFBB7F4E0CB94264F0}

[자동 모드]에서 Advertising Cloud 엔진이 검색 엔진 데이터를 처리하는 방법을 결정합니다. 보다 간편한 방법이지만 최상의 통합 데이터 세트를 생성할 수는 없습니다.

따라서 [자동 모드]를 선택할 때 먼저 계정 설정을 저장하기 전에 확인란을 선택해야 합니다.

자동 모드에서 검색 엔진 계정을 구성하려면 다음 조치를 수행해야 합니다.

* `s_kwcid` 매개 변수 및 값이 추가되는 계정의 계정 추적 템플릿 또는 랜딩 페이지 URL에 추가됩니다. URL의 끝에 삽입됩니다. 웹 서버에서 URL 끝에 특정 키=값 쌍이 필요하거나 URL에 새 키=값 쌍을 지원하는 업데이트가 필요한 경우 추가 작업이 필요할 수도 있습니다. **추가된 URL 매개 변수가 최종 랜딩 페이지에 올바르게 유지되는지는 사용자가 확인해야 합니다.**
* 또한 `s_kwcid` 값의 일부로 랜딩 URL에 키워드를 삽입할 수 있습니다. 특수 문자 또는 기호를 포함하는 경우 웹 서버에서 이러한 문자를 지원할 수 있는지 확인하십시오. 일반적인 특수 문자의 예는 &quot;Broad Match Modified&quot; 키워드에서 사용되는 &quot;+&quot;입니다.

>[!IMPORTANT]
>
>`s_kwcid` 매개 변수를 [CSP (콘텐츠 보안 정책)](https://docs.adobe.com/content/help/ko-KR/id-service/using/reference/csp.html)에 추가해야 하는지에 대해 자세히 알아보십시오.

## 수동 모드 추적 {#concept_87B28BA9E7F84BA5972F69E6F3482A33}

수동 모드에서는 Advertising Analytics 데이터 통합 프로세스에서 검색 엔진 데이터를 처리하는 방법을 지정해야 합니다.

### Google 계정에 수동 추적 추가 {#section_41C1EB1AEB034544A5BC291F53C05C67}

Google 계정에 추가해야 하는 문자열이 아래에 표시되어 있습니다. 계정 전체에 사용된 모든 추적 템플릿에 이 문자열을 추가해야 합니다.

>[!IMPORTANT]
>
>`<Advertising Analytics ID>` 값 (아래에 **굵게** 표시됨)은 제네릭이므로, **특정 계정 ID 문자열로 대체해야** 합니다. 계정 설정 화면의 &quot;추적&quot; 섹션 아래에서 특정 계정 ID 문자열을 가져올 수 있습니다.

**캠페인에 대한 추적 문자열:**

```
s_kwcid=AL! 
<b><Advertising Analytics ID></b>!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

![](assets/Google.png)

다양한 추적 템플릿 형식의 추적 코드 예제:

**`{lpurl}`**

```
{lpurl}?s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!network}!{product_partition_id}!{keyword}
```

**`{lpurl}`추가 URL 매개 변수 사용**

```
{lpurl}?campaign=PPC&s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!network}!{product_partition_id}!{keyword}
```

**타사 (DoubleClick)`{unescapedlpurl}`**

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={unescapedlpurl}?s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

**타사 (DoubleClick)`{lpurl}`**

URL이 리디렉션을 통과하고 &quot;unescapedlpurl&quot; 값을 사용하지 않는 경우, 최종 랜딩 페이지 URL로 리디렉션을 통해 지속하도록 문자열을 인코딩해야 합니다.

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={lpurl}?s_kwcid%3DAL!9999!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

### Bing 계정에 수동 추적 추가 {#section_094F8ACA493C4D65B1F54A695558EBF2}

Bing 계정에 추가해야 하는 문자열이 아래에 표시되어 있습니다. 계정 전체에 사용된 모든 최종 URL 접미사에 이 문자열을 추가해야 합니다.

>[!IMPORTANT]
>
>`<Advertising Analytics ID>` 값 (아래에 **굵게** 표시됨)은 제네릭이므로, **특정 계정 ID 문자열로 대체해야** 합니다. 계정 설정 화면의 &quot;추적&quot; 섹션 아래에서 특정 계정 ID 문자열을 가져올 수 있습니다.

**캠페인에 대한 추적 문자열:**

```
s_kwcid=AL!<Advertising Analytics ID>!10!{AdId}!{OrderItemId} 
```

![](assets/Bing.png)

다양한 최종 URL 접미사 형식의 추적 코드 예제:

**{lpurl}**

```
{lpurl}?s_kwcid=AL!9999!10!{AdId}!{OrderItemId}
```

**`{lpurl}`추가 URL 매개 변수 사용**

```
{lpurl}?campaign=PPC&
s_kwcid=AL!9999!10!{AdId}!{OrderItemId}
```

**타사 (DoubleClick)`{unescapedlpurl}`**

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={unescapedlpurl}?s_kwcid=AL!9999!10!{AdId}!{OrderItemId}
```

**타사 (DoubleClick)`{lpurl}`**

URL이 리디렉션을 통과하고 &quot;unescapedlpurl&quot; 값을 사용하지 않는 경우, 최종 랜딩 페이지 URL로 리디렉션을 통해 지속하도록 문자열을 인코딩해야 합니다.

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={lpurl}?s_kwcid%3DAL!9999!10!{AdId}!{OrderItemId}
```
