# 웹기반 전자제품 중고거래 플랫폼 '믿을테크마켓'

## Overview

본 프로젝트는 값 비싼 전자제품을 저렴하고 합리적으로 구매하고자 하는 사람들에게 보다 나은 정보를 제공하고 중고거래의 불안함을 해소하는 것에 목표를 둔 프로젝트이다. 웹사이트의 사용자들은 현재 올라온 전자제품 매물들의 이미지를 간편하게 확인 할 수 있고, 본인의 거래희망 지역, 가격에 따라 조회할 수 있다. 거래 시게글에 댓글을 통해 판매자와 소통할 수 있으며 쪽지를 통해 거래 약속을 잡을 수 있도록 기능을 제공하고 있다.

## Stack

- Frontend : React.js (상태관리: Redux, 디자인: React-BootStrap)
- Backend : Node.js
- DB : mySQL

## 기능 구현

- 회원가입 및 로그인
    - bcypt 모듈: 사용자의 비밀번호 DB 암호화하여 저장
    - jsonwebtoken 모듈:  로그인 상태 유지를 위한 토큰 발급
- 게시글 업로드, 조회
    - multer 모듈 : 클라이언트로부터 받은 이미지 파일은 서버 스토리지로 SQL엔 생성된 파일 ID 저장
    - 조회시 서버 스토리지에서 파일 ID를 조회하여 base64로 인코딩 후 클라이언트로 전송
- 댓글, 쪽지 기능
    - Axios POST 방식으로 api 통신 구현, JSON 형식 반환

## Screenshot

![랜딩 페이지](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/eef4b9dc-cfe2-4299-a016-c7ea1cfbf680/스크린샷_2022-02-04_오전_2.06.56.png)

랜딩 페이지

![상품 조회 페이지](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ae61db89-d6b5-4134-8012-2f4f5ec41781/스크린샷_2022-02-04_오전_2.07.15.png)

상품 조회 페이지

![상품별 개별 페이지](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/de742140-6132-44a0-bf1b-77b56f54cef7/스크린샷_2022-02-04_오전_2.08.16.png)

상품별 개별 페이지

![댓글 구현](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ae86c4e5-31ee-42b4-91bf-1328a21d7471/스크린샷_2022-02-04_오전_2.08.37.png)

댓글 구현

![쪽지 구현](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8ee27f1f-149d-4518-8cf6-02e2a38fcfc8/스크린샷_2022-02-04_오전_2.08.52.png)

쪽지 구현

## Team

- 김세한: React 프론트엔드 개발, 기획 / 게시글 전체보기, 작성, 조회 기능 구현
- 이병창: Node.js 백엔드 개발 / 로그인, 회원가입, 댓글, 쪽지 구현
