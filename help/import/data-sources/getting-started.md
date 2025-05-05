---
title: 데이터 소스 시작하기
description: 예제 데이터를 개발 보고서 세트에 업로드합니다.
exl-id: d9f74f55-abbb-4ceb-b4db-8d3c32aacd4a
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# 데이터 소스 시작하기

다음 단계에 따라 샘플 데이터를 개발 보고서 세트에 쉽게 업로드하여 워크플로우의 작동 방식을 확인할 수 있습니다. 프로세스를 이해하면 조직의 구현에 맞게 프로세스를 확장하고 맞춤화할 수 있습니다.

>[!IMPORTANT]
>
>개발 또는 테스트 보고서 세트를 사용하여 다음 단계를 수행합니다. 데이터 원본을 통해 업로드된 데이터는 **영구**&#x200B;입니다. 업로드되면 프로덕션 보고서 세트 데이터에 영향을 줍니다.

1. [https://experience.adobe.com](https://experience.adobe.com)을(를) 통해 Adobe Analytics에 로그인합니다.
1. **[!UICONTROL 관리자]** > **[!UICONTROL 모든 관리자]** > **[!UICONTROL 데이터 원본]**(으)로 이동합니다.
1. 오른쪽 상단의 드롭다운 목록을 사용하여 개발 보고서 세트를 선택합니다.
1. 왼쪽 상단의 **[!UICONTROL 만들기]** 단추를 클릭합니다.
1. [!UICONTROL 범주 선택]에서 &quot;[!UICONTROL 일반]&quot;을 선택하고 [!UICONTROL 유형 선택]에서 &quot;[!UICONTROL 일반 데이터 Source(요약 데이터만)]&quot;을 선택합니다.
1. **[!UICONTROL 활성화]**&#x200B;를 클릭합니다. 팝업 창이 열리고 [!UICONTROL 데이터 Source 활성화 마법사]가 표시됩니다.
   1. 1단계: 데이터 소스에 이름을 지정하고 면책조항 확인란을 클릭합니다.
   1. 2단계: 이 단계는 이전 버전의 Adobe Analytics에서 더 많이 사용되었습니다. 확인란을 클릭한 다음 옆의 텍스트 필드에 값을 입력합니다.
   1. 3단계: 데이터 소스 템플릿 파일에 포함할 지표를 선택합니다. 드롭다운 목록에서 &quot;이벤트 1&quot;을 선택합니다.
   1. 4단계: 이 단계는 이전 버전의 Adobe Analytics에서 더 많이 사용되었습니다. 확인란을 클릭한 다음 옆의 텍스트 필드에 값을 입력합니다.
   1. 5단계: 데이터 소스 템플릿 파일에 포함할 차원을 선택합니다. 드롭다운 목록에서 &quot;eVar 1&quot;을 선택합니다.
   1. 6단계: 템플릿 파일에 포함된 차원 및 지표를 보여주는 요약을 검토합니다.
   1. 7단계: **[!UICONTROL 다운로드]** 단추를 클릭하여 데이터 원본 템플릿 파일을 다운로드합니다. 또한 FTP 사이트에 대한 로그인 자격 증명을 곧 사용할 수 있습니다.
1. 이제 데이터 소스가 만들어지고 다음 단계에서 처리할 데이터를 제공합니다. 원하는 텍스트 편집기에서 다운로드한 파일을 엽니다.
1. 템플릿 파일에는 3개의 줄, 2개의 주석 줄(&quot;`#`&quot;(으)로 시작) 및 머리글 행이 있습니다.

   ```text
   # Generic Data Source (Summary Data Only) template file (user: 123456789 ds_id: 2)
   #    eVar1    event1
   Date    Evar 1    Event 1
   ```

1. 각 항목을 탭으로 구분하여 여러 데이터 행에 입력합니다. 값을 구분하기 위해 공백이나 쉼표를 사용하지 마십시오.
   * 첫 번째 열은 `MM/DD/YYYY/HH/mm/SS` 형식의 날짜입니다.
   * 두 번째 열은 eVar1에 포함할 텍스트 값입니다.
   * 세 번째 열은 이벤트 1을 증가시킬 양입니다.

   ```text
   # Generic Data Source (Summary Data Only) template file (user: 123456789 ds_id: 5)
   #    eVar1    event1
   Date    Evar 1    Event 1
   09/07/YYYY/11/23/00    Data source example value    3
   09/07/YYYY/15/59/00    Another data source value    18
   ```

1. 파일을 저장합니다. 필요한 경우 선택적으로 다른 파일 이름을 지정할 수 있습니다. 파일이 저장되면 텍스트 편집기를 닫을 수 있습니다.
1. Windows 탐색기, Finder 또는 선택한 FTP 클라이언트에서 [ftp://ftp.omniture.com](ftp://ftp.omniture.com)(으)로 이동합니다.
1. 로그인 자격 증명을 입력하라는 메시지가 표시되면 데이터 소스 생성 마법사의 마지막 단계에서 입력한 사용자 이름과 암호를 사용합니다. [!UICONTROL 데이터 소스] (으)로 이동한 다음 만든 데이터 소스 옆에 있는 **[!UICONTROL FTP 정보]**&#x200B;를 클릭하여 다시 참조할 수 있습니다.
1. 인증되면 편집한 파일을 인증된 FTP 창으로 드래그합니다.
1. FTP 창 외부의 아무 위치에나 빈 텍스트 파일을 만듭니다. 한 가지 예외를 제외하고 FTP 사이트에 업로드한 데이터 소스 파일과 동일한 파일 이름을 지정합니다. `.txt` 파일 형식 대신 `.fin` 파일 형식을 지정하십시오. 운영 체제 설정에서 파일 유형을 보고 변경할 수 있는지 확인하십시오.
1. 빈 `.fin` 파일을 데이터 원본 파일과 동일한 FTP 위치로 드래그합니다. `.fin` 파일이 있으면 데이터 원본 파일이 완전히 업로드되어 수집할 준비가 되었음을 Adobe에게 알려 줍니다.
1. 몇 분 후에 파일이 FTP 위치에서 사라지고 보고에 표시됩니다.
1. 데이터 소스 페이지를 새로 고치고 파일이 성공적으로 수집되었는지 확인합니다.
1. Analysis Workspace 로 이동하여 프로젝트를 만듭니다.
1. eVar 1을 작업 영역 캔버스에 차원으로 드래그하고 이벤트 1을 지표로 드래그합니다. Workspace 날짜 범위에 데이터 소스에서 제공한 날짜가 포함되어 있는지 확인합니다.

   ![보고서 예시](assets/success-report.png)

## 다음 단계

[파일 형식](file-format.md): 조직에 맞는 데이터 원본 파일을 만드는 방법에 대한 자세한 내용을 알아봅니다.
