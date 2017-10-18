# 코코스 크리에이터 유저 메뉴얼

## 필요사항

본 문서는 [GitBook](https://www.gitbook.com/)를 기반으로 합니다. [영어원본](http://docs.cocos.com/creator/manual)에서 영문 온라인 버전을 체크하실 수 있습니다.

사이트를 빌드하시려면 [Node.js](https://nodejs.org/en/)와 NPM이 필요합니다.

gitbook 설치:

```bash
npm install gitbook-cli -g
```

gitbook 플러그인 설치:

```bash
gitbook install
```

## 미리보기와 빌드

문서를 미리보기하시려면, 다음과 같은 명령어를 실행하세요:

```bash
gitbook serve
```

문서를 빌드하고 사이트를 호스팅할 웹서버를 실행합니다. 또한 livereload 플러그인을 사용하여 마크다운 소스 파일을 수정하면 자동으로 문서가 재빌드됩니다.

만약 마크다운을 HTML로 빌드하기를 원한다면, 아래의 명령어를 사용하세요:

```bash
gitbook build
```

또한 ebook 형식(PDF, ePub, mobi)으로도 빌드하실 수 있으며, 아래의 가이드를 참조하세요:

https://toolchain.gitbook.com/ebook.html

## 컨텐츠 수정

이 책의 마크다운 소스는 언어별 폴더에 들어있으며 한국어 폴더는 [/ko](ko)입니다. 언어 옵션을 수정하시려면 [LANGS.md](LANGS.md)를 참조해주세요.
원본에서는 중국어와 영어 버전도 존재하지만 번역의 편의상 본 저장소에서는 한국어만 유지합니다.

### 색인

각 언어 폴더에 위치한 [SUMMARY.md](ko/SUMMARY.md) 파일은 빌드할 모든 페이지가 포함되어있으며 또한 이 파일은 사이드 바의 탐색 목록으로도 사용됩니다. 이 색인에 나열되지 않은 페이지들은 빌드되지 않습니다.

이 색인 파일에 각 마크다운 파일에 대한 링크를 작성해주세요. 들여쓰기된 목록은 확장 가능한 세부 주제를 나타냅니다:

```md
- [에디터 사용하기](getting-started/basics/editor-overview.md)
	- [에셋](getting-started/basics/editor-panels/assets.md)
	- [씬](getting-started/basics/editor-panels/scene.md)
	- [노드 트리](getting-started/basics/editor-panels/node-tree.md)
```

토글 가능한 챕터 제목인 '에디터 사용하기'를 만들고 클릭하면 관련된 모든 세부 주제가 보여집니다.

### 첫 페이지

각 언어 폴더의 [index.md](ko/index.md) 파일은 문서의 첫 페이지입니다.

### 페이지 내용

각 페이지의 내용을 수정하시려면 마크다운 소스 파일을 수정하세요. 특별한 양식은 존재하지 않으며 각 페이지의 제목이 `h1`으로 되어있는지만 확인하세요.

## 컨트리뷰션

오타 또는 내용에 문제가 있으면 본 저장소로 알려주세요. 풀 리퀘스트도 환영합니다!

## 기타

본 저장소는 번역의 편의를 위하여 일시적으로 운영하며 추후 원래 저장소인 [https://github.com/cocos-creator/creator-docs](https://github.com/cocos-creator/creator-docs)에 통합할 예정입니다.
