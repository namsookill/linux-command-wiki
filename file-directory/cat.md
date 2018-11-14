# cat

첫 번째 파라미터로 읽을 파일(여러 개 가능)을 입력 받아 파일의 내용을 출력해주는 명령어

## 사용법

> **cat [옵션] [파일...]**

| 옵션 	| 설명 	|
|:----:	|:---------------------------------------------------------	|
| -b 	| 각 라인의 행번호 표시(공백 줄은 제외) 	|
| -n 	| 각 라인의 행번호 표시(공백 줄의 행번호 표시) 	|
| -s 	| 공백이 2줄 이상 반복될 때, 한 줄만 표시하고 나머지는 생략 	|


``` shell
❯  cat mytest.txt
테스트파일의 첫번째 라인

테스트파일의 두번째 라인

테스트파일의 세번째 라인
```

파일이 너무 길면 `more` 명령어를 조합해서 사용해야한다.  
`more`를 사용하면 페이지를 나눠준다. 다음 페이지를 보려면 **Space** 를 입력해야하고, 한 줄씩 읽으려면 **Enter키**를 입력하면 된다.

``` shell
❯  cat /etc/man.conf | more
```

인터프리터 형식으로 한 줄씩 입력할 때도 사용할 수 있다.

``` shell
❯  cat > mytest2.txt
한 줄씩 입력가능하며,
이미 입력된 것은 수정할 수 없다
종료하기 위해선 Ctrl + d를 입력한다.
```

### 옵션

``` shell
❯  cat -b mytest.txt
     1	테스트파일의 첫번째 라인


     2	테스트파일의 두번째 라인

     3	테스트파일의 세번째 라인
❯  cat -n mytest.txt
     1	테스트파일의 첫번째 라인
     2
     3
     4	테스트파일의 두번째 라인
     5
     6	테스트파일의 세번째 라인
❯  cat -s mytest.txt
테스트파일의 첫번째 라인

테스트파일의 두번째 라인

테스트파일의 세번째 라인
```

