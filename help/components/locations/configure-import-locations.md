---
description: 분류 데이터를 업로드할 수 있는 클라우드 가져오기 계정 및 위치를 구성합니다.
keywords: Analysis Workspace
title: 클라우드 가져오기 위치 구성
feature: Classifications
exl-id: 55179868-6228-44ff-835c-f4a7b38e929b
source-git-commit: f71b80dce9d447c431130901d86947d23e28d378
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 7%

---

# 클라우드 가져오기 위치 구성

<!-- This page is almost duplicated with the "Configure cloud export locations" article in CJA. Differences are that Snowflake isn't supported here and there is a Suffix field for each account type. -->

클라우드 대상에서 Adobe Analytics 분류 데이터를 가져오려면 먼저 분류 데이터를 수집할 계정 및 해당 계정 내의 위치를 추가하고 구성해야 합니다.

이 프로세스는 계정(예: Amazon S3 역할 ARN, Google Cloud Platform 등)과 계정 내 위치(예: 계정 내 폴더)를 추가하고 구성하는 것으로 구성됩니다.

클라우드 가져오기 위치를 구성하려면:

1. 위치를 추가하려면 먼저 계정을 추가해야 합니다. 아직 계정이 없다면 의 설명에 따라 계정을 추가합니다. [클라우드 가져오기 계정 구성](/help/components/locations/configure-import-accounts.md).
1. Adobe Analytics에서 [!UICONTROL **구성 요소**] > [!UICONTROL **위치**].
1. 다음에서 [!UICONTROL 위치] 페이지에서 [!UICONTROL **위치**] 탭.
1. 선택 [!UICONTROL **위치 추가**]. <!-- add screenshot? -->

   위치 대화 상자가 표시됩니다.
1. 다음 정보를 지정합니다. |필드 | 함수 | ------------------- | [!UICONTROL **이름**] | 위치의 이름입니다.  | | [!UICONTROL **설명**] | 같은 계정 유형의 다른 계정과 구분할 수 있도록 계정에 대한 간단한 설명을 제공합니다. | | [!UICONTROL **위치 계정**] | 만든 위치 계정 선택 [계정 추가](#add-an-account). |

1. 다음에서 [!UICONTROL **위치 속성**] 섹션에서 위치 계정의 계정 유형과 관련된 정보를 지정합니다.

   구성 지침을 보려면 아래에서 선택한 계정 유형에 해당하는 아래 섹션을 확장합니다. [!UICONTROL **위치 계정**] 필드.

   +++Amazon S3 Role ARN

   Amazon S3 역할 ARN 위치를 구성하려면 다음 정보를 지정하십시오.

   | 필드 | 함수 |
   |---------|----------|
   | [!UICONTROL **버킷 이름**] | Adobe Analytics 데이터를 전송할 Amazon S3 계정 내의 버킷입니다. |
   | [!UICONTROL **키 접두사**] | 데이터를 저장할 버킷 내의 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예: folder_name/ |

   {style="table-layout:auto"}

+++

   +++Google Cloud 플랫폼

   다음 정보를 지정하여 Google Cloud Platform 위치를 구성하십시오.

   | 필드 | 함수 |
   |---------|----------|
   | [!UICONTROL **버킷 이름**] | Adobe Analytics 데이터를 전송할 GCP 계정 내의 버킷입니다. 이 버킷에 파일을 업로드할 수 있도록 Adobe이 제공한 사용자에 대한 권한을 부여했는지 확인하십시오. |
   | [!UICONTROL **키 접두사**] | 데이터를 저장할 버킷 내의 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예: folder_name/ |

   {style="table-layout:auto"}

+++

   +++Azure SAS

   Azure SAS 위치를 구성하려면 다음 정보를 지정하십시오.

   | 필드 | 함수 |
   |---------|----------|
   | [!UICONTROL **컨테이너 이름**] | Adobe Analytics 데이터를 전송할 지정한 계정 내의 컨테이너입니다. |
   | [!UICONTROL **키 접두사**] | 데이터를 저장할 컨테이너 내의 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예, `folder_name/` |

   {style="table-layout:auto"}

+++

   +++Azure RBAC

   Azure RBAC 위치를 구성하려면 다음 정보를 지정하십시오.

   | 필드 | 함수 |
   |---------|----------|
   | [!UICONTROL **컨테이너 이름**] | Adobe Analytics 데이터를 전송할 지정한 계정 내의 컨테이너입니다. 이전에 만든 Azure 애플리케이션에 파일을 업로드할 수 있는 권한을 부여했는지 확인하십시오. |
   | [!UICONTROL **키 접두사**] | 데이터를 저장할 컨테이너 내의 폴더입니다. 폴더 이름을 지정한 다음 이름 뒤에 백슬래시를 추가하여 폴더를 만듭니다. 예, `folder_name/` |
   | [!UICONTROL **계정 이름**] | Azure 스토리지 계정입니다. |

   {style="table-layout:auto"}

+++

1. [!UICONTROL **저장**]&#x200B;을 선택합니다.

   이제 구성한 계정 및 위치에서 데이터를 가져올 수 있습니다.

   데이터는 가져온 후 클라우드 대상에서 삭제되지 않습니다.

   >[!NOTE]
   >
   >   이전에 을 사용한 경우 [분류를 가져오는 FTP](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md) Adobe Analytics에 FIN 파일을 업로드해야 했습니다. 클라우드 계정에서 가져올 때는 이 FIN 파일이 필요하지 않습니다.

