## 내장함수



### 수치연산함수

- abs()
  - 인자로 숫자를 전달하면 그 **숫자의 절대값을 반환**하는 함수
- divmod()
  - 첫 번째 인자를 두 번째 인자로 나눴을 때의 **몫과 나머지를 튜플 객체로 반환하는 함수**
  - a=divmod(9,5)  ==>  a=(1,4)
- pow()
  - 첫 번째로 전달된 인자 값에 대해 두 번째로 전달된 인자 값으로 **제곱한 결과를 반환**하는 함수
  - b=pow(3,2)  ==>  b=9 #3^2

### 시퀀스형/반복 가증한 자료형을 다루는 함수

- all()   #(and)
  - 반복 가능한 자료형인 List, Tuple, Set, dicrtionary, 문자열 등을 인자로 전달하여 **항목 모두가 True로 평가되면 True를 반환**하고, **False로 평가되는 항목이 하나라도 있으면 False를 반환**하는 함수
  - 0, '공백', False, None ==> False로 평가
- any()   #(or)
  - 반복 가능한 자료형인 List, Tuple, Set, dicrtionary, 문자열 등을 인자로 전달하여 **항목 모두가 False로 평가되면 False를 반환**하고, **True로 평가되는 항목이 하나라도 있으면 True를 반환**하는 함수
- enumerate()
  - List, Tuple, 문자열과 같은 시퀀스형을 입력받아 **인덱스를 포함하는 튜플 객체를 항목으로 구성하는 enumerate 객체를 반환**하는 함수
- filter()
  - **조건에 해당하는 항목을 걸러내는 함수**
  - 첫번째 매개변수: 인자에 대한 True or False
  - 두번째 매개변수: 자료형 인자에 대한 반환값
- 반복 가능한 자료형을 인자로 전달받아
  - list() : 리스트로 변환해 반환하는 함수
  - tuple() : 튜플로 변환해 반환하는 함수
  - set() : 셋으로 변환해 반환하는 함수  //중복포함x , 순서상관 x
  - dict() : 딕셔너리로 변환해 반환하는 함수
- map()
  - 두 번째 인자로 반복 가능한 자료형을 전달 받아 **자료형의 각 항목에 대해 첫 번째 인자로 전달 받은 함수를 적용한 결과를 맵 객체로 반환**하는 함수
- max()
  - 반복 가능한 자료형을 인자로 전달받아 항목 중 **가장 큰 값 반환**
- min()
  - 반복 가능한 자료형을 인자로 전달받아 항목 중 **가장 작은 값 반환**
- range()
  - 첫 번째 인자로 전달된 시작값, 두번째 인자로 전달된 종료 값, 세 번째 인자로 전달된 증감치를 이용해 시퀀스형 객체를 생성하는 함수
  - 종료 값으로 사용된 두 번째 인자의 값은 포함되지 않음
- sorted()
  - 반복 가능한 자료형을 인자로 전달받아 항목들로부터 **정렬된 리스트를 생성해 반환**하는 함수
  - 오름차순으로 정렬
  - list(reversed(sorted(a)))  ==> 리스트a에 대한 내림차순의 리스트 객체 생성
- zip()
  - 둘 이상의 반복 가능한 자료형을 인자로 전달 받아, **동일 위치의 항목을 묶어 튜플을 항목으로 구성하는  zip객체를 생성**하는 함수
  - 인자로 전달된 객체는 동일 자료형이면서, 항목의 개수가 같아야함



### 변환함수

- chr()
  - **정수형태의 유니코드 값**을 인자로 전달받아 **해당 코드의 문자**를 반환하는 함수
- ord()
  - **문자**를 인자로 전달 받아 **유니코드 값(10진수 정수)**을 반환하는 함수
- hex()
  - 1**0진 정수값**을 인자로 전달 받아 **16진수로 변환된 값을 반환**하는 함수
- int()
  - 인자로 전달된 **숫자 형식의 문자열, 부동소수점 숫자**를 **정수**로 변환한 값을 반환하는 함수
  - int("10", 2)  ==> 2   #2진수 표현인 문자열 '10'을 10진수 2로 변환해줌 
  - int("3C",16)  ==> 60  #16진수 표현인 문자열 '3C'를 10진수 60으로 변환해줌
  - int(4.5)  ==> 4  #4.5를 정수 4로 변환
- float()
  - 인자로 전달된 **숫자 형식의 문자열, 정수**를 **부동소수점 숫자**로 변환한 값을 반환하는 함수
- str()
  - 인자로 전달된 객체에 대한 **문자열 변환 값**을 반환하는 함수
  - str(4.5)  ==> '4.5'  # 부동소수점이 문자열로 변환



### 객체 조사를 위한 함수

- dir()
  - 인자로 전달된 개체가 가지고 있는 변수, 메서드와 같은 **속성 정보를 리스트 객체로 반환**
  - 인자를 전달하지 않고 호출하면 현재 **지역 스코프에 대한 정보를 리스트 객체로 반환**
- globals()
  - 현재의 **전역 심볼 테이블**을 보여주는 **딕셔너리를 반환**하는 함수
  - 전역변수와 함수, 클래스의 정보 포함
- locals()
  - 현재의 **지역 심볼 테이블**을 보여주는 **딕셔너리를 반환**하는 함수
  - 매개변수를 포함한 지역변수와 중첩함수의 정보 포함
- id()
  - 인자로 전달된 객체의 **고유 주소(참조값)를 반환**하는 함수
  - 보통 16진수로 표현 ==> hex(id(x))
- isinstance()
  - 첫 번째 인자로 전달된 객체가 두 번재 인자로 전달된 클래스의 **인스턴스인지에 대한 여부를 True/False로 반환**하는 함수
- issubclass()
  - 첫 번째 인자로 전달된 객체가 두 번재 인자로 전달된 클래스의 **서브클래스인지에 대한 여부를 True/False로 반환**하는 함수



### 실행 관련 함수

- eval()
  - 실행 가능한 표현식의 **문자열**을 인자로 전달받아 해당 **문자열의 표현식을 실행한 결과값**을 반환하는 함수
