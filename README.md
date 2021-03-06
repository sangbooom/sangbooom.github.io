## 📂 Directory structure
```bash
├── _config.yml   ## 사이트 설정. 사이트 url, 플러그인, 테마 등을 설정한다.
├── _data   ## 사이트 공통 데이터. 다국어, 글로벌 메뉴 등이 있다.
|   └── members.yml
├── _drafts  ## 퍼블리시 하기 전 포맷들이다.
|   ├── begin-with-the-crazy-ideas.md
|   └── on-simplicity-in-technology.md
├── _includes   ## 메뉴, 사이드바.. 와 같은 사이트 요소들.
|   ├── footer.html
|   └── header.html
├── _layouts   ## 레이아웃 정보. _includes의 내용들을 조합한다.
|   ├── default.html
|   └── post.html
├── _posts   ## 포스팅들. 마크다운으로 저장하면 웹페이지로 생성한다.
|   ├── 2007-10-29-why-every-programmer-should-play-nethack.md
|   └── 2009-04-26-barcamp-boston-4-roundup.md
├── _sass   ## 사이트 스타일시트. scss로 관리된다.
|   ├── _base.scss
|   └── _layout.scss
├── _site   ## 실제 웹 페이지에 게시되는 정보들.
├── .jekyll-metadata
└── index.html
```
***
사이트 제목을 바꾸려면 _config.yml에서 title을 뒤진다.

사이트 테마를 바꾸려면 _config.yml에서 theme 관련을 뒤진다.

사이드바를 없애려면 _layout폴더 아래 default나, _config.yml에서 설정된 테마 파일을 뒤진다.

사이드바를 수정하려면 _include폴더 아래 sidebar를 뒤진다.

사이트의 margin, padding을 수정하려면 _sass폴더 아래를 뒤진다.

새로운 글을 쓰려면 _post 폴더 아래에 새로운 markdown 파일을 생성한다.
…
또하나 눈여겨볼 것은, _site 폴더다. _site폴더에 있는 것이 최종 결과물이다. 나머지는 _site를 만들기 위한 자료에 불과하다.

다시 말하면 jekyll은 시작될 때, _site를 제외한 폴더에서 사이트 구성에 필요한 자료를 가져온다. _include에서 사이트 모듈 정보를 불러오고, _layout에서 모듈을 조합하고, _post에서 사이트 본문을 불러온다. ~~ 마지막으로 _site폴더에 진짜 사이트 내용, html코드를 생성한다. 이후에 사이트에 요청이 들어올 때, _site폴더에서 내용을 찾아 응답하는 방식이다.

[출처](https://andole87.github.io/web/making-themeof-minimal-mistakes-2/#)

[mmistakes thema guide](https://mmistakes.github.io/minimal-mistakes/docs/structure/)

[mmistakes thema 깃허브](https://github.com/mmistakes/minimal-mistakes)
