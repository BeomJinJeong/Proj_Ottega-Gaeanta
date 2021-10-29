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
  - 사용자의 선호 스타일 3가지 입력
  - 입력한 선호 스타일을 기반하여 스타일 사진 목록 검색 기능 제공
  - 120만건의 데이터를 보여주기 전에, 많은 양의 데이터를 전처리하는데 Hadoop 사용 (이후 상세히 설명)

**2.** 스타일 색 조합 평가
  - 사용자의 의상을 색 조합에 따라 등급화하여 보여주는 패션 평가 서비스
  - 웹캠을 활용한 방식과 이미지 업로드를 활용한 방식 두 가지를 지원
  - Mask R-CNN 모델을 사용하여 이미지의 상/하의 객체 인식 후, Pillow lib를 사용하여 평균 색 추출 (이후 상세히 설명)
  - 프로젝트 내의 개별적인 색 조합 등급표 기준으로 사용자의 색 조합 평가

**3.** 패피티아이 
  - MBTI + 패션 피플의 합성어
  - 사용자의 옷을 입는 스타일과 행동 성향을 파악할 수 있는 간단한 질문지를 통해 패션 성향을 알아보는 서비스
  - 13개의 질문으로 구성되어 있으며 모든 질문에 대한 답안을 선택하면 10개의 스타일 캐릭터 중 가장 점수가 높은 캐릭터로 결과 반환
  - 카카오톡 공유로, 결과 페이지 공유 가능

---

## 와이어 프레임

**-** [B4A1 피그마 초안](https://www.figma.com/file/lhDtkfKlM8cGv4efBdTGrO/B4A1-%ED%94%BC%EA%B7%B8%EB%A7%88-%EC%B4%88%EC%95%88?node-id=0%3A1)

---

## 데이터 구조

**-** [DB 구조](https://www.notion.so/DB-31e92abfea9849eb915e8b67d74ee96e)

---

**## 주요 기술스택(특이점)**

**-** **Frontend**

    - Vue.js

**-** **BackEnd**

    - SpringBoot

    - MongoDB

    - Flask Model Server

​      - MaskRCNN Model(Tensorflow), Pillow Library

​      - Docker Flask Server

  ​    - MaskRCNN Model 사용하여 상의, 하의, 아우터, 드레스 분리

  ​    - Pillow Library 사용하여 색 추출

  ​    - {“outer”:”beige”,"dress":"skyblue","pants":"","top":""} → Json 형식

  ​    - Flask Server README.md Link ([https://lab.ssafy.com/s05-bigdata-dist/S05P21B206/-/tree/develop/backend/Flask Server](https://lab.ssafy.com/s05-bigdata-dist/S05P21B206/-/tree/develop/backend/Flask%20Server))

**-** **Hadoop**

    **-** 120만건의 패션 데이터 전처리

---

## 프로젝트 구조

![image-20211029235314752](C:\Users\multicampus\AppData\Roaming\Typora\typora-user-images\image-20211029235314752.png)

