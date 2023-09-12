# Deeplearning
단국대 AI 융합 디지털 헬스케어 인재 양성 사업
---

## 왜 딥러닝인가?
- 1997년 : IBM 딥블루가 체스 챔피언 개리 카스파로프를 꺾음
- 2011년 : IBM 왓슷이 제오파디 퀴즈쇼애서 우승
- 2016년 : 딥마인드 알파고가 바둑에서 이세돌 9단을 꺾음
- 2018년 : 웨이모 자율주행 택시 웨이모원 아리조나 피닉스에서 운행
- 2021년 : 깃헙과 오픈AI가 자동 프로그래밍 도구 출시


## AI 민주화가 가능해진 이유
1. 오픈 데이터셋
2. 오픈 엑세스 논문
3. 오픈소스 코드
4. 오픈소스 라이브러리
5. 강력한 소비자용 하드웨어
6. 올인원 클라우드 서비스


## 강의 소개
- 딥러닝 기초
  - 딥러닝 소개 : 배경, 기초 수학, 기본 알고리즘
  - 딥러닝 개발 환경 구축 - 콘다, 핍, 주피터 노트북, 클라우드, 코랩
  - 딥러닝 개발 도구 - 판다스, 넘파이, 텐서플로우, 케라스


# 신경망 모델
강한 AI (인공 일반 지능, 인간의 수준까지) > 약한 AI (알파고 등) > 기계학습(머신러닝) > 신경망 > 딥러닝

## 기계학습
- 데이터로부터 특정 업무 수행을 위한 규칙을 학습
- 딥러닝 외에 다양한 기계학습 알고리즘이 있음
### 기계학습 알고리즘
1. 결정트리
2. 랜덤 포레스트
3. GBM
- 일련의 결정 규칙에 기반한 기계학습 알고리즘
- 정형 데이터 모델링에 최고 성능
4. 선형회귀
5. 로지스틱회귀
- 입력 변수와 출력 변수의 관계를 선형 수식으로 표현
- 가장 오래되었고 가장 널리 쓰이는 모델

### 신경망
- 입력 변수와 출력 변수 관계를 여러 층으로 이루어진 뉴런들의 네트워크로 표현
- 이미지. 음성, 언어, 센서 데이터 모델링에 최고 성능

#### 로컬 시스템 설정
1. 하드웨어
   - GPU : 딥러닝 연산 가속, NVidia, 램 8GB 이상, RTX 3070 이상(추천 RTX 3080)
   - 메모리 : 입력 데이터 로딩할 수 있을 만큼, 16GB 이상(추천 64GB 이상)
   - CPU : GPU 사용하지 않는 연산, AMD 또는 인텔
   - SSD/HDD : 입력 데이터를 저장하기 충분한 만큼 - 1TB SSD 또는 500GB SSD + 4T HDD
   - 파워서플라이 : CPU + GPU 지원 가능한 파워
2. 운영체제
   - 우분투 리눅스 > 윈도우즈 10 + WSL2 > MacOS
3. 소프트웨어
   - 콘다 + 파이썬3 + 주피터 노트북 + 판다스/넘파이/텐서플로우2 + CUDA/cuDNN
   - 호환되는 파이썬3 + 텐서플로우2 + CUDA/cuDNN 버전을 설치해야 함
4. 클라우드
   - AWS, Azure, GCP
   - 딥러닝 개발 환경이 설치된 이미지 제공
   - 사용량에 따라 과금
5. 원격 노트북 서비스
   - 구글 코랩, 캐글 노트북
   - 주피터 노트북 + 한정된 GPU/TPU 자원 제공
   - 일정 시간 동안 사용하지 않으면 연결이 끊김
6. 주피터 노트북
   - 웹 기반 파이썬 개발/실행/문서화 프로그램
     ```
     pip install jupyter
     jupyter notebook
     ```
   - 장점 : 사용이 쉽고 코드 개발 및 실행을 빨리 할 수 있음
   - 단점 : 코드의 버전 관리나 타 프로그램과 연동이 어려움
   - 터미널 상에서 주피터 노트북 설치/실행 : 미니콘다 설치 -> 파이썬3 가상환경 생성/실행 -> 주피터 노트북 설치/실행
7. 판다스
   - 파이썬 대표 오픈소스 데이터 분석/처리 라이브러리
   - 다양한 데이터 입/출력, 변환, 선택, 결합, 정제, 병합 지원
     ```
     pip install -U pandas
     ```
8. 케라스
   - 파이토치와 함께 주요 오픈소스 딥러닝 프레임워크
   - 텐서플로우의 하이레벨 API 제공
   - 텐서플로우 2.0부터 케라스 라이브러리 포함
     ```
      pip install -U tensorflow
     ```
   - 순차적 API : 손쉽게 신경망을 생성할 수 있는 API - 입력층부터 출력층까지 차례로 층을 추가
   - 함수적 API : 여러 종류의 층을 다양하게 조합한 신경망을 생성 가능, 임의의 레이어의 출력들을 다음 레이어의 입력으로 사용가능
   - 객체 지향적 API : 라이브러리가 제공하지 않는 새로운 층/모델 생성 시 사용
