# Ottega-Gaeanta 서버는 2021.10.15 이후로 비활성화 하였습니다.



**# <img src="https://lab.ssafy.com/s05-bigdata-dist/S05P21B206/-/raw/develop/frontend/src/assets/hanger.png" alt="image-20211029182657119" width="30" height="30"/> Ottega Gaeanta**

---

옷을 어떻게 입을지 몰라 고민하는 사람들을 위해 120만건의 여성 패션 데이터를 기반한 Look-Book 서비스입니다.

- 총 개발 기간 : 6주
- 팀원 : 5명
- 맡은 역할 : ???

---

## 기능

**1.** 스타일 검색

**2.** 스타일 색 조합 평가

**3.** 퍼스널 컬러 진단

---

## 와이어 프레임

**-** [B4A1 피그마 초안](https://www.figma.com/file/lhDtkfKlM8cGv4efBdTGrO/B4A1-%ED%94%BC%EA%B7%B8%EB%A7%88-%EC%B4%88%EC%95%88?node-id=0%3A1)

---

## 데이터 구조

**-** [DB 구조](https://www.notion.so/DB-31e92abfea9849eb915e8b67d74ee96e)

---

**## 주요 기술스택(특이점)**

**-** **Frontend**

  **-** Vue.js

**-** **BackEnd**

  **-** SpringBoot

  **-** MongoDB

  **-** Flask Model Server

​    **-** MaskRCNN Model(Tensorflow), Pillow Library

​    **-** Docker Flask Server

​    **-** MaskRCNN Model 사용하여 상의, 하의, 아우터, 드레스 분리

​    **-** Pillow Library 사용하여 색 추출

​    **-** {“outer”:”beige”,"dress":"skyblue","pants":"","top":""} → Json 형식

​    **-** Flask Server README.md Link ([https://lab.ssafy.com/s05-bigdata-dist/S05P21B206/-/tree/develop/backend/Flask Server](https://lab.ssafy.com/s05-bigdata-dist/S05P21B206/-/tree/develop/backend/Flask%20Server))

**-** **Hadoop**

  **-** 120만건의 패션 데이터 전처리

---

## 프로젝트 구조

![image-20211029235314752](C:\Users\multicampus\AppData\Roaming\Typora\typora-user-images\image-20211029235314752.png)

