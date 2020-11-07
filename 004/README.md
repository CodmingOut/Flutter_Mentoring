# 데이터도 형태가 있어요!

다트 언어에서의 데이터 타입을 알아봅시다.

<br>

## 데이터 타입 종류

다트 언어에는 여러 데이터 타입이 존재합니다.

1. 숫자

	- int : 정수

	- double : 실수

2. 문자

	- String : 문자열

3. 불(불리언, 불린, Boolean)

	- bool : 불(true, false)

4. 리스트

	- List : 여러 데이터를 가질 수 있는 데이터 타입

5. 맵

	- Map : 여러 데이터를 Key-Value 형태로 가질 수 있는 데이터 타입.

6. 모든 타입이 가능한 타입

	- dynamic : 어떤 데이터 타입 값이든 가질 수 있는 데이터 타입.

그 외에도 여러 데이터 타입이 있습니다. 하지만 여기선 위의 6가지만 알아보도록 하겠습니다.

<br>

## 숫자

숫자를 표현하는 데이터 타입은 int 와 double 이 있습니다.

각각 살펴보도록 합시다.

1. int

	정수를 나타내는 데이터 타입입니다.

	```dart
	int a = 0;
	```

	위와 같이 선언하고, 초기화합니다.

2. double

	실수를 나타내는 데이터 타입입니다.

	```dart
	double a = 7.1;
	```

	위와 같이 선언하고, 초기화합니다.

<br>

숫자 데이터 타입에서 쓸 수 있는 속성(Property)은 다음과 같습니다.

아래의 속성들 외에도, 여러 속성이 있습니다.

|ID|Property|Description|
|:---:|:---|:---|
|1|hashCode|해당 숫자 값의 해시값을 반환|
|2|isFinite|해당 값이 유한한 값이면 true, 아니면 false|
|3|isInfinite|해당 값이 무한한 값이면 true, 아니면 false|
|4|isNan|해당 값이 숫자가 아닌 값(Not A Number)이면 true, 아니면 false|
|5|isNegative|해당 값이 음수면 true, 아니면 false|
|6|sign|해당 값이 음수면 -1, 0이면 0, 양수면 1을 반환|
|7|isEven|해당 값이 짝수면 true, 아니면 false|
|8|isOdd|해당 값이 홀수면 true, 아니면 false|

속성은 아래와 같이 쓸 수 있습니다.

```dart
void main() {
  int val = -7;
  print(val.sign); // Print -1
}
```

<br>

숫자 데이터 타입에서 쓸 수 있는 함수(메서드)는 다음과 같습니다.

아래의 함수들 외에도, 여러 함수가 있습니다.

|ID|Method|Description|Parameters|
|:---:|:---|:---|:---|
|1|abs|해당 숫자 값의 절댓값을 반환||
|2|ceil|해당 숫자 값보다 작지 않은 가장 작은 정수 값을 반환(올림)||
|3|compareTo|해당 숫자 값과 매개변수로 준 값을 비교하여 같다면 0, 해당 숫자 값이 크면 1, 작다면 -1을 반환|num(int, double)|
|4|floor|해당 숫자 값보다 크지 않은 가장 큰 정수 값을 반환(내림)||
|5|remainder|해당 숫자 값과 매개변수로 준 값을 나눈 나머지를 반환(~/)|num(int, double)|
|6|round|해당 숫자 값과 가장 가까운 정수 값을 반환(반올림)||
|7|toDouble|해당 값을 double 형으로 형변환한 값을 반환||
|8|toInt|해당 값을 int 형으로 형변환한 값을 반환||
|9|toString|해당 값을 문자열 형으로 형변환한 값을 반환||
|10|truncate|해당 값에서 소숫점 아래를 모두 버린 정수 값을 반환||

함수는 아래와 같이 쓸 수 있습니다.

```dart
void main() {
  double n = 7.1;
  print(n.toInt()); // Print 7
}
```

<br>

## 문자

문자를 표현하는 데이터 타입은 String 이 있습니다.

```dart
String s = '안녕!';
String multiLineString = '''
  안녕!
  이렇게 하면 여러 줄도 쓸 수 있어요!
''';
```

위와 같이 선언하고, 초기화합니다.

문자열을 직접 써주는 경우(위의 경우, 안녕! 이라는 문자열), 작은 따옴표 혹은 큰 따옴표로 감싸주셔야 합니다.

<br>

```dart
void main() { 
   String str1 = "hello"; 
   String str2 = "world"; 
   String res = str1 + str2;

   int idx = 5;
   
   print("${idx}. The string : ${res}"); // 5. The string : helloworld

   int n=1+1; 
   
   String str1 = "The sum of 1 and 1 is ${n}";
   print(str1); // The sum of 1 and 1 is 2
   
   String str2 = "The sum of 2 and 2 is ${2+2}"; 
   print(str2); // The sum of 2 and 2 is 4
}
```

다트에서는 위와 같이 '+' 연산자를 통해 문자열과 문자열을 결합하는 것을 지원하고, $와 중괄호(상황에 따라 생략 가능)를 통해 문자열 안에 값을 넣을 수도 있습니다.

<br>

```dart
void main() {
	String hello = "안녕하세요!";
	print(hello[1]); // 녕
}
```

문자열에서 어떤 위치에 있는 문자 1개를 가져오려면, 위와 같이 대괄호와 인덱스를 사용하여 가져올 수 있습니다.

<br>

문자 데이터 타입에서 쓸 수 있는 속성(Property)은 다음과 같습니다.

아래의 속성들 외에도, 여러 속성이 있습니다.

|ID|Property|Description|
|:---:|:---|:---|
|1|codeUnits|문자열의 각각의 문자 하나의 UTF-16 코드들의 리스트를 반환|
|2|isEmpty|문자열의 값이 비었다면 true, 아니면 false|
|3|length|문자열의 길이 반환|

속성은 아래와 같이 쓸 수 있습니다.

```dart
void main() {
  String hello = "안녕하세요 여러분!";
  print(hello.length); // 10
}
```

<br>

문자 데이터 타입에서 쓸 수 있는 함수(메서드)는 다음과 같습니다.

아래의 함수들 외에도, 여러 함수가 있습니다.

|ID|Method|Description|Parameters|
|:---:|:---|:---|:---|
|1|toLowerCase|문자열의 영어들을 모두 소문자로 바꾼 문자열을 반환||
|2|toUpperCase|문자열의 영어들을 모두 대문자로 바꾼 문자열을 반환||
|3|trim|문자열 앙 옆에 있는 빈 칸을 모두 없앤 문자열을 반환||
|4|compareTo|문자열과 매개변수로 들어온 문자열을 비교. 같으면 0, 사전순으로 해당 문자열이 더 앞에 있다면 -1, 더 뒤에 있다면 1을 반환|String|
|5|replaceAll|매개변수로 패턴과 바뀔 문자열을 받고, 해당 문자열에 받은 패턴과 같은 형태의 패턴을 모두 바뀔 문자열로 바꾼 문자열을 반환|Pattern, String|
|6|split|매개변수로 패턴을 받고, 그를 기준으로 문자열을 나눈 뒤, 결과를 리스트로 반환|Pattern|
|7|substring|매개변수로 한(두) 개의 정수값을 받고, 그를 기준으로 문자열을 자른 결과를 반환|int, [int]|
|8|codeUnitAt|매개변수로 한 개의 인덱스(정수)를 받아서, 해당 인덱스 위치에 있는 문자의 UTF-16 코드를 반환|int|

함수는 아래와 같이 쓸 수 있습니다.

```dart
void main() {
  String str1 = "  Hello World!    ";
  print(str1.trim()); // Hello World!
  
  String str2 = "Hello World";
  print("New String: ${str2.replaceAll('World','ALL')}"); // New String: Hello ALL
  
  String str3 = "Today,is,Thursday"; 
  print("New String: ${str3.split(',')}"); // New String: [Today, is, Thursday]
  
  String str4 = "Hello World"; 
  print("New String: ${str4.substring(6)}"); // New String: World
  print("New String: ${str4.substring(2,6)}"); // New String: llo (인덱스 2부터 6미만(즉, 5)까지 자름)
}
```

<br>

## 불(불리언, 불린, Boolean)

불을 표현하는 데이터 타입은 bool 이 있습니다.

이 타입은 오직 true와 false만 가질 수 있습니다.

```dart
bool test = false;
bool isHuman = true;
```

위와 같이 선언하고, 초기화합니다.

불 타입은 딱히 속성이나 함수가 존재하지 않습니다.

그만큼 간단한 데이터 타입이죠!

