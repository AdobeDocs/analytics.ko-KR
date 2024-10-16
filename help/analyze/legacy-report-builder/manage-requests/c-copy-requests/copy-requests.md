---
description: 두 개 이상의 요청으로 매핑된 셀을 복사하고 붙여넣는 방법을 알아봅니다.
title: 요청 복사 방법 개요
uuid: 1e0274a3-2038-45c7-87c8-bd949538d4e1
feature: Report Builder
role: User, Admin
exl-id: 14578c79-a9e6-4587-b91b-f590453df347
source-git-commit: bb908f8dd21f7f11d93eb2e3cc843f107b99950d
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 87%

---

# 요청 복사 개요

두 개 이상의 요청과 매핑된 셀을 복사하고 그 내용을 스프레드시트의 비어 있는 선택된 영역에 붙여넣을 수 있습니다.

셀을 복사하면 Report Builder와 Excel은 최소한의 사본을 붙여넣는 데 필요한 영역을 판단합니다. 영역이 충분히 크면 붙여넣기 작업에 의해 모든 요청의 사본이 만들어지고 이 때 각각의 붙여넣기가 수행된 요청은 원래의 요청과 동일한 공간 배치 및 서식을 갖게 됩니다.

이러한 과정을 요청을 전파한다라고 하며, 긴 보고서를 만드는 쉽고 빠른 방법입니다. Report Builder는 먼저 대상 붙여넣기 영역에 셀에 있는 모든 요청을 붙여넣어 요청을 전파한 다음, 해당 요청들에 대해 설정된 보고서 날짜를 기반으로 셀을 새로 고칩니다.
