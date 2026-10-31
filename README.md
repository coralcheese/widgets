# Widgets

직접 만든 HTML 페이지들을 모아두는 정적 사이트. `main`에 push하면 GitHub Pages(Deploy from branch)로 배포된다.

## 페이지 추가

1. `pages/` 폴더(하위 폴더 가능)에 `.html` 파일을 넣는다.
2. `<head>`에 메타 정보를 넣는다. 모두 선택 사항.

   ```html
   <title>페이지 제목</title>
   <meta name="description" content="한 줄 설명">
   <meta name="tags" content="태그1, 태그2">
   <meta name="date" content="2026-11-01">
   ```

   - 제목이 없으면 파일명을 쓴다.
   - 날짜가 없으면 비워두고, 정렬 시 맨 뒤로 간다.

3. 커밋 후 `main`에 push.

목록은 브라우저가 GitHub API로 `pages/` 파일 목록을 받아 각 HTML의 메타 정보를 직접 읽어서 만든다.
API 호출 결과는 브라우저에 5분간 캐시되므로, 새 페이지는 push 후 최대 몇 분 뒤에 보일 수 있다.

## 로컬 미리보기

```bash
python -m http.server 8000
```

`http://localhost:8000` 접속. 파일 목록은 GitHub의 `main` 기준이라, push 전 새 파일은 로컬 미리보기 목록에 나오지 않는다.
