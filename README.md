## 키워드 기반의 주식 인사이트 제공 플랫폼: Stockey
![image](https://github.com/Pro-Digital-Academy-Frontend-Project/.github/blob/main/asset/1-%EC%9D%B8%ED%8A%B8%EB%A1%9C%ED%8E%98%EC%9D%B4%EC%A7%80.png?raw=true)

## ⁉️기획 배경
테마주와 같은 특정 키워드 기반의 투자 성향에서 아이디어를 시작했습니다.
#### 투자자의 니즈
- 헤비 트레이더: 자신만의 투자 전략과 특정 키워드를 바탕으로 주식 변동성을 분석하는 투자 패턴
- 라이트 트레이더: 숙련된 트레이더의 분석 키워드와 투자 전략에 관심이 높음
#### 기존 서비스의 한계
- 한정된 키워드에 대해 한정된 주식 종목 인사이트만 제공
- 종목 토론방과 달리 키워드 기반의 커뮤니케이션 공간의 부재
#### [Stockey]의 목표
- 사용자의 키워드 자율성 보장
- 키워드와 종목 간의 관계를 시각화 및 랭킹화하여 인사이트 제공
- 키워드 기반의 헤비 트레이더-라이트 유저 연결

<br>

## 🗝️주요 기능 및 UI
- 키워드 기반의 주식 랭킹 및 차트
- 종목 기반의 키워드 랭킹 및 차트
- 키워드 별 채팅방
- 즐겨찾기 키워드/종목 알림 서비스
![image](https://github.com/user-attachments/assets/43bd4a12-c210-4c0d-9745-bb79c952ad9c)
🎥[시연 영상 보러 가기](https://www.youtube.com/watch?v=MWXZM-6tnXA)

<br>

## 🤔구현 방식
1. 스케줄링을 통해 매일 Naver Open API로 종목 별 뉴스 데이터를 가져왔습니다.
2. 뉴스 데이터에서 Kiwi로 토큰화 후, kr-wordrank로 키워드와 키워드-종목 별 가중치를 추출했습니다.
3. 추출한 데이터를 DB에 저장 후 [키워드 별 종목 랭킹], [종목 별 키워드 랭킹], [키워드 별 채팅방] 등을 제공하였습니다.

<br>

## 👍회고
![image](https://github.com/user-attachments/assets/e91226fc-330e-48e9-b785-dc4e7779c8ee)

<br>

## ElasticSearch 성능 향상
<img width="522" alt="스크린샷 2024-12-19 오후 3 06 11" src="https://github.com/user-attachments/assets/3477cb7e-0818-4388-adcc-d1e23fba547a" />
<br>
Node.js의 라이브러리 Artillery를 통해 테스트 결과
요청 응답 속도가 약 80% 향상된 것을 확인할 수 있었습니다
