# IOT 기말 과제
## 현재 위치 기반 길찾기
### 주제 선정 이유
기존 발표 예정이던 2048게임에서 실용적인 주제를 선정하기 위함

---
### 앱 설명
구글 지도를 통해 자신의 위치와 위도,경도,정확도를 파악할 수 있다. 그리고 자신의 위치를 메시지 혹은 다른 어플을 통해 공유할 수도 있다.

또한 길찾기 기능을 통해 현재 위치부터 목적지까지의 경로를 검색 가능

---
### 디자이너
사용한 컴포넌트 : 지도, 수평배치, 레이블, 텍스트박스, 버튼, 목록뷰, 웹뷰어, 전화번호선택, 위치센서, 문자메시지, 알림, 시계, 공유

![디자이너](https://github.com/Lambet12/MyLocation/blob/main/%EB%94%94%EC%9E%90%EC%9D%B4%EB%84%88.jpg)

---
### 블록
![초기](https://github.com/Lambet12/MyLocation/blob/main/%EC%B4%88%EA%B8%B0%20%EC%86%8D%EC%84%B1%20%EB%B8%94%EB%A1%9D.png)

위치 센서의 업데이트 간격을 2초로 지정
목록에 값이 나오기 전 텍스트도 지정

위치 정보의 개수를 1로
위치리스트는 빈 리스트를 만들어 
위치 정보 누적을 하는 변수 생성

---
![위치센서](https://github.com/Lambet12/MyLocation/blob/main/%EC%9C%84%EC%B9%98%EC%84%BC%EC%84%9C%20%EB%B8%94%EB%A1%9D.png)

위치 센서로 위도, 경도, 정확도, 주소 표기

위치 리스트 변수의 빈 리스트를
목록 값을 위한 항목들로 채우기

**정보수)시간/위도/경도**

항목을 모두 입력한 후 목록에 변수 입력

위치 정보의 수는 +1씩 추가해 누적

---
![지도업데이트](https://github.com/Lambet12/MyLocation/blob/main/%EB%B2%84%ED%8A%BC%20%EC%A7%80%EB%8F%84%EC%97%85%EB%8D%B0%EC%9D%B4%ED%8A%B8%20%EB%B8%94%EB%A1%9D.png)

만약 초기에 위치가 보이지 않을 때
클릭하면 사진과 같은 알림이 출력

사용자의 현재 위치 정보가 입력된 후
정상적으로 클릭했다면 총 2번 줌을 해
상세 위치를 표시

길찾기 기능의 공간을 위해서
지도 업데이트로 현재 위치를 사용할 땐
길찾기 뷰어가 보이지 않고
지도가 보이도록 설정

---
![위치전송](https://github.com/Lambet12/MyLocation/blob/main/%EB%B2%84%ED%8A%BC%20%EC%9C%84%EC%B9%98%EC%A0%84%EC%86%A1%20%EB%B8%94%EB%A1%9D.png)

현재 위치를 지도로 저장할 변수 지정

만약 초기에 위치가 보이지 않을 때
클릭하면 사진과 같은 알림이 출력

현재 위치가 입력된 후 클릭을 하면
선택 알림창이 메시지와 함께 출력
문자메시지 / 공유 / 취소 버튼 중
선택하면 각 기능 실행

---
![위치전송알림](https://github.com/Lambet12/MyLocation/blob/main/%EB%B2%84%ED%8A%BC%20%EC%9C%84%EC%B9%98%EC%A0%84%EC%86%A1%20%EB%B8%94%EB%A1%9D.png)

이전 알림에서 선택을 했다면 지도URL 값에
구글 지도 링크와 위도,경도가 합쳐져 입력

문자메시지를 선택했다면 연락처가 나온 뒤
현재위치 (지도) 와 같이 출력되어 전송

공유를 선택했다면 사용자의 어플이 나온 뒤
어플들 중 선택하면 현재위치 (지도) 전송

---
![길찾기](https://github.com/Lambet12/MyLocation/blob/main/%EA%B8%B8%EC%B0%BE%EA%B8%B0%20%EB%B8%94%EB%A1%9D.png)

길찾기 함수를 만들고 출발/도착 변수 생성
실행 시 구글 길찾기 출발지와 도착지 주소 입력


버튼을 클릭하면 함수를 실행해
출발지에는 위치 센서의 현재 주소
도착지는 텍스트 박스의 주소로 길찾기 실행

지도와 마찬가지로 공간을 위해 버튼 실행 시
길찾기 뷰어가 보이고 지도가 보이지 않음

---
### 실행화면
![실행화면](https://github.com/Lambet12/MyLocation/blob/main/%EC%8B%A4%ED%96%89%ED%99%94%EB%A9%B4.png)
