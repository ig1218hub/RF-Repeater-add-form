# RF중계기 신설 양식 작성기

현장에서 휴대폰으로 RF중계기 신설 양식(4페이지)을 작성하고, 원본 양식 그대로 `.pptx` 파일로 저장하는 웹 페이지입니다.

- 서버 없이 동작합니다. 입력한 내용과 사진은 외부로 전송되지 않고, 브라우저 안에서 PPT 파일로 만들어집니다.
- 입력 내용은 해당 기기의 브라우저에 자동 저장됩니다(텍스트는 localStorage, 사진은 IndexedDB).
- PPT 양식은 `index.html` 안에 base64로 들어 있습니다.

## GitHub Pages로 배포

1. 새 저장소를 만들고 `index.html`을 저장소 최상위에 올립니다.
2. 저장소 **Settings → Pages**에서 Source를 `Deploy from a branch`로, Branch를 `main` / `(root)`로 선택하고 저장합니다.
3. 1~2분 뒤 `https://<계정명>.github.io/<저장소명>/` 주소로 접속합니다.

## 필요 사항

- 인터넷 연결: PPT 생성 라이브러리(JSZip)와 글꼴을 CDN에서 불러옵니다.
- 지원 브라우저: 최신 Chrome, Safari(iOS 15 이상), Samsung Internet, Edge
- '공유' 버튼은 파일 공유를 지원하는 모바일 브라우저에서만 표시됩니다(카카오톡, 메일 등으로 바로 전송).
