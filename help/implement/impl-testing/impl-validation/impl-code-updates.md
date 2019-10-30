---
description: .JS 파일이나 HTML 코드에 대한 수정 사항을 테스트하는 것은 고객의 책임입니다. 프로덕션 웹 사이트에 대한 수정 사항을 게시하려면 그 전에 테스트를 완료해야 합니다.
keywords: Analytics 구현
seo-description: .JS 파일이나 HTML 코드에 대한 수정 사항을 테스트하는 것은 고객의 책임입니다. 프로덕션 웹 사이트에 대한 수정 사항을 게시하려면 그 전에 테스트를 완료해야 합니다.
seo-title: 코드 수정
solution: Analytics
title: 코드 수정
topic: 개발자 및 구현
uuid: efac045e-15f5-45f6-a21a-de6c4b0a8185
translation-type: ht
source-git-commit: 86fe1b3650100a05e52fb2102134fee515c871b1

---


# 코드 수정

.JS 파일이나 HTML 코드에 대한 수정 사항을 테스트하는 것은 고객의 책임입니다. 프로덕션 웹 사이트에 대한 수정 사항을 게시하려면 그 전에 테스트를 완료해야 합니다.

줄 바꿈/리턴 문자가 HTML 내에 삽입된 코드나 [!DNL .JS] 파일 내부에서 제거되거나 바뀌지 않도록 하십시오. JavaScript가 모든 페이지 및 페이지 템플릿에서 오류 없이 실행되도록 하십시오(Internet Explorer의 [인터넷 옵션]에서 [고급] 탭을 선택한 다음 [모든 스크립트 오류에 관련된 알림 표시] 클릭).

오류 테스트 시, 코드를 기본 HTML 페이지에 붙여넣어 다른 페이지 요소/개체 때문에 오류가 발생하는지 파악하십시오.

```js
<html><head></head><body>
...paste code here to debug...
</body></html>
```

