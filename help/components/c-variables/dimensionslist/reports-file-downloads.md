---
description: 파일 다운로드는 방문자가 사이트에서 파일을 다운로드하는 빈도를 파악하는 데 도움이 됩니다. 파일 다운로드의 예에는 워드 프로세서 문서, 스프레드시트, 오디오 파일, 동영상 파일, 사용자 설명서 등이 있습니다. 여기에는 브라우저에서 직접 저장하고 여는 파일과 사용자의 컴퓨터에 저장된 파일이 모두 포함됩니다. 보고서에는 다운로드 중인 파일의 이름(파일 액세스에 필요한 전체 URL 포함)이 표시됩니다.
title: 파일 다운로드
topic: Reports
uuid: 897fc221-aa30-4eac-aca6-bccb76adaf71
translation-type: tm+mt
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16

---


# 파일 다운로드

파일 다운로드는 방문자가 사이트에서 파일을 다운로드하는 빈도를 파악하는 데 도움이 됩니다. 파일 다운로드의 예에는 워드 프로세서 문서, 스프레드시트, 오디오 파일, 동영상 파일, 사용자 설명서 등이 있습니다. 여기에는 브라우저에서 직접 저장하고 여는 파일과 사용자의 컴퓨터에 저장된 파일이 모두 포함됩니다. 보고서에는 다운로드 중인 파일의 이름(파일 액세스에 필요한 전체 URL 포함)이 표시됩니다.

**탐색**

**[!UICONTROL Reports]** > **[!UICONTROL Site Content]** > **[!UICONTROL Links]** > **[!UICONTROL File Downloads]**

이 보고서가 기본 위치에 없을 경우에는 관리자에게 문의하십시오. 관리자가 조직에 맞게 기본 메뉴 구조를 변경했을 수 있습니다.

이 보고서를 사용하여 다음을 수행할 수 있습니다.

* 사이트에서 가장 자주 다운로드되는 파일을 확인합니다.
* 특정 기간에 더 자주 다운로드되는 파일이 있는지 확인합니다.
* 해당 문서에 대해 모든 형식이 필요한지 여부를 검증합니다.

   예를 들어 현재 사용 설명서를 12개 언어로 번역하여 웹 사이트에서 사용할 수 있도록 지원하는 경우를 가정합니다. 파일 다운로드 보고 기능을 사용하여 각 버전의 사용 설명서 다운로드 빈도를 파악하고 설명서를 계속 12개 언어로 모두 번역하는 일의 효율을 평가할 수 있습니다.

**문제 해결**

마케팅 보고서는 사이트에서 JavaScript 코드가 포함된 페이지를 통한 파일 다운로드 정보를 캡처합니다. 그러나 파일 다운로드 정보를 보고하려면 특정 변수가 있고 올바르게 설정되어 있어야 합니다. 이 보고서에 데이터가 표시되지 않거나 예상한 값이 표시되지 않는 경우는 아래 단계를 수행하여 구현의 유효성을 검사합니다.

1. 사이트에서 글로벌 JavaScript 파일을 찾습니다. [!DNL s_code.js]라는 이름을 많이 사용하지만 다른 이름으로 변경되었을 수도 있습니다. 이름이 변경된 경우는 사이트의 JavaScript 파일에서 값 *`s.account`*&#x200B;를 찾습니다. 이 값은 JavaScript 코드에 들어 있습니다.

1. 이 파일에서 [s.trackDownloadLinks](https://docs.adobe.com/content/help/ko-KR/analytics/implementation/vars/config-vars/trackdownloadlinks.html) 변수를 찾습니다. *true*&#x200B;로 설정되어 있는지 확인합니다.

1. [s.linkDownloadFileTypes](https://docs.adobe.com/content/help/ko-KR/analytics/implementation/vars/config-vars/linkdownloadfiletypes.html) 변수를 찾습니다. 원하는 파일 확장자가 모두 이 목록에 있는지 확인합니다. 필요한 경우 [!DNL .zip].[!DNL .pdf] 등의 누락된 확장자를 추가합니다.

If these variables appear to be configured correctly, but the [!UICONTROL File Downloads Report] still is not receiving data, your organization&#39;s supported users should contact Customer Care.
