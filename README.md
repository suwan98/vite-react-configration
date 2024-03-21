## Create Vite없이 Vite + React 환경 구성하기

<br />
<br />

## 0. 설치 환경 구성

**package.json 생성을 위해 아래 키워드를 통해 생성합니다.**

```bash
pnpm init
```

React 애플리케이션 구동을 위해 React와 ReactDOM라이브러리를 설치합니다.

```bash
$ pnpm i -D react react-dom
```

<br />
<br />

## 1. Vite 및 필요 플러그인 설치하기

Vite와 Vite 구성을 위한 플러그인인 `@vitejs/plugin-react`를 설치합니다.

### @vitejs/plugin-react

- Vite를 위한 React 공식 플러그인입니다.
- Vite 프로젝트에서 React를 사용 시 필요한 기능들을 제공합니다.

**주요기능**

1. Fast Refresh

- 컴포넌트 상태를 유지하며 코드의 변경사항을 즉시 반영할 수 있습니다.
- 최종적으로 개발시 코드의 변화가 일어나면 페이지를 새로고침하지 않고도 변경사항을 바로 확인할 수 있게됩니다.

2. JSX Transfile

- JSX코드를 바닐라 JavsScript 코드로 변환해줍니다.
- Vite와 해당 플러그인을 사용하게되면, 이러한 과정을 자동으로 구동해줘, 개발자가 따로 Babel등을 설정할 필요가 없습니다.

3. TypeScript 지원

- TypeScript 사용 시 추가 설정 없이도 타입스크립트 파일(.ts,.tsx)을 자동으로 처리해줍니다.

```bash
$ pnpm i -D vite @vitejs/plugin-react
```

## 2. HTML 파일 생성하기

Vite는 기본적으로 개발서버 시작 시 `index.html`을 파일의 진입적으로 사용합니다.

- 따라서 프로젝트 루트에 `index.html`파일을 생성하고 아래와 같은 내용을 추가합니다.

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>React + Vite</title>
  </head>

  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.jsx"></script>
  </body>
</html>
```
