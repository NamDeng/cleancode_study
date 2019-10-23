# 코딩 규칙

## 1장. 깨끗한 코드 [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter01.md)

- 깨끗한 코딩의 의미, 동기부여 :)

<br/>

## 2장. 의미있는 이름

1. **변수, 함수, 클래스의 이름은 다음 내용을 포함하도록 하자 : 22p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter02.md#%EC%9D%98%EB%8F%84%EB%A5%BC-%EB%B6%84%EB%AA%85%ED%9E%88-%EB%B0%9D%ED%98%80%EB%9D%BC)
    - 존재 이유, 수행 기능, 사용 방법
2. **이름만 구분하지 말고 개념을 구분하도록 하자 : 24p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter02.md#%EC%9D%98%EB%AF%B8-%EC%9E%88%EA%B2%8C-%EA%B5%AC%EB%B6%84%ED%95%98%EB%9D%BC)
    - 이와같이 사용 안됨 - ProductInfo, ProductData
3. **이름의 크기는 범위의 크기에 비례해야 한다 : 28p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter02.md#%EA%B2%80%EC%83%89%ED%95%98%EA%B8%B0-%EC%89%AC%EC%9A%B4-%EC%9D%B4%EB%A6%84%EC%9D%84-%EC%82%AC%EC%9A%A9%ED%95%98%EB%9D%BC)
    - 패키지 범위에서 사용되는 상수의 이름
    - `contst int WORK_DAYS_PER_WEEK = 5`
4. **접두어 사용 안함 : 29p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter02.md#%EC%9D%B8%EC%BD%94%EB%94%A9%EC%9D%84-%ED%94%BC%ED%95%98%EB%9D%BC)
    - sProduct → X

    4-1) 인터페이스

    - 접두어 I 나 구현에서 impl은 사용하지 않는다.
    - 상황에 따라 impl은 사용한다. 
    → 예) 다형성으로 쓰려는게 아니라 내부 속성을 감추려고 인터페이스를 쓰는 경우에는 구현체와 이름이 같아져서 Impl을 쓸 수 밖에 없다.
    - 인터페이스가 리스너로 쓰일 때는 앞에 On을 붙여준다. 메서드는 on을 붙여준다.
5. **축약형 변수명, 짧은 변수명 쓰지 않기 : 31p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter02.md#%EC%9E%90%EC%8B%A0%EC%9D%98-%EA%B8%B0%EC%96%B5%EB%A0%A5%EC%9D%84-%EC%9E%90%EB%9E%91%ED%95%98%EC%A7%80-%EB%A7%88%EB%9D%BC)
    - u, x 등등
    - 5줄 이내에서 순서에 관한 i j k 는 괜찮음
6. **클래스 이름 : 32p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter02.md#%ED%81%B4%EB%9E%98%EC%8A%A4-%EC%9D%B4%EB%A6%84)
    - 명사나 명사구를 사용할 것
    - 동사는 사용하지 않을 것
7. **메서드 이름 : 32p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter02.md#%EB%A9%94%EC%84%9C%EB%93%9C-%EC%9D%B4%EB%A6%84)
    - 동사나 동사구를 사용할 것
    - 접근자, 변경자, 조건자는 get, set, is를 붙일 것
8. **기발한 이름 사용하지 말 것 : 32p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter02.md#%EA%B8%B0%EB%B0%9C%ED%95%9C-%EC%9D%B4%EB%A6%84%EC%9D%80-%ED%94%BC%ED%95%98%EB%9D%BC)
9. **한 개념에 한 단어를 사용할 것 : 33p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter02.md#%ED%95%9C-%EA%B0%9C%EB%85%90%EC%97%90-%ED%95%9C-%EB%8B%A8%EC%96%B4%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%9D%BC)
    - fetch, retrieve, get → 하나로 통일
    - controller, manager, driver → 하나로 통일
    - 지금 당장은 가시적이지 못하니 코드리뷰 하면서 이러한 사항이 있을 때 통일하자.

    9-1) 서버에서 데이터 가져오는 경우 

    상위 개념 계층을 따라서 사용하자 Load → request → get

10. **해법 영역에서 가져온 이름을 사용하자 : 34p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter02.md#%ED%95%B4%EB%B2%95-%EC%98%81%EC%97%AD%EC%97%90%EC%84%9C-%EA%B0%80%EC%A0%B8%EC%98%A8-%EC%9D%B4%EB%A6%84%EC%9D%84-%EC%82%AC%EC%9A%A9%ED%95%98%EB%9D%BC)
    - 전산용어, 알고리즘, 패턴 이름을 사용
    - 도메인 용어는 사용하지 말자.
11. **문제 영역에서 가져온 이름을 사용하자 : 34p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter02.md#%EB%AC%B8%EC%A0%9C-%EC%98%81%EC%97%AD%EC%97%90%EC%84%9C-%EA%B0%80%EC%A0%B8%EC%98%A8-%EC%9D%B4%EB%A6%84%EC%9D%84-%EC%82%AC%EC%9A%A9%ED%95%98%EB%9D%BC)
    - 전산용어나 적절한 용어가 없을 땐 일반적으로 사용되는 용어를 사용하자
12. **변수명에 의미있는 맥락을 추가하자 : 35p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter02.md#%EC%9D%98%EB%AF%B8%EC%9E%88%EB%8A%94-%EB%A7%A5%EB%9D%BD%EC%9D%84-%EC%B6%94%EA%B0%80%ED%95%98%EB%9D%BC)
    - firstName, lastName, Street가 결국 주소를 나타낸다면 addrStreet처럼 맥락을 추가하자.
    - 클래스로 만들면 더 좋다.
13. **불필요한 맥락을 없애자 : 37p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter02.md#%EB%B6%88%ED%95%84%EC%9A%94%ED%95%9C-%EB%A7%A5%EB%9D%BD%EC%9D%84-%EC%97%86%EC%95%A0%EB%9D%BC)
    - 시스템 이름 등을 클래스 이름에 넣지 말자
14. **표준 명명법을 사용하자**
    - Decorator 패턴을 사용했다면 - AutoHangupModemDecorator
    - 예를 들어 자바에서 객체를 문자열로 변환하는 함수는 toString을 많이 씀.
15. **모델 클래스의 이름은 Post나 Put에서 응답 받는 경우가 모두 사라지기 전에는 응답 모델에 Get을 붙인다.**

    → 추후 Get을 삭제했을 때 각 API의 최상위 모델에만 Response를 붙인다.

<br/>

## 3장 함수

1. **작게 만들것 :42p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter03.md#%EC%9E%91%EA%B2%8C-%EB%A7%8C%EB%93%A4%EC%96%B4%EB%9D%BC)
    - 들여쓰기 수준은 2단 이내로..
2. **함수는 한가지만 하자 : 44p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter03.md#%ED%95%9C-%EA%B0%80%EC%A7%80%EB%A7%8C-%ED%95%B4%EB%9D%BC)
3. **서술적인 이름을 사용하자 : 49p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter03.md#%EC%84%9C%EC%88%A0%EC%A0%81%EC%9D%B8-%EC%9D%B4%EB%A6%84%EC%9D%84-%EC%82%AC%EC%9A%A9%ED%95%98%EB%9D%BC)
    - includeSetupAndTeardownPages
        - 함수 구현에서 순서의 지시가 필요한 경우에 사용하자.
        - 함수 세개 이상은 서술하지 말고 추상화 단어를 생각 해 보자.
4. **함수 인수 : 50p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter03.md#%ED%95%A8%EC%88%98-%EC%9D%B8%EC%88%98)
    - 4개 이하로 제한해 보자.
    - 코드리뷰시 케이스 발견하면 해결 방법과 같이 고민해 보자.
5. **플래그 인수를 사용하지 말자 : 52p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter03.md#%ED%94%8C%EB%9E%98%EA%B7%B8-%EC%9D%B8%EC%88%98)
6. **출력 인수를 사용하지 말자** 
7. **부수 효과를 일으키지 말 것 : 54p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter03.md#%EB%B6%80%EC%88%98-%ED%9A%A8%EA%B3%BC%EB%A5%BC-%EC%9D%BC%EC%9C%BC%ED%82%A4%EC%A7%80-%EB%A7%88%EB%9D%BC)
    - checkPassword 함수에서 Session을 초기화 한다거나 노노
    - 함수명이 checkPasswordAndInitializeSession이 될 수는 있다.
8. **명령과 조회를 분리하자 : 56p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter03.md#%EB%AA%85%EB%A0%B9%EA%B3%BC-%EC%A1%B0%ED%9A%8C%EB%A5%BC-%EB%B6%84%EB%A6%AC%ED%95%98%EB%9D%BC)
    - 수행하거나, 답하거나
    - 정 분리할 수 없는 경우 createOrGet 과 같이.
9. **오류 코드보다 예외를 사용하자 : 57p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter03.md#%EC%98%A4%EB%A5%98-%EC%BD%94%EB%93%9C%EB%B3%B4%EB%8B%A4-%EC%98%88%EC%99%B8%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%9D%BC)
10. **중복 코드는 제거하자 : 60p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-08-28%20Chapter03.md#%EB%B0%98%EB%B3%B5%ED%95%98%EC%A7%80-%EB%A7%88%EB%9D%BC%EC%A4%91%EB%B3%B5-%EC%BD%94%EB%93%9C%EB%A5%BC-%EC%97%86%EC%95%A0%EC%9E%90)
11. **사용하지 않는 함수는 제거하자.**

<br/>

## 4장 주석

- 기본적으로는 주석을 최대한 쓰지 말자.

**좋은 주석** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-04%20Chapter04.md#4%EC%9E%A5-%EC%A3%BC%EC%84%9D)

    법적인 주석 : 70p
    정보를 제공하는 주석 : 71p
    의도를 설명하는 주석 -> 실제 정책에 의한 의도를 코드로 표현할 수 없을 때 : 71p
    의미를 명료하게 밝히는 주석 : 72p
    결과를 경고하는 주석 : 73p
    TODO 주석  : 74p
    중요성을 강조하는 주석 75p
    공개 API에서 Javadocs

**나쁜 주석**

    주절거리는 주석
    같은 이야기를 중복하는 주석
    오해할 여지가 있는 주석
    의무적으로 다는 주석
    이력을 기록하는 주석
    있으나 마나 한 주석
    무서운 잡음
    함수나 변수로 표현할 수 있다면 주석을 달지 마라
    위치를 표시하는 주석
    닫는 괄호에 다는 주석
    공로를 돌리거나 저자를 표시하는 주석
    주석으로 처리한 코드
    HTML 주석
    전역 정보
    너무 많은 정보
    모호한 관계
    함수 헤더
    비공개 코드에서 Javadocs

<br/>

## 5장. 형식 맞추기

1. **500줄 미만 대부분 200줄 미만 : 96p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-04%20Chapter05.md#%EC%A0%81%EC%A0%88%ED%95%9C-%ED%96%89-%EA%B8%B8%EC%9D%B4%EB%A5%BC-%EC%9C%A0%EC%A7%80%ED%95%98%EB%9D%BC)
    - Import 포함 200줄 미만 시행
        - 넘을 경우 : 코드가 이미 완벽해서 분리 할 수 없는 경우 푸시 후 같이 고민하자.
2. **세로 밀집도**
    - 밀접한 행은 세로로 가까이 둔다
    - 중간에 주석이 있으면 읽기 불편하다 → 주석 쓰지 말자.
3. **수직 거리 : 101p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-04%20Chapter05.md#%EC%88%98%EC%A7%81-%EA%B1%B0%EB%A6%AC)

    4-1) protected를 쓰지말고 overriding이나 함수를 통해 접근하자

    4-2) 변수 선언 → 사용부에 최대한 가까이 선언

    4-3) 인스턴스 변수 

    - 클래스 맨 처음에 선언
    - 인스턴스 변수간 공백 없음
        - 인스턴스 변수간 개념 단위로는 묶일 수 있음.

    4-4) 종속 함수

    - 한 함수가 다른 함수를 호출한다면 두 함수는 가까이 배치한다

    4-5) 개념적 유사성

    - 명명법이나 기본 기능이 유사한 경우 개념적으로 유사하다고 본다. 가까이 배치
4. **가로 형식 맞추기 : 107p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-04%20Chapter05.md#%EA%B0%80%EB%A1%9C-%ED%98%95%EC%8B%9D-%EB%A7%9E%EC%B6%94%EA%B8%B0)
    - 최대 120자의 행길이

<br/>

## 6장. 객체와 자료구조 [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-04%20Chapter05.md#%EA%B0%80%EB%A1%9C-%ED%98%95%EC%8B%9D-%EB%A7%9E%EC%B6%94%EA%B8%B0)

1. **자료 추상화 : 118p** 
    - 무조건 getter, setter등 사용하지 말고, 객체를 표현 할 가장 좋은 방법을 고민하자.
2. **자료/객체 비대칭 : 119p** 
    - 새로운 자료 타입이 필요한 경우 → 객체 지향 기법
    - 새로운 함수가 필요한 경우 → 절체적인 코드
3. **디미터의 법칙 : 123p** 
    - 허용된 메서드가 반환한 객체의 메서드를 호출하면 안된다. A→B , B→C, A→C 노노

4. **자료 전달 객체 : 126p** 
    - 자료 전달 객체 : 공개 변수만 있고 함수가 없는 클래스 (완벽한 VO)
    - DTO / 활성 레코드는 포멧팅 하는 정도의 함수를 가지고 있을 수 있다.
    - 활성 레코드 : 소스에서 자료를 직접 변환한 결과 자료 구조와 활성 레코드를 혼합하여 자료 구조도 아니고 객체도 아닌 혼종이 나오기 쉽다.
        - 활성 레코드를 자료구조로 취급, 비즈니스 규칙을 담으면서 내부 자료를 숨기는 객체는 따로 생성
5. **VO를 주로 쓰자**.
    - 데이터 구조를 이뮤터블하게 사용할 것.

<br/>

## 7장. 오류 처리

1. **오류 코드보다 예외를 사용하자 : 130p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-11%20Chapter07.md#%EC%98%A4%EB%A5%98-%EC%BD%94%EB%93%9C%EB%B3%B4%EB%8B%A4-%EC%98%88%EC%99%B8%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%9D%BC)

    1-1) 통신을 할 때에는 Exception으로 받는다.

    → 서버에서 공통 에러 코드를 정해주면 공통 에러로직을 담고 있는 ErrorUtil을 만들어서 통신에서 받은 Exception의 공통 에러 로직을 처리하게 한다.

    → 공통 에러로직에서 처리되지 않은 Exception들은 printStackTrace()로 처리한다.

    → 의도적으로 크래시 로그를 쌓아야 하는 것만 crashlytics에 보내는 로직을 직접 추가한다. (의도하지 않은 것들을 모두 로그로 보내면 의도적으로 보고싶은 중요한 로그를 찾기 힘들기 때문)

2. **Unchecked 예외를 사용하라 : 133p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-11%20Chapter07.md#unchecked-%EC%98%88%EC%99%B8%EB%A5%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%9D%BC)
3. **예외 메세지에 의미를 제공하라 : 135p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-11%20Chapter07.md#%EC%98%88%EC%99%B8%EC%97%90-%EC%9D%98%EB%AF%B8%EB%A5%BC-%EC%A0%9C%EA%B3%B5%ED%95%98%EB%9D%BC%EC%98%88%EC%99%B8-%EB%A9%94%EC%84%B8%EC%A7%80)
    - 연산 이름, 실패 유형 등
4. **호출자를 고려해 예외 클래스를 정의하자 : 135p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-11%20Chapter07.md#%ED%98%B8%EC%B6%9C%EC%9E%90%EB%A5%BC-%EA%B3%A0%EB%A0%A4%ED%95%B4-%EC%98%88%EC%99%B8-%ED%81%B4%EB%9E%98%EC%8A%A4%EB%A5%BC-%EC%A0%95%EC%9D%98%ED%95%98%EB%9D%BC)
5. **정상 흐름을 정의하라 ( try / catch에서 실패시 결과값을 정의하지 말자 : 137p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-11%20Chapter07.md#%EC%A0%95%EC%83%81-%ED%9D%90%EB%A6%84%EC%9D%84-%EC%A0%95%EC%9D%98%ED%95%98%EB%9D%BC)
6. **결과를 null을 반환하지 말자 : 138p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-11%20Chapter07.md#null%EC%9D%84-%EB%B0%98%ED%99%98%ED%95%98%EC%A7%80-%EB%A7%88%EB%9D%BC)
    - 이 개념을 적용하면 좋겠지만, 서버에서 적용되지 않은 내용이라면 어쩔수 없이 사용해야 할 수 있다.
7. **함수의 인수로 null을 전달하지 말자 : 140p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-11%20Chapter07.md#null%EC%9D%84-%EC%A0%84%EB%8B%AC%ED%95%98%EC%A7%80-%EB%A7%88%EB%9D%BC)
    - 구글 코드에서는 null을 이용하는 코드도 있다. 그래서 이 규칙을 의심할 수도 있지만 이것에 대한 장점이 있으므로 최대한 사용 해 볼 것

<br/>

## 8장. 경계

1. **외부코드 사용할 때는 Wrapper 클래스로 감싸고 필요한 기능만 노출하자 : 144p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-11%20Chapter08.md#%EC%99%B8%EB%B6%80%EC%BD%94%EB%93%9C-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0)
2. **경계는 테스트 코드를 작성하자 : 147p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-11%20Chapter08.md#log4j-%EC%9D%B5%ED%9E%88%EA%B8%B0)

<br/>

## 9장. 단위 테스트 [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-11%20Chapter08.md#log4j-%EC%9D%B5%ED%9E%88%EA%B8%B0)

1. **테스트 케이스 갯수**
    - 잠정적으로 의심되는 부분은 다 추가
2. **사소한 테스트라도 건너뛰지 말 것**
3. **버그 주변은 철저히 테스트 할 것**
4. **테스트 코드도 가독성을 위해 단순화, 명료화 하자.**
5. **빠른 테스트 케이스를 만들자 : 167p** 
6. **테스트간 의존성이 없도록 한다 : 167p** 
7. **환경에 따라 테스트가 실패하거나 성공하면 안된다 : 168p** 
8. **테스트의 결과는 무조건 boolean형으로 가늠하자  : 168p** 
9. **실제 코드를 작성하기 직전에 테스트 코드를 작성하자 → 테스트가 정착 되고나서 하자.**

<br/>

## 10장. 클래스 [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-18%20Chapter10.md#2-%EB%B3%80%EA%B2%BD%ED%95%98%EA%B8%B0-%EC%89%AC%EC%9A%B4-%ED%81%B4%EB%9E%98%EC%8A%A4%EC%9D%8C)

1. **클래스는 작아야 한다 : 172p** 
2. **클래스의 이름 : 175p** 
    - 25자 내외로 가능해야 한다.
    - if, and, or, but은 제외한다.
    - 이름이 너무 길거나 표현하기 어려운 경우 책임이 너무 많은 것
3. **클래스의 메서드는 인스턴스 변수 하나 이상을 사용하여야 한다.(응집도) : 177p** 
4. **Enum**
    - private으로 class 종속인 경우 class안에 두자
    - 외부에서 쓸 수 있는 경우 클래스를 분리하자.

<br/>

## **11장. 시스템 (아키텍처)**

1. **시스템 제작과 시스템 사용을 분리하자 : 194p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-18%20Chapter11.md#%EC%8B%9C%EC%8A%A4%ED%85%9C-%EC%A0%9C%EC%9E%91%EA%B3%BC-%EC%8B%9C%EC%8A%A4%ED%85%9C-%EC%82%AC%EC%9A%A9%EC%9D%84-%EB%B6%84%EB%A6%AC%ED%95%98%EB%9D%BC)
2. **객체 사용에 있어서 가능하다면 DI를 사용하자 :**
3. **관심사 분리를 잘 할 것**

<br/>

## **12장. 창발성 - 각 구성 별개로서는 보이진 않지만 합쳐졌을 때 두드러지게 보이는 특성** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-18%20Chapter12.md#12-%EC%B0%BD%EB%B0%9C%EC%84%B1)

1. **모든 테스트를 실행하자 : 216p** 
2. **클래스의 크기와 메서드 수를 최소화 하자 : 217p** 
3. **리펙터링 시에는 '조금 변경 → 테스트'를 반복하자**

<br/>

## **13장. 동시성**

1. **임계 영역을 최소화 하자. (비동기 처리를 적게)**
2. **동시성 방어 원칙 : 230p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-25%20Chapter13.md#%EB%8F%99%EC%8B%9C%EC%84%B1-%EB%B0%A9%EC%96%B4-%EC%9B%90%EC%B9%99)

    1-1) **동시성 코드는 분리하라**

    단일 책임 원칙

    1-2) **자료를 캡슐화하여 공유 자료를 최대한 줄여라**

    - 공유자원은 임계영역(synchronized)으로 보호하라

    1-3) **자료 사본을 이용하라**

    1-4) **스레드는 가능한 독립적으로 구현하라** 

3. **동기화 메서드 사이의 의존성 : 235p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-25%20Chapter13.md#%EB%8F%99%EA%B8%B0%ED%99%94%ED%95%98%EB%8A%94-%EB%A9%94%EC%84%9C%EB%93%9C-%EC%82%AC%EC%9D%B4%EC%97%90-%EC%A1%B4%EC%9E%AC%ED%95%98%EB%8A%94-%EC%9D%98%EC%A1%B4%EC%84%B1%EC%9D%84-%EC%9D%B4%ED%95%B4%ED%95%98%EB%9D%BC)

    **2-1) 공유 객체 하나에는 메서드 하나만 사용하라**

    **2-2) 공유 객체 하나에 여러 메서드가 필요한 경우 아래의 방법을 고려**

    - 클라이언트에서 잠금 : 클라이언트에서 첫 번째 메서드를 호출하기 전에 서버 잠금, 마지막 메서드를 호출할 때까지 잠금 유지⇒ synchronized
    - 서버에서 잠금 : 서버에 '서버를 잠그고 모든 메서드 호출한 후 잠금 해제' 메서드 구현
    - 클라이언트에서 이 메서드 호출⇒ lock - unlock연결 서버 : 잠금을 수행하는 중간 단계 생성, '서버에서 잠금' 방식과 유사하지만 원래 서버 변경 안함

<br/>

## **14장. 점진적인 개선 : 245p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-25%20Chapter14.md#14-%EC%A0%90%EC%A7%84%EC%A0%81%EC%9D%B8-%EA%B0%9C%EC%84%A0)

- **규칙을 정하는데 해당 사항이 없음**
- **유연한 구조로 변경하기 위한 절차들을 학습하기 좋음.**

<br/>

## **15장. JUnit 들여다보기** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-09-25%20Chapter15.md#15-junit-%EB%93%A4%EC%97%AC%EB%8B%A4%EB%B3%B4%EA%B8%B0)

1. **조건문을 캡슐화하기 : 331p 
`if(a = null || b == null || c == null)` → `if(isCompact())`**
2. **부정문은 긍정문으로 바꾸기 : 331p** 

    `**shouldNotCompact()` → `canBeCompacted()`**

3. **변수명을 명확하게 짓기 : 332p** 

    `**val filteredList = filter(list)**`

4. **시간 결합을 명시하기 : 333p** 
    - `findCommonPrefix(); findCommonSuffix()` → `fun findCommonPrefixAndSuffix() { findCommonPrefix(); ...findCommonSuffix 로직... }`
    - 처음 호출 함수의 리턴값을 다음 함수에서 이용하도록 하여 순서를 강제화

<br/>

## **16장. SerialDate 리펙터링 : 343p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-10-17%20Chapter16.md#16%EC%9E%A5-serialdate-%EB%A6%AC%ED%8E%99%ED%84%B0%EB%A7%81)

- **앞선 내용들로 리펙터링 해본다.**

<br/>

## **17장. 냄새와 휴리스틱 : 368p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-10-17%20Chapter17.md#17-%EB%83%84%EC%83%88%EC%99%80-%ED%9C%B4%EB%A6%AC%EC%8A%A4%ED%8B%B1)

- **전체적인 사항을 요약한 장으로서 각 장에 규칙을 옮겼습니다.**
- **현재 안드로이드 개발에 해당하는 사항이 아닌 경우 제외하였습니다.**

<br/>

1. **환경 : 370p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-10-17%20Chapter17.md#17-%EB%83%84%EC%83%88%EC%99%80-%ED%9C%B4%EB%A6%AC%EC%8A%A4%ED%8B%B1)

    **1-1) 한 명령어로 빌드 할 수 있도록 한다.**

    **1-2) 한 명령어로 모든 단위 테스트를 할 수 있도록 한다.**

2. **일반 : 371p** [링크](https://github.com/bucketplace/cleancode_study/blob/master/2019-10-17%20Chapter17.md#%EC%9D%BC%EB%B0%98)

    **2-1) 당연한 동작은 같이 구현해 놓을 것**

    - 특정 문자열을 파싱하는데 괜히 대소문자에 따라 되고 안되고 하면 안됨

    **2-2) 컴파일러 경고를 무시하지 말자.**

    **2-3) 실패한 테스트 케이스를 미루지 말자.**
    
    **2-4) 저차원 개념은 파생 클래스에 넣고, 고차원 개념은 기초 클래스에 넣자.**

    **2-5) 기초 클래스가 파생 클래스에 의존하지 않도록 하자.**

    **2-6) 노출되는 변수나 함수를 최소화 하자.**

    **2-7) 동작 하나에 너무 많은 인터페이스를 요구하도록 하지 말자.**

    **2-8) 기능 욕심**

    **2-9) 매직 번호는 상수로 정의**

    **2-10) static 함수**

    - static 함수는 메서드를 소유하는 객체의 정보를 사용하지 않고, 재정의 할 가능성이 없을 때 만들자
    - 조금이라도 위 사항을 위반한다고 의심이 생기면 인스턴스 함수로 만들자.

    **2-11) 서술적인 변수를 사용하자.**

    - 자료구조에서 데이터를 직접 가져와서 쓰기보다 변수 이름을 두어 담아서 쓰기.( 가독성)

    **2-12) 논리적 의존성은 물리적으로도 드러내자**

    **2-13) 정확하자.**

    - null이 반환될 확률이 있다면 null 체크 할 것
    - 갱신될 확률이 희박하다고 트랜젝션 관리를 건너뛰지 말자.
    - List로 선언 할 변수를 ArrayList로 선언하지 말자
    - 모든 변수를 protected로 선언하지 말자.