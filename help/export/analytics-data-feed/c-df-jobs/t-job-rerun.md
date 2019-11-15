---
description: '[작업] 목록에서 하나 이상의 작업을 다시 실행할 수 있습니다.'
keywords: Data Feed;job;rerun
solution: Analytics
title: 작업 재실행
uuid: 5caf95da-dd88-4b1a-a081-684f4fd1f714
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# 작업 재실행

[작업] 목록에서 하나 이상의 작업을 다시 실행할 수 있습니다.

1. 재실행하려는 작업을 하나 이상 선택합니다.
1. Click **[!UICONTROL Rerun Job]**.

   재실행 프로세스는 현재 작업 상태에 따라 다릅니다.

   | 상태 | 서버에서 캐시된 파일 이름 | 프로세스 |
   |---|---|---|
   | 완료 | 예 | 파일이 다시 전송됩니다. |
   | 완료 | 아니오 | 작업이 다시 처리된 다음 다시 전송됩니다. |
   | 실패 | 아니오 | 작업이 다시 처리된 다음 다시 전송됩니다. |
   | 기타 상태 | N/A | 지원되지 않음. |

