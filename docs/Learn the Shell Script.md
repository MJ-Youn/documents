# 비교 옵션

### $#

`number of params`

ex)
```shell
./program param01 param02
```

* param01은 스크립트내에서 `$1`로 불러올 수 있다.
* 마찬가지 방법으로 program name과 param02는 `$0`, `%2`로 불러올 수 있다.

### -eq

`equal`


### -z

`check the string empty`

ex)
```sh
if [ -z $line ], then
fi
```

# 문법
