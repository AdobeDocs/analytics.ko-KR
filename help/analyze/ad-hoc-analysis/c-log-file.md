---
title: 로그 파일
description: 문제 해결을 위해 로그 파일을 얻습니다.
translation-type: tm+mt
source-git-commit: 5d96a2868bee48e2294ec2fb27e0340a3bcc50ae
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 5%

---


# 로그 파일

>[!IMPORTANT]
>
>Adobe은 2021년 3월 1일, Ad Hoc Analysis을 종신형으로 전환할 예정이다. [추가 정보](https://adobe.ly/discoverworkspace)

Ad Hoc Analysis 관련 문제를 해결할 때 로그 파일을 얻어야 하는 경우가 있습니다. Adobe은 로그 파일을 사용하여 문제의 근본 원인을 찾고 해결 방법을 제공할 수 있습니다. 이 파일에는 모든 세션의 모든 사용자 상호 작용, 보고서 로드 정보 및 Java 오류 메시지가 포함되어 있습니다. `discover.log` 사용자의 암호와 같은 보호된 정보는 모두 숨겨집니다. 큰 로그 파일은 10MB 단위로 분할됩니다. 로그 파일에 Adobe을 제공할 때 모든 파일이 선택되어 있는지 확인합니다.

## Windows

Windows용 `discover.log` 파일 가져오기:

1. 시작 메뉴를 클릭하고 실행 **을**&#x200B;선택하거나 `[Win]` +를 `[R]`누릅니다.
2. 텍스트 필드에 다음을 붙여 넣고 [ **확인]을 클릭합니다**.

   ```text
   %appdata%/../Local/Adobe/Discover/log
   ```

3. 폴더의 모든 파일을 강조 표시한 다음 마우스 오른쪽 버튼을 클릭하고 보내기 > 압축( **zip) 폴더를 선택합니다**.
4. Adobe 담당자에게 .zip 파일을 제공합니다.

## Mac

Mac OS용 `discover.log` 파일을 얻으려면 다음을 수행합니다.

1. 파인더를 열고 `/Users/your-user/.adobe/Discover/log`
2. 폴더의 모든 파일을 강조 표시한 다음 마우스 오른쪽 버튼을 클릭하고 **압축을 선택합니다**.
3. Adobe 담당자에게 .zip 파일을 제공합니다.

압축된 파일의 전체 크기가 10MB를 초과하는 경우 Adobe 담당자가 임시 FTP 위치를 제공할 수 있습니다.
