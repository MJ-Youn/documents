# 기본 문법

### 변수

 - 변수를 선언할때 '=' 양 옆의 공백이 없어야 한다.
 - `변수명=` : NULL로 초기화된 변수 선언
 - `unset 변수명` : 변수를 제거
 - `readonly 변수명` : 상수로 생성
 - `set` : 사용하고 있는 변수들의 리스트

*특별한 변수 할당 방법*

 - `${X:-Y}` : x에 값이 있으면 그대로 출력, 그렇지 않으면 Y값을 사용
 - `${X:=Y}` : 위와 동일 하게 실행. Y가 사용되면 X에 Y값을 할당
 - `${X:?에러메세지}` : X에 값이 ㅇ벗으면 에러메세지와 함께 종료

### $#

 > number of params

ex)
```sh
./program param01 param02
```

 - param01은 스크립트내에서 `$1`로 불러올 수 있다.
 - 마찬가지 방법으로 program name과 param02는 `$0`, `%2`로 불러올 수 있다.

### read

```sh
read 변수명
```

 - 사용자로 부터 변수를 입력 받을 때, 위와 같이 사용한다.

### 제어문

 - `||` : 앞의 명령어 실행이 실패 했을 때, 뒤의 명령어가 실행되도록 한다.
   - ex) ``` Run Command1 || echo 실패 >> log.txt ```
 - `&&` : 앞의 명령어 실행이 성공 했을 때, 뒤의 명령어가 실행되도록 한다.
   - ex) ``` Run Command2 && echo 성공 >> log.txt ```

# 비교 옵션

### -eq

 > equal

ex)
```sh
if [ $a -eq $b ], then
fi
```

### -n

 > check the string is not empty

ex)
```sh
if [ -n $stringName ], then
fi
```

### -z

 > check the string is empty

ex)
```sh
if [ -z $line ], then
fi
```
