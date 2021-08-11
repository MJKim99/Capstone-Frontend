# 효자손 Andorid application

## 프로젝트 소개
효자손(HyoJason) 애플리케이션은 노년층인 부모님의 건강관리와 부모-자식 간의 간접 소통 지원을 위한 애플리케이션입니다.

집의 내외부에서 발생할 수 있는 다양한 위험 요소에 대해 부모님의 안전을 보장할 수 없고, 주거 상의 물리적 차이로 인해 쉽게 단절될 수 있는 부모-자식 간의 소통 문제를 자연스럽게 개선할 수 있는 방법을 찾기 위한 취지에서 해당 애플리케이션을 구상하였습니다.

1. 집 내부에서는 IoT(Internet of Things) 기기를 이용한 사용자의 이상 행동 탐지를 통해 일상생활 중 신체적인 문제가 발생했다고 판단되는 경우(낙상 사고, 쇼크 등), 이를 신속히 알아냄과 동시에 그에 따른 적절한 조치를 취할 수 있도록 합니다.
2. 애플리케이션을 통한 소통 방법으로는 스냅톡 기능을 활용할 수 있습니다. 기존 메신저와는 달리 간단한 사용법으로 사진 또는 영상(스냅샷)을 신속하게 전송할 수 있습니다. 스마트폰 사용에 익숙치 않은 연령층들에게도 편리한 사용감을 제공합니다.

## 개발 환경
- Kotlin
- Firebase 4.3.5 / -messaging:21.0.1
- Android Studio
- Kakao login API v2 2.0.5

## WBS
![제목 없음](https://user-images.githubusercontent.com/81893393/128988642-3c717699-c45d-4a31-a061-7623630d3047.png)

## DB 명세서 (사용자 정보)
```
* Firebase Realtime Database 사용
	: No-SQL 방식

Users
-	agerange
-	kakaoemail
-	nickname
-	type
-	userid
-	friend
-	chatroom

agerange (연령대) : 카카오 회원 정보에서 자동으로 불러오는 연령대 정보
kakaoemail (카카오 이메일) : 카카오 회원 정보에서 자동으로 불러오는 이메일 정보
nickname (별명) : 고유한 사용자 별명 값
type (부모-자녀 타입) : 부모(P)인지 자녀(C)인지를 나타내는 값
userid (사용자 고유 id) : 카카오 회원 정보에서 자동으로 불러오는 고유 id number 정보
friend (친구 별명) : 친구 추가 한 상대 회원의 닉네임
chatroom (채팅방 이름) : 친구 추가 시 생성되는 채팅방 이름. ‘부모별명-자녀별명’인 고유한 값으로 생성되므로 해당 값을 이용하여 채팅방에 입장할 수 있음
```

## 사용 예
- 카카오 로그인 API를 사용하여 별도의 회원가입 절차 없이 카카오 계정을 이용해 로그인할 수 있다.
- 앱 실행 시 바로 메인화면이 뜨게 되는데, 메인화면에 존재하는 긴급전화 버튼을 이용하여 위급 상황 시 발 빠른 대처를 할 수 잇다.
- 스냅톡 기능을 필수 기능으로만 구성하고, 가독성 좋게 화면을 구성하여 애플리케이션을 사용함에 있어 어려움이 없도록 하였다.
- 스냅톡 기능 내 카메라 기능을 구현함으로써 
- 고유 닉네임을 이용한 간단한 친구 추가 기능을 이용하여 부모 사용자와 자녀 사용자를 연결할 수 있다.
- 부모 사용자의 사고 탐지 시 본 애플리케이션 내 토큰 값을 이용해 자녀 사용자에게 사고 알림이 전송된다.

## 개발 팀
Team Muyaho - Kyonggi university

## 작성자
- Github: [@MJKim99](https://github.com/MJKim99)

---
