# TravelHub (React Project)

여행 상품을 탐색하고 일정과 취향에 맞는 여행지를 찾아볼 수 있는 SPA(Single Page Application)입니다.  
React + React Router + styled-components를 사용해 화면을 구성하고, `axios`로 백엔드 API와 통신하도록 설계된 프론트엔드 프로젝트입니다.

> 이 레포지토리는 **React 기반 포트폴리오 프로젝트(TravelHub)**의 프론트엔드 코드만 포함하고 있습니다.

---

## 주요 기능

- **회원가입 / 로그인**
  - 이메일, 닉네임, 비밀번호를 이용한 회원가입
  - 로그인 후 사용자 정보를 전역 상태로 보관하여 다른 페이지에서 활용
- **게시글 목록 페이지 (MainPage)**
  - 게시글 리스트 조회
  - 제목/작성자/작성일 등의 기본 정보 표시
  - 게시글 클릭 시 상세 페이지로 이동
- **게시글 상세 페이지 (ViewPostPage)**
  - 선택한 게시글의 상세 내용 확인
  - 글 작성자일 경우 수정 페이지로 이동할 수 있는 버튼 제공
- **게시글 작성 페이지 (WritePostPage)**
  - 제목, 내용 등을 입력하여 새 게시글 작성
  - 작성 완료 후 목록 또는 상세 페이지로 이동
- **게시글 수정 페이지 (EditPostPage)**
  - 기존 게시글의 제목·내용을 수정
  - 수정 완료 후 해당 게시글 상세 페이지로 이동
- **라우팅 처리**
  - `react-router-dom`을 사용하여 로그인, 회원가입, 메인, 상세, 작성, 수정 페이지 간 라우팅 처리
  - SPA 형태로 페이지 전환 시 전체 새로고침 없이 화면 전환

---

## 기술 스택

### Frontend

- **React** `^19.0.0`
- **React DOM** `^19.0.0`
- **React Router DOM** `^7.1.1`  
  → 페이지 이동, 동적 라우팅
- **styled-components** `5.3.6`  
  → 컴포넌트 단위 스타일링, Theme 기반 확장 용이
- **axios** `^1.7.9`  
  → 백엔드 REST API 연동용 HTTP 클라이언트

### 개발 환경

- **Create React App** 기반  
- **yarn** 패키지 매니저
- Node.js 18+ 권장

---

## 폴더 구조

리포지토리의 대략적인 구조는 다음과 같습니다.

```bash
react-project/
├─ public/
│  ├─ index.html
│  └─ ...  # 이미지 파일
├─ src/
│  ├─ App.js
│  ├─ index.js
│  ├─ reportWebVitals.js
│  ├─ components/
│  │  ├─ page/
│  │  │   ├─ MainPage.jsx         # 메인(게시글 목록) 페이지
│  │  │   ├─ ViewPostPage.jsx     # 게시글 상세 페이지
│  │  │   ├─ WritePostPage.jsx    # 게시글 작성 페이지
│  │  │   ├─ EditPostPage.jsx     # 게시글 수정 페이지
│  │  │   ├─ LoginPage.jsx        # 로그인 페이지
│  │  │   └─ SignupPage.jsx       # 회원가입 페이지
│  │  ├─ ui/
│  │  └─ list/
├─ TravelHub포트폴리오.pdf       # 프로젝트 포트폴리오 문서
├─ package.json
├─ yarn.lock
└─ README.md
````

> 실제 파일명/확장자는 리포지토리 구조에 따라 약간 다를 수 있습니다.

---

## 로컬 실행 방법

### 1. 리포지토리 클론

```bash
git clone https://github.com/imyj1013/react-project.git
cd react-project
```

### 2. 패키지 설치

Yarn 사용 시:

```bash
yarn install
```

또는 npm 사용 시:

```bash
npm install
```

### 3. 개발 서버 실행

```bash
yarn start
# 또는
npm start
```

브라우저에서 아래 주소로 접속합니다.

* [http://localhost:3000](http://localhost:3000)

---

## 화면/플로우 개요

1. 사용자는 메인 페이지에서 전체 게시글 목록을 확인합니다.
2. 상단 또는 특정 버튼에서 **회원가입/로그인 페이지**로 이동할 수 있습니다.
3. 로그인 이후:

   * 메인 페이지에서 **새 글 작성 버튼**을 통해 글 작성 페이지로 이동
   * 자신의 게시글 상세 페이지에서 **수정 버튼**을 통해 수정 페이지로 이동
4. 작성/수정 완료 시 해당 게시글 상세 페이지 또는 메인 페이지로 이동하여 변경사항 확인

자세한 UX 흐름 및 화면 와이어프레임은 **`TravelHub포트폴리오.pdf`** 에 정리되어 있습니다.
