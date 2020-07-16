# 서초 근처 음식점 찾기
> 귀펭(귀여운 펭귄처럼)의 미니 프로젝트
## 프로젝트 결과물
* [오늘 뭐 먹지? - 남부터미널 맛집여지도](https://www.notion.so/94246cbe24d541bd807d2889c2dbe8d3)
* [분석 과정](https://slides.com/seanparkk/title-textfdasf)
* Members: 
  * Soulinj 
  * Sean-Parkk
  * YoonseongHer 
  
- - -
# 프로젝트 설명
## 프로젝트 목적
* Playdata에서 공부하는 학우들에게 맛집을 제공하기 위해 시작
  * 오늘 뭐 먹지? 이 근처에 뭐 있지? 라는 고민을 해결해주기 위한 프로젝트

## 데이터 수집 및 전처리
### 크롤링
* 카카오맵에서 서초-강남 지역 음식점 4,680곳 크롤링
  * Selenium, BeautifulSoup 사용
### 데이터 전처리
* str to numeric
* 결측값 처리
* 특성 추가
  * 위도, 경도
  * 학원에서부터의 직선 거리
  * 도보로 걸리는 시간
* ZMS 지표 계산
  * 맛집 지표를 나타내줄 지표 선정 (ZMS, Zzon Mat Score)
  * 수식: $$ZMS = score * log(eval\_cnt) + log(review\_cnt)$$
## 분석
* 분석 데이터 필터링
  * 평가 4회 이상 받은 곳으로 필터링 (중앙값)
* ZMS의 분포 확인
* 리뷰 정성적 분석, WordCloud기법 활용
* 리뷰 비교/분석
* 연도별 평점 변화 확인
  * 시계열 데이터를 통해 리뷰의 증감 변화 확인
* 최근 3년간 평균 평점, 평가 수 확인 
  * 리뷰조작, 과도한 알바 등 필터링
* 최근 3년 평점 수 변화 모니터링
* 검증 (실사)

