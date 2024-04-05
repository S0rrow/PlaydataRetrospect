# Playdata Data Engineering Track 31 Weekly Retrospct
## Week 1
- 24.04.01: 
    - DE 개념 소개
    - 개발 환경 구축: wsl, Ubuntu, python3.10
    - Python 기초: for-loop, list, dict and indexing
- 24.04.02:
    - Linux 명령어 기초: su, ls, vim
    - DNS, TCP/IP, IPv4 등의 간단한 네트워크 개념
    - Jupyter
    - Python: 람다, 형변화, map
    - 웹 크롤링: requests + bs4를 활용한 크롤링 및 file i/o
        - 실습: genie에서 top50위까지 노래 목록을 추출해서 그 노래들의 가사를 .txt 파일로 저장해보기
- 24.04.03:
    - Linux에서 process의 id를 찾고, 백그라운드에서 실행해보기
    - kernel 개념 소개
    - pip를 통한 파이썬 패키지 설치
    - Python venv: virtualenv 모듈을 통한 가상 환경 구축
        - tqdm: progress indication meter package
    - Linux command: mv, rm, cp
    - Python: with 구문을 통한 file i/o, try-except 구문을 통한 예외처리
    - Web Crawling: requests 모듈에서 post 메서드를 통해 서버에 header와 payload를 전달해 비가시적으로 데이터를 받아오기
    - Python Pandas, Selenium: 간단한 소개 및 활용
    - BI 개념
- 24.04.04
    - IP: Private & Public IP 개념
    - Networks: 브로드캐스팅, 서브넷 마스크, ping, netstat
    - Anaconda: 유료라서 무료인 miniconda 사용, 가상환경 구축
    - Python pickle: Python의 데이터구조를 .pkl 파일로 저장하고 불러올 수 있는 패키지
    - Python Pandas & Numpy: 데이터 분석과 연산 패키지. 
    - 실습: 
        - KBO 홈페이지에서 모든 선수들의 정보를 selenium, requests, bs4를 활용해 크롤링하고 csv파일로 저장해보기
        - 각 선수들의 BMI를 계산해보기
- 24.04.05
    - ML: 학습 종류 소개
        - 지도학습, 비지도학습, 강화학습
            - [마르코프 결정과정](https://ko.wikipedia.org/wiki/%EB%A7%88%EB%A5%B4%EC%BD%94%ED%94%84_%EA%B2%B0%EC%A0%95_%EA%B3%BC%EC%A0%95), [벨만-포드 알고리즘](https://ko.wikipedia.org/wiki/%EB%B2%A8%EB%A8%BC-%ED%8F%AC%EB%93%9C_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98)
    - Pandas: Masking, dataframe의 copy와 대입의 차이 
        - masking은 기본적으로 sql에서 where에 해당됨
    - Python 모듈:
        - 실습과정에서 정의한 함수들을 모듈화해보기
    - 실습:
        - 하나은행에서 각 통화별 원화에 대한 환율을 하나은행 홈페이지에서 크롤링해보기
            - requests와 pd를 통해 dataframe으로 html을 변환.
        - kbo 선수들 중 외국인 선수들의 연봉을 원화로 바꿔보기
                1. 연봉에 '달러'가 포함되는 선수들을 masking
                2. 'USD' 통화 코드를 기준으로 하나은행에섯 24.01.02의 환율 가져오기
                3. 연봉을 만원 단위로 변환해 저장하기
        - 위의 실습으로 얻어낸 데이터를 기반으로 평균, 표준편차 및 분산을 계산해보기
        - FTP를 통해 비교적 10000개의 txt 파일의 압축파일을 wsl 내부에 unzip하기. 이후 파일명에 있는 성별정보에 따라서 남자 혹은 여자로 구분해 각각 폴더에 저장하기. 이후 데이터프레임으로 정보를 저장해 파일 내부 값의 평균, 표준편차 및 분산을 계산해보기