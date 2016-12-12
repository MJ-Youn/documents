## userid is not in the sudoers file. This incident will be reported

 - /etc/sudoers 파일에 해당 계정이 없을 경우 나오는 문제
 - 파일에 계정을 추가하는 방식으로 해결 할 수 있다.

> username ALL=(ALL) NOPASSWD: ALL

 - user가 sudo를 사용할 수 있다.
 - sudo password를 물어보지 않는다.

> username ALL=(ALL) ALL

 - sudo를 사용 할 수 있게 하지만, password를 물어본다.
