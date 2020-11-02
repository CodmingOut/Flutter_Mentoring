# 플러터 설치해봅시다!

필자는 윈도우 환경이므로, 윈도우를 기준으로 설명하겠습니다.

MacOS는 [여기](https://flutter.dev/docs/get-started/install/macos)를 참고하고, 리눅스는 [여기](https://flutter.dev/docs/get-started/install/linux)를 참고해주세요!

<br>

## 설치를 시작해볼까요?

이 글은 원문을 기반으로 쓰였습니다. 원문은 [이곳](https://flutter.dev/docs/get-started/install/windows)을 참고해주세요.

<br>

## SDK 다운로드

![i01](./i01.png)

먼저, [여기](https://flutter.dev/docs/development/tools/sdk/releases?tab=windows)서 플러터 SDK를 다운로드 받습니다.

링크를 들어가면, 위의 사진과 같이 `Stable channel`이 보일텐데, 거기서 최신 버전을 다운로드 받아줍니다.

<br>

![i02](./i02.png)

다운받은 압축 파일을 원하는 곳에 놓고, 이름을 `flutter`로 바꿔준 뒤, 압축을 풀어줍니다.

그러면 위와 같이 flutter 파일을 볼 수 있습니다.

<br>

## 환경변수 설정

![i03](./i03.png)

시작 키를 누르고 환경을 치면, 다음과 같이 '시스템 환경 변수 편집'을 볼 수 있습니다.

<br>

![i04](./i04.png)

그럼 위와 같이 시스템 속성 창이 나올텐데요.

거기서 환경 변수 버튼을 눌러줍니다!

<br>

![i05](./i05.png)

위의 사진에는 개인정보 때문에 가려놨지만, 원래는 값이 가득가득합니다.

나온 환경 변수 창에서, 시스템 변수 중 `Path` 항목을 찾아줍니다.

`Path`를 선택하고(누르고) 편집을 눌러줍니다.

<br>

![i06](./i06.png)

위의 사진 처럼 환경 변수 편집 창이 나올겁니다.

여기서 '새로 만들기' 버튼을 누르고, 아까 저장했던 `flutter` 파일 위치에 `bin` 파일을 더해서 위와 같이 경로를 추가해줍니다.

저는 D드라이브의 `Program Files` 파일에 `flutter` 파일의 압축을 풀어놓았으므로 위와 같이 `D:\Program files\flutter\bin\` 의 형태로 경로가 나오게 됩니다.

<br>