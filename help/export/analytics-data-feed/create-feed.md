---
title: 데이터 피드 만들기 또는 편집
description: 데이터 피드를 만들거나 편집하는 방법을 알아봅니다.
feature: Data Feeds
exl-id: 36c8a40e-6137-4836-9d4b-bebf17b932bc
source-git-commit: 60335be9a60b467969f5e1796ce465a7d453951f
workflow-type: tm+mt
source-wordcount: '1518'
ht-degree: 56%

---

# 데이터 피드 만들기 또는 편집

데이터 피드를 만들면 Adobe에서 원시 데이터 파일을 보낼 위치와 각 파일에 포함할 내용을 알 수 있습니다. 이 페이지에는 데이터 피드를 만들 때 사용자 지정할 수 있는 개별 설정이 나열됩니다.

데이터 피드에 대한 기본 지식이 있으면 이 페이지를 읽는 데 도움이 됩니다. [데이터 피드 개요](data-feed-overview.md)를 참조하여 데이터 피드를 만들기 위한 요구 사항을 충족하는지 확인하십시오.

## 피드 정보 필드

* **이름**: 데이터 피드의 이름. 선택된 보고서 세트 내에서 고유해야 하며 최대 255자까지 사용할 수 있습니다.
* **보고서 세트:** 데이터 피드의 기반이 되는 보고서 세트. 동일한 보고서 세트에 대해 여러 데이터 피드를 만드는 경우 데이터 피드의 열 정의가 서로 달라야 합니다. 소스 보고서 세트만 데이터 피드를 지원합니다. 가상 보고서 세트는 지원되지 않습니다.
* **완료 시 이메일 보내기**: 피드의 처리가 완료되면 알림을 받을 이메일 주소. 이메일 주소 형식을 제대로 지정해야 합니다.
* **피드 간격**: 시간별 피드에는 1시간 동안의 데이터가 포함됩니다. 일별 피드에는 하루 분량의 데이터가 포함됩니다. 여기에는 보고서 세트 시간대의 자정부터 자정까지의 데이터가 포함됩니다.
* **프로세싱 지연**: 데이터 피드 파일을 처리하기 전에 지정된 시간을 대기하십시오. 지연은 오프라인 디바이스를 온라인 상태로 전환하여 데이터를 전송할 수 있는 기회를 모바일 구현에 제공하는 데 유용합니다. 또한 이전에 처리된 파일을 관리할 때 조직의 서버측 프로세스를 수용하는 데 사용할 수도 있습니다. 대부분의 경우에는 지연이 필요하지 않습니다. 피드는 최대 120분 정도 지연될 수 있습니다.
* **시작 및 종료 날짜**: 시작 날짜는 데이터 피드를 원하는 첫 번째 날짜를 나타냅니다. 이전 데이터에 대한 데이터 피드 처리를 즉시 시작하려면 이 날짜를 과거로 설정하십시오. 피드는 종료 날짜가 될 때까지 계속 처리합니다. 시작 및 종료 날짜는 보고서 세트의 시간대를 기반으로 합니다.
* **지속 피드**: 이 확인란을 선택하면 종료 날짜가 제거되어 피드가 무기한 실행될 수 있습니다. 한 피드가 이전 데이터 처리를 완료하면 한 피드가 지정된 시간 또는 날 동안 데이터 수집이 완료되기를 기다립니다. 현재 시간 또는 날이 끝나면 지정된 지연 후 처리가 시작됩니다.

## 대상 필드

대상 필드에서 사용할 수 있는 필드는 대상 유형에 따라 다릅니다.

### Google Cloud Platform

보안 대상으로 GCP 스토리지 버킷에 액세스

**필드**
* *유형:* Google Cloud Platform의 대상 유형
* *프로젝트 ID:* 저장소 버킷이 있는 GCP 프로젝트 ID
* *저장소 버킷 이름:* 점이 없는 버킷 이름은 3-63자로 제한됩니다. 점이 포함된 이름은 최대 222자를 포함할 수 있지만 점으로 구분된 각 구성 요소는 63자를 초과할 수 없습니다.
* *경로(선택 사항):* &amp; *경로에 보고서 세트 ID 추가:* 검색 또는 저장할 리소스 위치

![GCP 정보](assets/dest-gcp.png)

**서비스 계정 생성 프로세스**

Google Cloud Platform 대상에 대한 서비스 계정을 만드는 데 사용자가 필요합니다.

Analytics 조직당 하나의 GCP 서비스 계정만 허용됩니다. 데이터 피드에 대해 서비스 계정이 만들어지면 조직 내의 모든 추가 데이터 피드가 서비스 계정으로 미리 채워집니다.

![GCP 서비스 계정 정보](assets/service-account.png)


### Amazon S3

신뢰할 수 있는 엔터티 내의 IAM 역할을 통해 액세스되는 Amazon S3 버킷 저장소입니다.

**필드**

* *유형:* Amazon S3의 대상 유형
* *버킷:* S3 버킷 이름
* *신뢰할 수 있는 엔터티 ARN:* AWS IAM 엔터티 ARN `arn:aws:iam::<12 digit account number>:user/<username>`
* *역할 ARN:* AWS IAM 역할 ARN `arn:aws:iam::<12 digit account number>:role/<role name>`
* *경로(선택 사항):* &amp; *경로에 보고서 세트 ID 추가:* 검색 또는 저장할 리소스 위치
* *지역 지정(선택 사항):* CN 영역을 포함하여 사용 가능한 모든 AWS 지역의 드롭다운

![Amazon S3 정보](assets/dest-s3-secure.png)


**신뢰할 수 있는 엔터티 만들기 및 선택**

사용자는 드롭다운에 나열된 옵션 중에서 신뢰할 수 있는 엔티티를 선택하거나 을(를) 클릭하여 새 엔티티를 만들고 검색할 수 있습니다 `Create Entity` 버튼을 클릭합니다.

을(를) 클릭한 후 `Create Entity` 버튼을 클릭하면 사용자가 인증 프로세스로 리디렉션됩니다. 사용자가 인증되면 신뢰할 수 있는 엔티티가 생성되고 드롭다운의 옵션에 추가됩니다.

드롭다운에는 이 사용자가 조직에서 생성한 모든 신뢰할 수 있는 엔티티가 나열됩니다.

![엔티티 정보](assets/entity-creation.png)

이전 방법을 통해 피드를 Amazon S3 버킷으로 직접 보낼 수 있습니다. 자세한 내용은 Amazon S3 문서 내의 [Amazon S3 버킷 이름 지정 요구 사항](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-s3-bucket-naming-requirements.html)을 참조하십시오.

**필드 - 사용되지 않음**

* *유형:* 사용되지 않는 S3 메서드의 대상 유형입니다.
* *버킷:* Amazon S3 버킷 이름
* *경로(선택 사항):* &amp; *경로에 보고서 세트 ID 추가:* 검색 또는 저장할 리소스 위치
* *액세스 키:* AWS 사용자의 키 ID에 액세스
* *비밀 키:* AWS 사용자의 비밀 키
* *암호 키 확인:* AWS 사용자의 암호 키 다시 입력

![S3 정보](assets/dest-s3-dpr.png)

데이터 피드 업로드를 위해 제공한 사용자는 다음 [권한](https://docs.aws.amazon.com/AmazonS3/latest/API/API_Operations_Amazon_Simple_Storage_Service.html)이 있어야 합니다.

* s3:GetObject
* s3:PutObject
* s3:PutObjectAcl

Amazon S3 버킷에 대한 각 업로드의 경우 [!DNL Analytics]는 버킷에 필요한 정책이 있는지 여부에 관계없이 버킷 소유자를 BucketOwnerFullControl ACL에 추가합니다. 자세한 내용은 “[Amazon S3 데이터 피드에 대한 BucketOwnerFullControl 설정은 무엇입니까?](df-faq.md#BucketOwnerFullControl)”를 참조하십시오.

**지원되는 AWS 지역**:
* us-east-2
* us-east-1
* us-west-1
* us-west-2
* ap-south-1
* ap-northeast-2
* ap-southeast-1
* ap-southeast-2
* ap-northeast-1
* ca-central-1
* eu-central-1
* eu-west-1
* eu-west-2
* eu-west-3
* eu-north-1
* sa-east-1
* cn-north-1
* cn-northwest-1


### Azure Blob

RBAC(역할 기반 액세스 제어) 또는 SAS(공유 액세스 서명)를 사용하는 Azure Blob 보안 대상입니다. 액세스 제어를 선택하면 패널의 컨텐츠가 해당 필드를 반영하도록 업데이트됩니다.

**필드 - RBAC**
* *유형:* Azure Blob의 대상 유형
* *액세스 제어:* RBAC 또는 SAS 사용 옵션
* *Active Directory 테넌트 ID:* Azure 계정의 조직 ID
* *애플리케이션 ID:* Active Directory 어댑터의 응용 프로그램 ID
* *클라이언트 암호:* Azure 클라이언트 암호
* *저장소 계정 이름:* 데이터 개체가 포함된 계정 이름
* *컨테이너 이름:* 주어진 저장소 계정에 속하는 컨테이너입니다.
* *경로(선택 사항):* &amp; *경로에 보고서 세트 ID 추가:* 검색 또는 저장할 리소스 위치

![Azure RBAC 정보](assets/dest-azure-rbac.png)

**필드 - SAS**
* *유형:* Azure Blob의 대상 유형
* *액세스 제어:* RBAC 또는 SAS 사용 옵션
* *Active Directory 테넌트 ID:* Azure Active Directory 인스턴스의 ID
* *애플리케이션 ID:* Active Directory 어댑터의 응용 프로그램 ID
* *클라이언트 암호:* Azure 클라이언트 암호
* *키 저장소 URI:* Azure 키 저장소 위치
* *주요 저장소 암호 이름:* 보안 키 자격 증명 모음에 액세스하는 암호 이름
* *경로(선택 사항):* &amp; *경로에 보고서 세트 ID 추가:* 검색 또는 저장할 리소스 위치

![Azure SAS 정보](assets/dest-azure-sas.png)

**필드 - 사용되지 않음**
* *유형:* Azure Blob의 대상 유형
* *컨테이너:* Azure 컨테이너 이름
* *경로(선택 사항):* &amp; *경로에 보고서 세트 ID 추가:* 검색 또는 저장할 리소스 위치
* *계정:* Azure 계정 암호
* *키 저장소 URI:* Azure 키 저장소 위치
* *주요 저장소 암호 이름:* 보안 키 자격 증명 모음에 액세스하는 암호 이름

피드 대상의 디스크 공간을 관리하려면 자체 프로세스를 구현해야 합니다. Adobe는 서버에서 데이터를 삭제하지 않습니다.
자세한 내용은 Microsoft Azure 문서 내에서 [저장소 계정 만들기](https://docs.microsoft.com/ko-kr/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal#view-and-copy-storage-access-keys)를 참조하십시오.

![Azure 사용 중지 정보](assets/dest-azure-dpr.png)

>[!NOTE]
>
>피드 대상의 디스크 공간을 관리하려면 자체 프로세스를 구현해야 합니다. Adobe는 서버에서 데이터를 삭제하지 않습니다.

### FTP - 사용되지 않음

**필드**
* *유형:* FTP 대상 유형
* *호스트:* 호스트에 액세스할 끝점
* *경로(선택 사항):* &amp; *경로에 보고서 세트 ID 추가:* 검색 또는 저장할 리소스 위치
* *사용자 이름:* 호스트의 사용자 이름
* *암호:* 호스트의 암호
* *암호 확인:* 호스트의 암호 재입력 및 확인

![FTP 정보](assets/dest-ftp-dpr.png)

### SFTP - 사용하지 않음

데이터 피드에 대한 SFTP 지원을 사용할 수 있습니다. 유효한 RSA 또는 DSA 공개 키를 포함하기 위해 SFTP 호스트, 사용자 이름 및 대상 사이트가 필요합니다. 피드를 만들 때 적절한 공개 키를 다운로드할 수 있습니다.

**필드**
* *유형:* SFTP 대상 유형
* *호스트:* 호스트에 액세스할 끝점
* *경로(선택 사항):* &amp; *경로에 보고서 세트 ID 추가:* 검색 또는 저장할 리소스 위치
* *RSA 공개 키:* 또는 *DSA 공개 키:* 호스트에 액세스할 공개 키

![SFTP 정보](assets/dest-sftp-dpr.png)

## 데이터 열 정의

데이터가 있는지 여부에 관계없이 모든 열을 사용할 수 있습니다. 데이터 피드는 하나 이상의 열을 포함해야 합니다.

* **이스케이프 처리된 문자 제거**: 데이터를 수집할 때 일부 문자 (예: 줄바꿈)가 문제를 초래할 수 있습니다. 피드 파일에서 이러한 문자를 제거하려면 이 확인란을 선택하십시오.
* **압축 포맷**: 사용된 압축 종류입니다. Gzip은 파일을 `.tar.gz` 형식으로 출력합니다. Zip은 파일을 `.zip` 형식으로 출력합니다.
* **패키징 타입**: 단일 파일이 `hit_data.tsv` 파일을 하나의 파일로 출력합니다. 이 파일은 매우 클 수 있습니다. 여러 파일이 데이터를 2GB 청크 (압축되지 않음)로 페이지를 매깁니다. 여러 파일을 선택하고 보고 기간의 압축되지 않은 데이터가 2GB 미만이면 하나의 파일이 전송됩니다. 대부분의 데이터 피드에서 여러 파일을 사용하는 것이 좋습니다.
* **매니패스트**: 피드 간격에 대한 데이터가 수집되지 않을 때 Adobe에서 [매니페스트 파일](c-df-contents/datafeeds-contents.md#feed-manifest)을 대상에 전송할지 여부를 나타냅니다. 매니페스트 파일을 선택하면 데이터가 수집되지 않을 때 다음과 유사한 매니페스트 파일이 수신됩니다.

```text
   Datafeed-Manifest-Version: 1.0
    Lookup-Files: 0
    Data-Files: 0
    Total-Records: 0
```

* **열 템플릿**: 많은 데이터 피드를 만들 때는 열 템플릿을 만드는 것이 좋습니다. 열 템플릿을 선택하면 지정된 열이 템플릿에 자동으로 포함됩니다. Adobe도 기본적으로 여러 템플릿을 제공합니다.
* **사용 가능한 열**: Adobe Analytics에서 사용 가능한 모든 데이터 열. 데이터 피드에 모든 열을 포함하려면 [!UICONTROL 모두 추가]를 클릭하십시오.
* **포함된 열**: 데이터 피드에 포함할 열. 데이터 피드에 모든 열을 제거하려면 [!UICONTROL 모두 제거]를 클릭하십시오.
* **CSV 다운로드**: 포함된 모든 열이 들어 있는 CSV 파일을 다운로드합니다.
