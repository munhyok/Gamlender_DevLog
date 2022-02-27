# 날짜 별 개발 노트

# #Gamlender

**프로젝트 시작 : 2020.09.20**

출시 예정인 게임을 달력 형식으로 정리해 사용자들이 한 눈에 보기 쉽게 해주는 앱

## 개발플랫폼

- ~~Xamarin (Android / IOS CrossPlatform)~~

- ~~개발의 속도와 유지보수를 위해 Xamarin을 채택~~

- ~~[https://github.com/lilcodelab/Xamarin.Plugin.Calendar](https://github.com/lilcodelab/Xamarin.Plugin.Calendar) 의 플러그인을 사용예정~~

- 리액트 네이티브(React Native)로 할 예정

- [https://github.com/wix/react-native-calendars](https://github.com/wix/react-native-calendars)

- [https://codinghub.tistory.com/40](https://codinghub.tistory.com/40) 기초 문법

## 핵심 기능

- 출시 예정된 게임을 달력으로 보기 좋게 정리

- 출시 당일에 캘린더 알림 기능

## 추가하고 싶은 기능

- 출시 예정 게임 관련 뉴스 모음

- 인디게임 개발자들이 자신의 게임 출시일을 미리 등록시키는 기능

(추후 업데이트 예정)

## 데이터 수집

게임 출시 일의 정보를 어떻게 가져올 것인가?

- 파이썬을 활용한 크롤링 기법으로 데이터를 수집

- Steam에선 Database(DB)를 제공 중이므로 DB를 활용

## 피드백

- **사용자들이 관심있는 출시 예정 게임의 표시 기능 추가(한눈에 확인가능)**

- **출시 예정 게임의 출시 이후 변경된 사항 및 할인 정보 추가**

- **~~게임 장르별 사용자들을 위한 카테고리 선택란 추가 / 원하는 정보만 찾아보기 쉬움~~**

- **개발자들의 게임이 출시 이후에 추가적인 정보나 이벤트 홍보를 원할 경우 알림을 띄워주거나 그걸 이용해 홍보비(광고비용) 받는 건 어떰 이건 그냥 생각나서 적**

**출시 예정 게임을 받아오는 기본 로직**

![https://lh4.googleusercontent.com/J6Tw8u36GLjZ8RAn0JKrDcqn7lol6g4N75Ha1118cZhJoMw2Z9aW1AtnWUC2CFFFEn_YNaGHBu4MubjGTl6YQNfu0DnFl8RvSls4gJBriWX24QTgOliKC5mCK9Yre_WywM7k75bG=s0](https://lh4.googleusercontent.com/J6Tw8u36GLjZ8RAn0JKrDcqn7lol6g4N75Ha1118cZhJoMw2Z9aW1AtnWUC2CFFFEn_YNaGHBu4MubjGTl6YQNfu0DnFl8RvSls4gJBriWX24QTgOliKC5mCK9Yre_WywM7k75bG=s0)

![https://lh6.googleusercontent.com/SkkU5DpdymdULfnRZxtUDzFN9MNu-05su-762g5QU0hY2JXZdrlNiWKDTMQi8D1Z4KdRGCN6wL2vZ6-pDFL-tyFVUp-Y8eQpukOxNdWdBB6zK0tO59zxCO0WYJgdFkLNWOb3k0-P=s0](https://lh6.googleusercontent.com/SkkU5DpdymdULfnRZxtUDzFN9MNu-05su-762g5QU0hY2JXZdrlNiWKDTMQi8D1Z4KdRGCN6wL2vZ6-pDFL-tyFVUp-Y8eQpukOxNdWdBB6zK0tO59zxCO0WYJgdFkLNWOb3k0-P=s0)

## 2020.09.28 Update Note

Dot : 출시 예정 게임

Line : 스팀,Epic store등의 각종 스토어 할인 기간

현재 해야할 목록

1. ListView (게임 리스트 표시) 혹은 다른 페이지로 넘어가서 표시(stack 네비게이션으로 구현 예정)

2. status bar 숨기기

[https://www.robinwieruch.de/react-native-navigation](https://www.robinwieruch.de/react-native-navigation)

리액트 네비게이션 튜토리얼

난제

- markedDates를 하나의 함수로 불러와 로드를 시켜야할듯하다.

- 크롤링 가공 형식을 JSON으로 해야하나?

- 

## 2020.10.03 Update Note

![https://lh3.googleusercontent.com/miJZxLH1A70mkC5cr6FRfAmpGN2bqGQQ5zx1dgbJRJVgNqWv5Y6IwfhyQQCbPSh3_rGRYaNdcKJ_IIqjDd4E5oVmfLYm6kekb7hZ-7nxF2ZVp9H52y_XzgxlO1xUI4WIHSVoPO4_=s0](https://lh3.googleusercontent.com/miJZxLH1A70mkC5cr6FRfAmpGN2bqGQQ5zx1dgbJRJVgNqWv5Y6IwfhyQQCbPSh3_rGRYaNdcKJ_IIqjDd4E5oVmfLYm6kekb7hZ-7nxF2ZVp9H52y_XzgxlO1xUI4WIHSVoPO4_=s0)

레이아웃 및 트리식으로 구조 정리

![https://lh6.googleusercontent.com/VX-NldoQW6e3XVbXu-BifpNvicaX2d2z3TJnruyX6G2THl8HwrxVHColpvyaEYb027V6t7LsqLdY0UzLFrdv0TyRCxMtCgSU5F_40wD5jsvVzhkSfidmo3R-X--6lDWEZbDOpyvt=s0](https://lh6.googleusercontent.com/VX-NldoQW6e3XVbXu-BifpNvicaX2d2z3TJnruyX6G2THl8HwrxVHColpvyaEYb027V6t7LsqLdY0UzLFrdv0TyRCxMtCgSU5F_40wD5jsvVzhkSfidmo3R-X--6lDWEZbDOpyvt=s0)

상단 캘린더 하단 FLATLIST 추가

![https://lh4.googleusercontent.com/Te9deo0muxjZOXMCHS3rdGEP00ZArI_YIjo_qjaDwifwu7su2UI3yp_9CLI2Onj-zVmkPW6xAp-CKxAamAgoukkLv5AYVty4bPYIIyjJVQEz2s4g8AqAZgBl2DbySywqZCL6m0_z=s0](https://lh4.googleusercontent.com/Te9deo0muxjZOXMCHS3rdGEP00ZArI_YIjo_qjaDwifwu7su2UI3yp_9CLI2Onj-zVmkPW6xAp-CKxAamAgoukkLv5AYVty4bPYIIyjJVQEz2s4g8AqAZgBl2DbySywqZCL6m0_z=s0)

2020.10.05 리스트 디자인 중

서버에서 JSON으로 받아와서 리스트화 시킬 것

조만간 코드 다 갈아엎어버릴 예정

**구현 목록**

1. ~~리스트 디자인(기본 디자인)~~

2. ~~달력 날짜 클릭 시 해당 날짜에 있는 리스트 정보 불러오기~~

3. ~~리스트에 있는 게임 클릭 시 디테일 화면으로 넘어가기~~

4. ~~크롤링한 데이터를 달력에 적용하기~~

5. ~~디테일화면 재구성~~

6. ~~UI & UX 리디자인~~

## 2020.10.05 Idea List

1. Details페이지는 직접 만들지 않고 각 게임의 상세정보 링크로 이동

물론 인터넷 앱으로 넘어가는 것이 아닌 WebViewer를 이용할 예정

ex) steam게임이면 스팀링크로 바로 이동

## 2020.10.06 UpdateNote

### Update

- 리스트를 클릭 시 상세페이지로 즉시 이동

![https://lh3.googleusercontent.com/Vi_TeyM95hKkfoHpbElgvXQgqJ_u027WNg6nVSDZFCYzt5cbO68d2Ho8Ug5dO1sX3FLvMz6P4Vm0_ahfsyduNElT_au9w_17SSRBtcVHt_WZpRqLVRaPX7K93CnWZPlj1YHS8OwT=s0](https://lh3.googleusercontent.com/Vi_TeyM95hKkfoHpbElgvXQgqJ_u027WNg6nVSDZFCYzt5cbO68d2Ho8Ug5dO1sX3FLvMz6P4Vm0_ahfsyduNElT_au9w_17SSRBtcVHt_WZpRqLVRaPX7K93CnWZPlj1YHS8OwT=s0)

## 2020.10.10 UpdateNote

### (UI & UX) Idea

![https://lh6.googleusercontent.com/HHwN8uByMQcUuZnae6lOtifs55386xcH0cVSoyvsN97Gt4A5MbRgLdFrDc5auARAlX-QgujZK-KU1aAbeChmIB4ZGRfwK42zSgPm1bh0PG352k9OAZn6S0C6aMa_KDppkJxrpor4=s0](https://lh6.googleusercontent.com/HHwN8uByMQcUuZnae6lOtifs55386xcH0cVSoyvsN97Gt4A5MbRgLdFrDc5auARAlX-QgujZK-KU1aAbeChmIB4ZGRfwK42zSgPm1bh0PG352k9OAZn6S0C6aMa_KDppkJxrpor4=s0)

## 2020.10.11 Update Note

### Idea List (서버 방향성)

- JSON으로 날짜, 게임이름, 플랫폼, 상세페이지까지 정보를 가져온다

원래는 세부적으로 나누고 싶어 년도 > 월 > 일 순으로 디렉토리를 할 예정이였으나 JSON 구조가 복잡해지므로 유지보수에서 불리해져 YYYY-MM-DD로 받아올 예정

Reference Source ([prod.danawa.com/game](http://prod.danawa.com/game/))

Calendar의 형식과 동일하게 날짜는 YYYY-MM-DD식으로 받을 예정

- 게임일정이 없는 날짜도 받아와야하는데 이유는 추후에 넣을 기능인 인디게임등록 서비스를 위해 모든 날짜를 받아와야한다. 그리고 JSON에 직접 기입으로 패치를 하든 프로그램을 제작해서 JSON에 업데이트 가능하게 할 예정

- JSON 서버를 어디다가 할까 생각을 해본 결과 일단 정식 앱 출시 전까진 본체 컴으로 서버를 만들고 추후에는 JSON서버 호스팅 서비스를 활용할 예정

## 2020.10.14 Update Note

### Update

- JSON서버와 연결해 달력의 날짜를 클릭하면 서버에서 게임 리스트를 불러오는 방식으로 개편

- 코드를 갈아엎느라 navigation을 다시 작업해야함

![https://lh3.googleusercontent.com/q2S5eUo9z95rz_p3CR2jUqVtPUxYD1Uzr1Mkzt7qzst2nl7YL6iTz2a8GWzMPsdB2pKUbLzz_up2pWbOEJQc7ZcK0wI1XxPVC45pFyCSmJz0gM8XKzddEFvSQ2iZ_BM-eeQoLXme=s0](https://lh3.googleusercontent.com/q2S5eUo9z95rz_p3CR2jUqVtPUxYD1Uzr1Mkzt7qzst2nl7YL6iTz2a8GWzMPsdB2pKUbLzz_up2pWbOEJQc7ZcK0wI1XxPVC45pFyCSmJz0gM8XKzddEFvSQ2iZ_BM-eeQoLXme=s0)

각 날짜별로 게임 리스트를 불러오는 작업 완료

## 2020.10.16 Update Note

### 버그 FIX

- 달력 도트가 제대로 렌더링이 되지않는 오류 수정

- Navigation 버그 재 수정완료

- 

### 보고 된 버그

- 아이폰에서 달력의 월을 계속 바꾸거나 날짜를 클릭하는 등 특정 이벤트에서 오버플로우 발생

- 

### 결정 사항

- 인디게임 개발자들을 위한 게임 등록 서비스의 비용을 생각해보았으나 최종적으로 무료로 결정

- 

## 2020.10.20 Note

- Scroll View로 할 예정인데 각각의 헤더의 역할을 정해야한다.

- SectionList로 추후 각 플랫폼을 섹션별로 구별해 분류한다.

(SectionList로 할 경우 DB수정 필요)

## 2020.10.22 Update Note

### 버그 FIX

- 아직 없음

- 

### 보고 된 버그

- 오버플로우 발생

- 예외처리 NaN등..

### 추가 된 점

- 리스트를 카드 형식으로 띄웠고 이미지 띄우기 까지 완료

- 달력 리프레시를 하기위한 엑티비티 인디케이터 생성

- GIF

![https://lh5.googleusercontent.com/oLHWGIII5GzW-tCstlQgKfrhq-QesIRpANvv4z-7IvDpwNHoLKm-BO0fEgciWbGkgmLBinrVwk-pAUbRLCfU0DF64VqtAdDP7y2Stp7igcprFQb3lBujcMdNrC7tAFD4FWbF04n_=s0](https://lh5.googleusercontent.com/oLHWGIII5GzW-tCstlQgKfrhq-QesIRpANvv4z-7IvDpwNHoLKm-BO0fEgciWbGkgmLBinrVwk-pAUbRLCfU0DF64VqtAdDP7y2Stp7igcprFQb3lBujcMdNrC7tAFD4FWbF04n_=s0)

## 2020.10.24 Update Note

### 버그 FIX

- 서버 및 네트워크 연결 관련 예외처리 전부 완료

- 여전히 버그가 존재하지만 로딩하는 딜레이를 0.6초 정도 주어 1분 이상 광클해야 뜨게 만들어 둠

### 보고 된 버그

- 캘린더 터짐 버그도 여전하다…

- 

### 추가 된 점

- 예외처리 메시지(서버관련)

- 

## 2020.10.28 Update Note

### 버그 FIX

- 아직 없음

### 보고 된 버그

- 아직 없음

### 추가 된 점

- 상세페이지 초안 디자인 완료

## 2020.11.19 Note

### 아이콘 추가

- 아이콘 추가를 벡터 아이콘을 불러와서 할 지 이미지로 할 지 고민중

물론 벡터 아이콘으로 할 시 매우 편함 태블릿같은 크기에도 화질이 깨지지 않는다.

추후 아이패드, 갤럭시탭으로 태블릿 UI 호환성 테스트

- 기종별로 번호를 부여해 숫자 조합으로 아이콘을 생성할 예정이다

PS = P 1

XBOX = X 2

NS= N 3

PC = C 4

1,2,3,4 = 4개

12,13,14,23,24,34 = 6개

123,124,134,234 = 4개

1234 = 1개

이런식으로 분류해서 아이콘 코드를 DB에 등록할 예정

### 전체적인 개발 프로세스 진행 정리

- 개발이 많이 지체되었다. 이번 주내로 디자인 개선을 해야함

- 설명글 디자인을 어찌해야할지 난감하다,,, 링크를 넣으려고 했지만 상세 링크를 일일이 수동적으로 끌어오기엔 너무 난감… 크롤링으로 되려나?

- 서버는 그냥 라즈베리파이로 Linux서버로 해도 충분 할 것 같다는 생각을 했다. 초반엔 유저도 잘 없을거고 큰 리소스를 먹지도 않을 것같아서 그렇긴한데 네트워크 보안이 걱정 추후에 유저가 1만명 돌파하면 FireBase로 넘어갈 예정 미리만들어 놓자…

- REST API에 규격에 맞게 DB를 재 수정해야한다… 하필 뒤늦게 발견해서..

- 라즈베리는 구매 후 팀뷰어와 연동하고 Node.js(NPM) 설치 후 Json Server설치 추후 크롤링 봇도 제작하면 DB에 PUT 하는 형식으로 파이썬으로 한번 만들어 볼까 생각중이다.

- 일단 손수 데이터를 수집해서 해서 앱에 반영시키는 걸로...

- 알람기능은 출시하고 1차 업데이트로 한 번 해보는걸로

- 사업자 등록은 언제하니? 얼른하자

- 다음엔 Expo가 아닌 Init으로 개발해보자

- Widget

## 2020.11.21 Idea Note

### 출시 이후 겜린더의 방향성

- 과거의 게임 잡지 개념을 살려 월간 인디게임 리스트를 정리시켜 동영상 광고로 가볍게 볼 수 있게 만든다. 게임 잡지를 기획해보는 것으로 잡는다. (잡지 서비스) 해외 인디 게임 회사들과도 컨텍을 통해 잡지에 등록을 시도해본다.

## 2020.12.06 Update Note

### 추가 된 점

- 기존 상세페이지를 제거하고 빠른 반응성을 위해 Modal UI를 적용시킴

### 난제

- Modal Popup에 데이터를 불러와야하는데 기존 Stack Navigation 방식하고 다르고 관련 레퍼런스 부족

- 그렇다고 기본 React에서 제공하는 Modal를 쓰기엔 너무 부족한 기능들이 많다

- 

### 우선 순위

1. ~~Modal Popup Design~~ ~~(이놈이 빨리끝나야한다…)~~

2. Notification

3. Admob

4. DB 작업

5. 서버 구축

    

    ![https://lh5.googleusercontent.com/S0coD37B4-So5DD9OA3xEO0F91gp9kp-lhC16EZl8eK5RSYV2J6FR4ptLowz-K7UtYCCKHTq9RZXhnYzEfCceDu1F0dA8C2tYxNG6W7WCZK-TfF2wL-EA3cqrW-lnWxi6EQXlI0C=s0](https://lh5.googleusercontent.com/S0coD37B4-So5DD9OA3xEO0F91gp9kp-lhC16EZl8eK5RSYV2J6FR4ptLowz-K7UtYCCKHTq9RZXhnYzEfCceDu1F0dA8C2tYxNG6W7WCZK-TfF2wL-EA3cqrW-lnWxi6EQXlI0C=s0)

    

## 2021.01.02 Develop Note

### 추가 된 점

- 테마 변경 (다크)

- 플랫폼 아이콘 추가 - 드디어!

- Header 제거

- 전체적인 폰트 컬러 개선 (가독성 강화 및 배경 동화)

### 난제

- 상세페이지 디자인…(어떻게 정갈하고 알차게 해야 할지 모르겠다…)

- 이미지 삽입(이미지를 넣고싶은데 그럼 DB에 따로 이미지 링크 및 DB 재설계 필요…)

- 

### 우선순위

- 상세페이지 디자인(상세 정보 좀.. 누가 구원해줘…)

- Push Notification (푸시알림기능 추가! 미리 정의 좀 내리고 진행…)

- AdMob(하단 배너 광고 삽입)

- DB 작업(재 작업 필요)

- 서버 구축(네트워크 부터 해서 라즈베리 구매 후 작업 할 예정 FTP...tlqkf)

- APP favicon(앱 아이콘 디자인!)

    

    ![https://lh6.googleusercontent.com/CnyX--6Zi08W2e4qKzAilZsvH7FXE95sZR6aKi6zlksu1a5TuNIaDNxRImv73cExfLSUBcMiFoza7QpEF4IFHzFE5EPEYY0tJJSsVWgSFCAia0zhyd954iyBG6Dlg330jnGL-b_0=s0](https://lh6.googleusercontent.com/CnyX--6Zi08W2e4qKzAilZsvH7FXE95sZR6aKi6zlksu1a5TuNIaDNxRImv73cExfLSUBcMiFoza7QpEF4IFHzFE5EPEYY0tJJSsVWgSFCAia0zhyd954iyBG6Dlg330jnGL-b_0=s0)

    

## 

![https://lh3.googleusercontent.com/G1FEUK2D6A1DrdXSXLhGddSESkiMUu1yfOA2qqzeJI99AywIxI-RQtnbHoRiK723gj9gz19B6xUn2tDjFGhNQ2kfKf12zVHHpiSMN6ik9BuZHglNU_VCVtROe2zx9KOk6bOjF9Lf=s0](https://lh3.googleusercontent.com/G1FEUK2D6A1DrdXSXLhGddSESkiMUu1yfOA2qqzeJI99AywIxI-RQtnbHoRiK723gj9gz19B6xUn2tDjFGhNQ2kfKf12zVHHpiSMN6ik9BuZHglNU_VCVtROe2zx9KOk6bOjF9Lf=s0)

## 2021.01.12 Develop Note

### 추가 된 점

- Image Slider 추가 완료 예외 처리 완료

- 캘린더 도트색상, 폰트, 날짜 색상 변경완료

### 난제

- 도트없는 날짜 눌렀을때 없다는 예외처리 필요

~~빈 화면만 나오면 안드로이드에선 상단바 상태가 풀리는 것이 확인~~

- custom backbutton ios 전용으로 따로 뒤로가기 버튼이 필요

### 우선순위

- ~~서버~~

- ~~Admob~~

- ~~나머지 버그 Fix~~

- ~~Push notification~~

- ~~FTP Image Server를 구축하게 되면 라즈베리로 이미지 로딩 트래픽 감당이 가능할 지 의문..~~

- ~~분산으로 처리 Json은 라즈베리 Image는 별도의 호스팅 이용~~

- ~~스플래쉬 이미지, App Icon 제작(FAVICON 포함)~~

## 

![https://lh4.googleusercontent.com/oyQBz_OBMy4aTy88zpNXOjhUfMR5rEja8-EF_MlIySW4JtBcKIdyv-Tk5zKde6fwZW1qmZunubTL7zSvd-nPpp3LMC_yJDxkfo0Njg2pfLvKaJ93oVeLpX9U7AWw43NVR4Xv47WT=s0](https://lh4.googleusercontent.com/oyQBz_OBMy4aTy88zpNXOjhUfMR5rEja8-EF_MlIySW4JtBcKIdyv-Tk5zKde6fwZW1qmZunubTL7zSvd-nPpp3LMC_yJDxkfo0Njg2pfLvKaJ93oVeLpX9U7AWw43NVR4Xv47WT=s0)

## 2021.03.17 Develop Note

### 추가 할 점

- Youtube / 공식 홈페이지 바로가기 링크 추가

- 게임 추가… (누가 이거 좀 대신…)

- Apple iOS14 광고 정책 Admob 업데이트~~(망할 애플)~~

- 날짜를 누르면 동그라미로 표시해주기(이건 추가하려고 했으나 오류)

### 계획

- 겜린더가 어느정도 자리를 잡게 되면 추후 매거진 컨텐츠를 추가할 예정

어떤 식으로 할 지는 고민 중이고 1달에 1번 감각적인 글을 쓰면서 게임을 좋아하는 사람 즉 약간 MD(?)느낌의 역할을 해줄 사람이 필요… (과연 있을까…?)

수익 모델 : 해당 매거진을 보려고 할 때 동영상 광고 1회 재생 후 매거진 시청

주 내용 : 겜린더에 출시 등록되어있는 인디 게임들을 주로 다루게 될 듯한데 이 부분은 인디게임 회사들과 협업해서 해야할 부분인 것 같다(미리 데모 버전을 받고 플레이 하는 방식으로) 그 다음 플레이 이후 어떤 느낌이었는지 와 솔직한 리뷰 등을 작성 할 예정 (글을 읽는 유저들에겐 얼리엑세스라는 것을 매거진 초반에 작성해 무조건 인지시킬 예정

그 이외에도 기대되는 작품들을 글 작성자 관점에서 리뷰해보는 내 느낌대로 리뷰(?) 하는 식으로 해볼 예정

- 겜린더를 솔직히 혼자 개발하고 혼자 운영하기 힘들 것 같음… 추후 팀원을 구하는 방향으로 뭔가 잡아야할 듯 하다…

## 2021.03.25 Update Note

### 겜린더 드디어 플레이스토어에 정식으로 등록 완료!

### 해야할 것

- 마케팅 : 현재 인디 게임 개발 갤러리 같은 곳에 올렸지만 전혀 반응이 없음…

    - **마케팅 전략을 어떻게 세울 것인가?**

    - 일단 커뮤니티에 홍보를 끝냈으니 광고를 직접 영상으로 만들어보고

아는 유튜버 분들께 광고를 부탁드릴 예정(이건 기능이 좀 업데이트 됐을때…)

- Admob / youtube / Facebook / Twitter 세개로 적극적으로 광고를 때려야 할 것으로 보임

- SNS 소통도 생각중인데 여기는 꾸준히 업데이트 노트나 새로운 인디게임이 등록되었을때 홍보의 창구로 쓸 생각

- 트위터에 생각보다 인디게임개발하시는 분이 정말 많은데 이분들하고 직접 연락을 해보거나 트친소 스타일로 거부감 없게 개발자 분들께 다가갈 수 있는 방법을 생각해내야 할 것 같음

- 꾸준한 업데이트 : 게임을 꾸준히 업데이트하고 유저들의 피드백을 적극적으로 받아야할 때

    - **업데이트 목록**

    - 유튜브 트레일러 영상 링크

    - 필터링

    - 푸시 알림 기능(게임 출시 할 때 알림이 올 수 있게 할 예정)

    - 킬러 컨텐츠 제작 (저번에 작성했던 매거진 느낌의…)

    - 

### Issue

- 현재 플레이 스토어에 검색이 안됌(이건 시간이 지나면 자연스럽게 해결된다고 하는데 …)

- 플레이 스토어에서 삭제 시 플레이 스토어에 등록하지 않은 앱이라고 뜸 (이것도 위와 원인이 비슷할 것으로 예상 중)

- iOS에도 등록을 해야하는데 등록 과정이 상당히 까다로운 것으로 보임… (잘 못하면 맥북이 필요할 지도…?)

## 2021.03.28 Note

### 해야 할 것

- 에픽 스토어, SteamDB 정보 데이터 클리닝 진행

- 크롤링 툴 만들어서 1주일에 한 번씩 게임 정보 받아오기 Python

자동화가 필요할까? = No 굳이 필요 없음 한 번 크롤링해서 클리닝하는 것에 집중하는걸로..

- 겜린더 바로가기 버튼 업데이트 필요

겜린더가 현재 유튜브 트레일러 보기 기능과 공식홈페이지로 들어가는 기능이 존재하지 않는다.

유튜브 트레일러, 공식 홈페이지, 개발자 SNS 이렇게 3개 설명글 하단에 아이콘 출력

- 게임 컨텐츠 부족

해당 문제는 위에 에픽 스토어, SteamDB 정보 그리고 인디게임 개발자분들한테 더욱 더 홍보해야 할 느낌… 지금 상태는 겜린더가 경쟁력이 하나도 없음…

- 인디 개발자 모집

인디 개발자를 어떻게 모집을 해야할 까… 좀 더 치열하게 고민할 필요가 있어보임

- Admob 광고

Admob 광고를 위한 포토샵 이미지 작업이 필요할 것 같다…

아마 UI UX를 강조한 3D 레이어 구조 형식의 광고 이미지를 만들 것 같은데… Admob을 한 후에 Facebook으로 추가로 이어서 하는 걸로… 하자…

- 예전부터 오류가 터졌었던 달력 오버플로우 현상…

이것 또한 더욱 더 치열하게 고민해야하고 광클 방지를 위한 대책마련을 해야할듯

- 스팀 세일 목록을 어떻게 데이터화 시킬지 또 고민해야함…

예를 들어 봄 세일이면 겜린더 키자마자 공지 사항으로 바로 뜨게 만든다던지 그런식으로 바로바로 소비자가 볼 수 있게 해야함 그게 가장 경쟁력이 있을 것 같음

세일 목록 정리는 좀 더 어떻게 좋은 UI UX로 표현할 지 고민해야하고

간단한 기간세일은 모니터링하다가 나오면 겜린더에 즉시 업데이트

- Push Notification 꼭 넣기

게임 출시 일이 있는 날짜는 하루에 2번 정도 푸시 알림을 넣어주는 기능 마련

푸시 알림을 받기 위한 동의서도 앱 실행때 받아야함...

## 2021.07.10 Update Note

### 추가 된 점

- Expo에서 RN-CLI로 변경

    - 덕분에 전체적인 퍼포먼스 개선 및 최신 안드로이드 API 적용

- 메인 페이지 좌측 상단 메뉴 버튼 추가

    - 겜린더와 공지사항을 나눔 추후 계속 세분화 시킬 예정

    - 메인 페이지 하단은 “Live Event”를 추가할 예정

- 상세 정보 페이지에 게임 트레일러 영상 확인 가능

    - 영상이 없으면 기존 대표 이미지 출력

    - 영상의 품질은 데이터 절약 및 버퍼링을 줄이기 위해 가장 최저로 설정

**추후 영상을 터치하면 유튜브로 바로 이동할 수 있게 기능 추가 예정**

- webm형식으로 받고 싶으나 현재 라이브러리에서 지원을 안 함

![https://lh5.googleusercontent.com/krwLJfYSBBZlst6i8x-xUw60cxDNScf5-YOiVGMldJuKFbhXGVnxxCI-o2O4Zc44Ecy4Lb_s22Cbawvcs19aP9Tclxvp7WulSGzuXlpi_ZfYZMPM-wJbObAUxqq3xc3W-PuNKkFt=s0](https://lh5.googleusercontent.com/krwLJfYSBBZlst6i8x-xUw60cxDNScf5-YOiVGMldJuKFbhXGVnxxCI-o2O4Zc44Ecy4Lb_s22Cbawvcs19aP9Tclxvp7WulSGzuXlpi_ZfYZMPM-wJbObAUxqq3xc3W-PuNKkFt=s0)

![https://lh4.googleusercontent.com/uNiXbHdLY-0m--EF2H7A_k9h0OyulXnSVoSLLeK2-f0dCYplFlZMZ4T0zczI9AY706azoq1gCKFsll7wJzD0n6vFw92EvHOZ9UDxIeUtyfPSswZ92awX4otGlWZtjFYIFMzAkgCb=s0](https://lh4.googleusercontent.com/uNiXbHdLY-0m--EF2H7A_k9h0OyulXnSVoSLLeK2-f0dCYplFlZMZ4T0zczI9AY706azoq1gCKFsll7wJzD0n6vFw92EvHOZ9UDxIeUtyfPSswZ92awX4otGlWZtjFYIFMzAkgCb=s0)

### 해야할 것

- 위에서 언급한 트레일러 영상 터치 시 유튜브 바로 이동

- iOS 14 대응 Admob추가

- 크롤링 머신 만들기

- 새로운 UI & UX 공부 및 연구
