# Playdata Data Engineering Track 31 Weekly Retrospct
## Week 2
- 24.04.08
    - Statistics Basic: [통계 기초 개념](https://github.com/S0rrow/Playdata_Project01/blob/main/ext/01_%ED%86%B5%EA%B3%84%EC%9D%98%20%EA%B8%B0%EC%B4%88.ipynb) 소개
        - 평균, 중앙값, 최빈값, 편차 및 표준편차
    - 실습:
        - gs25의 전국 편의점 정보 크롤링해서 pkl로 저장해보기
        - cu편의점의 전국 점포 정보 크롤링해서 pkl로 저장해보기
            - 이거 시간복잡도가 O(n^3)인데...?
- 24.04.09
    - Python 개념: 
        - OOP and FP paradigm
        - class, inheritance, variable and method visiability
        - decorator
    - Django: 기본적인 백엔드 개념에 대한 소개
        - 웹 서버와 WAS
        - 로드 밸런싱과 컨테이너 개념
        - DevOps가 이루어지는 방식
    - Airflow: 개념 소개
    - EDA: Exploratory Data Analysis
    - Database: 여러 가지 데이터베이스들에 대한 소개
        - MySQL:
            - 직접 설치 및 ORM을 통한 간접 조작
            - sqlalchemy: Python에서 sql 기반 dbms를 조작하기 위한 ORM 프레임워크.
    - 실습:
        - Django 실습:
            - django 설치해서 웹 서버 열어보기
        - DBMS 실습:
            1. 어제 cu편의점에서 얻어온 데이터를 정리하기
            2. MySQL 설치
            3. heidisql 설치: 윈도우 11 환경에서 gui를 통해 가시적으로 현재 dbms의 데이터 및 쿼리 확인
            4. sqlalchemy 설치: Python ORM 프레임워크인 sqlalchemy를 통해 db제어.
            5. 정리한 cu편의점의 데이터들을 MySQL안에 'cu'라는 이름의 테이블 안에 집어넣기.
            - 경험한 error:
                - mysql을 public ip를 통해서 붙기 전에 /etc/mysql/ 디렉토리 아래에 있는 설정파일에서 bind_address 설정을 건드려서 접속가능한 ip값을 조정해줄 필요가 있었음.
                - sqlalchemy와 더불어서 mysqlclient를 pip를 통해 설치해줄 필요가 있었음.
- 24.04.10
    - 휴무
- 24.04.11
    - Python Decorator & Closure: 개념 설명 및 예시
    - API: 응용 프로그래밍 인터페이스 개념 설명
        - RESTful API: 서버-클라이언트 간 통신 매커니즘
    - 라벨 인코딩, One-Hot 인코딩: 범주형 데이터의 전산화 과정 개념 설명 및 예시
    - XML 개념 설명
        - XML을 ElementTree를 통해 pandas dataframe으로 변환하는 방법
    - SQL
        - 테이블 생성, DB 생성, 테이블 내용 조회 및 데이터 유형과 쿼리 생성
        - pymysql을 통한 쿼리 입력 및 커밋 방법
    - 실습:
        - cu, seven-eleven, gs25의 데이터프레임을 합쳐보기
        - 각각의 서비스들에 대해서 column을 유지하는 대신 column들을 pandas의 melt 함수를 통해 service라는 단일 column과 여러 row로 분해하기
        - pymysql을 통해 직접적으로 query문을 생성해 db에 테이블을 만들고 데이터프레임을 삽입하기
        - 전기차 API 키를 받아 XML 파일을 데이터프레임으로 분해하기
- 24.04.12
    - MatPlotLib, Seaborn: 데이터시각화 라이브러리
    - Folium: 위도, 경도 값을 받아 시각화한 그래프를 만드는데 사용되는 라이브러리
    - [실습](https://github.com/S0rrow/Playdata_Project02):
        - 지하철 시간대 및 역별 승하차 인원 데이터 전처리
        - 해당 데이터를 mysql DB에 집어넣기
            - Primary Key값은 날짜, 역명, 구분, 시간대로 삼아서 삽입함.
        - 역별 좌표를 받아서 해당 역의 승하차 데이터를 추산해 히트맵 형태로 folium을 통해 나타내기