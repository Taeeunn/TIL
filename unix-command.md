# unix-command


## :bulb: mv

### 1. 파일을 옮기는 경우
```
mv file DEST 
```

  - DEST가 나타내는 경로가 이미 존재하는 디렉토리라면 그 디렉토리 안으로 file이 이동한다.

  - DEST가 나타내는 경로가 아직 존재하지 않는 경로라면 그 경로명대로 이름 변경 혹은 위치 이동 혹은 둘 다를 할 수도 있다. 
    예를 들면 DEST가 file2면 이름만 file2로 바뀐다.
    하지만 DEST가 ../file이라면 위치 이동만 한다. 
    마지막으로 DEST가 ../file2라면 이름 변경도 되고 위치 이동도 된다. 

  - 이동하게 되는 디렉토리 안에 DEST와 이미 같은 이름의 파일이 있으면 그 파일을 덮어쓰게 된다. 이런 일을 방지하려면 mv 커맨드를 쓸 때 -i 옵션을 주면 된다.
    i는 interactive의 줄임말로 혹시 덮어쓰게 될 상황이 생기면 바로 덮어쓰지는 않고 사용자의 의견을 물어보겠다는 뜻이다.
    ```
    mv -i file ../alreadyExists
    ```
    
    
### 2. 디렉토리를 옮기는 경우
```
mv dir DEST
```

   - DEST가 나타내는 경로가 이미 존재하는 디렉토리라면 그 디렉토리 안으로 dir가 이동한다. 

   - DEST가 나타내는 경로가 아직 존재하지 않는 경로라면 그 경로명대로 이름 변경 혹은 위치 이동을 혹은 둘 다를 할 수도 있다.
     예를 들면 DEST가 dir2면 이름만 dir2로 바뀐다.
     하지만 DEST가 ../dir라면 위치 이동만 한다. 
     마지막으로 DEST가 ../dir2라면 이름 변경도 되고 위치 이동도 된다.

   - DEST가 이미 존재하는 파일의 이름이라면 어떻게 될까요? 이렇게 되면 에러 메시지가 출력되면서 아무 동작도 일어나지 않는다. 
     왜냐하면 하나의 디렉토리 안에는 같은 이름의 것들이 존재할 수 없기 때문이다.


<br><br><br>


## :bulb: cp

### 파일 복사
```
cp file1 file2
```

### 디렉토리 복사
```
cp -r dir1 dir2
```

### dir2가 이미 존재하는 파일일 경우 사용자 의견을 물어봄
```
cp -i file1 file2
```

<br><br><br>

## :bulb: rm

### 파일 삭제
```
rm file
```

### 디렉토리 삭제
```
rm -r dir
```

### 디렉토리 안의 파일을 하나씩 확인한 후 삭제
```
rm -r -i dir
```


<br><br><br>

## :bulb: cat, less

#### cat: 파일들의 내용을 이어서 출력
#### less: cat과 다르게 한 화면에 하나의 파일을 보여줌
```
less file1 file2
```
'space': 아래로 한 페이지 이동, 'b': 위로 한 페이지 이동
'G': 맨 끝으로 이동, 'g': 맨 처음으로 이동
':n': 다음 파일으로 이동, ':p': 이전 파일로 이동



<br><br><br>

## :bulb: head, tail: 파일의 일부 내용만 볼 수 있는 command

#### file의 처음 부분 20줄 
```
head -n 20 file
```

#### file의 뒷 부분 30줄 
```
tail -n 30 file
```


<br><br><br>




<br><br><br>

# terminal 사용 tip

<br><br>

### :heavy_check_mark: history: 사용한 command 내역을 보여줌
   - 느낌표(!)를 번호 앞에 붙이고 실행하면 간단하게 그 커맨드를 다시 실행할 수 있다.

### :heavy_check_mark: clear: 터미널 화면을 깔끔하게

### :heavy_check_mark: tab key: 디렉토리나 파일 이름 자동완성

### :heavy_check_mark: ctrl+a: 커서가 맨 앞으로 이동 / ctrl+e: 커서가 맨 뒤로 이동



<br><br><br>

# vim 사용 tip

<br>

Vim 공식 사용 설명서(https://vimhelp.org/#help.txt) <br>
Vim을 게임처럼 재미있게 배울 수 있는 사이트(https://vim-adventures.com/)

<br>

![image](https://user-images.githubusercontent.com/32799078/109022835-8ed51780-76ff-11eb-8c25-084bb2decfee.png)


<br>

## 일반모드

![image](https://user-images.githubusercontent.com/32799078/109022935-a8765f00-76ff-11eb-91e9-49a302aa5895.png)
  
<br>

## 입력모드
  
![image](https://user-images.githubusercontent.com/32799078/109023224-f55a3580-76ff-11eb-8330-484cde79e2c2.png)

<br>

## 명령모드 

![image](https://user-images.githubusercontent.com/32799078/109023703-5b46bd00-7700-11eb-8506-e16a5dc414ed.png)

  - : colon 명령모드로 전환
  - !: 강제 실행
  - / slash 명령모드로 전환 (텍스트 검색)


<br>


## 비주얼모드

![image](https://user-images.githubusercontent.com/32799078/109023828-787b8b80-7700-11eb-920b-7359562b019b.png)

   - v: 비주얼 모드로 전환 / 한 글자씩 블록 지정
   - V: 비주얼 모드로 전환 / 줄 단위로 블록 지정
   - 방향키로 블록 지정
   - x: 텍스트 삭제
   - y: yank 복사하기
   - p: 커서 다음 칸에 붙여넣기
   - P: 커서 이전 칸에 붙여넣기
   - d: delete 삭제하기 
   - 잘라내기: d(삭제) -> p/P(붙여넣기)


