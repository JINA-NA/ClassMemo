# git-hub 사용하는 방법

## 1. github.com 로그인
## 2. 로컬에 폴더 생성

C 드라이브에 work 폴더, 그 안에 jina 폴더 , 그 안에 testGit 폴더 생성.

$ mkdir work/jina/textGit -p

## 3. github.com가서 start project

- Repository name : 저장소 이름

- Description : 해당 프로젝트에 대한 이름

그러면 다음 페이지에 다음과 같은 주소가 뜰거임. 

https://github.com/JINA-NA/testGit_0309.git 이런식으로.  



## 4. 주소를 gitbash에 입력

```
$ git clone [git주소.git]
$ cd [reposity폴더]
```

**shell에서는 ctrl+c / ctrl+v 안 먹음.  그래서 복사는 ctrl+insert, 붙여넣기는 shift+insert**

git의 위치로 들어오면 문장 끝에 **master**이 생길거임. 꼭 이 상태에서 작업해야만 git이 작동된다.



``` shell
$ git add [폴더 및 파일명]		//파일의 갯수가 100개이상or100mb이상 한꺼번에 첨부하면 안됨 
								//한달기준 1기가 제한
```

메일 보내는 것에 비유하자면 <ins>파일을 첨부하는 것</ins>



파일/폴더 한꺼번에 보내기

```
$ git add .
```



## 5. 첨부된 파일의 내용(설명)을 작성

```
$ git commit -m "[첨부내용을 작성]"		//-m : 한 줄짜리 명령어
```

<ins>첨부한 파일에 대한 설명을 작성하는 것. </ins>

메일 보내는 것에 비유하자면 받는 사람 주소, 본문과 같은 내용을 짧게  한줄로 작성하는 것.
" " 큰 따옴표 안에 작성하는 이유는 코드가 아니고 실 내용이기 때문에.

- 내용을  잘못 작성해서 바꾸고 싶을 때는 ```git commit --amend -m "[수정할 내용]"```

근데, ```git reset```써서 add부터 다시 하는 것도 나쁘지 않음.



- **상태 확인하는 명령어**

상태는 자주자주 확인할 것. 한 줄 쓰고 확인하고  한 줄 쓰고 확인하고.

```
$ git status		// 빨간 글씨는 첨부가 안 된 것.
					// 녹색글씨는 첨부된 것(new, modifted...)
			 		// 내용이 없는 것은 전송할 자료가 없거나, commit이 되어 전송이 되기 전 상태
```



## 6. 자료 전송

```
$ git push		// 사용자 설정이 되어있지 않으면, git config를 통해 등록
```

쉽게 말하면, 클라우드에 파일을 업로드하는 것.



## 7. 사용자 등록

```
$ git config --global user.email "[najina603@gmail.com]"		//사용자 메일 및 이름은 변경가능함
$ git config --global user.name "[jina]"
```

git-hub 최초 사용시에 사용자 등록을 해야 push를 할 수 있다. 쉽게 말하면 회원등록.

git-hub에 가입한 메일 그리고 사용자 이름을 삽입하면 된다.

 `--global` 옵션으로 설정하는 것은 딱 한 번만 하면 된다. 해당 시스템에서 해당 사용자가 사용할 때는 이 정보를 사용한다. 만약 프로젝트마다 다른 이름과 이메일 주소를 사용하고 싶으면 `--global` 옵션을 빼고 명령을 실행한다. 개인 컴퓨터가 아니라면 이 옵션을 사용하지 않는 것을 추천.



## 8. 기존에 있는 자료 다운로드받는 방법

```
$ git pull
```

git-hub에 이미 존재하는 자료를 다운받을 때 사용.

?? hub에는 여러개의 파일이 있는데, 하나의 파일만 다운받고 싶다면??



## 9. git-hub 웹상에서 파일 수정하기

오른쪽에 연필 아이콘(수정) 클릭하면 수정이 가능하다. 수정하고나서 페이지 아래에 보면 commit 작성 하는 곳이 있는데, 이게 ```$ git commit -m``` 과 같은 것이다. 



## 10. git reset

```
git reset
```

음.. 쉽게 말하면 실행취소.

가장 최상위 상태에서 몇 단계 전까지 리셋을 하겠다.??

```git reset HEAD^```  한단계 전까지 리셋을 하겠다.

```git reset HEAD~``` 한단계 전까지 리셋을 하겠다.

^ : 최초

$ : 마지막 ??



## 11. error 해결하기

### (웹에서 수정된 문서와 로컬에서 수정된 문서가 서로 충돌일으킬 때)

상황: 문서가 웹에 있고, 웹상에서 바로 수정을 했다. 그리고 그걸 로컬에서 pull 안함.
동시에 로컬에서 수정을 하고나서 push를 함.
이 때, 서로 충돌을 일으킴.

![image-20200309141037740](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200309141037740.png)

-해결방법-

1.  ```git pull```을 해서 먼저 웹에서 다운을 받아.

2.  그리고나서 충돌이 일어난 파일을 열어서 보면 아래와 같이 뜸.

   `<<<<<<<HEAD` 이하는 로컬에서 작성된 내용이고,

   `=======` 이하는  웹에서 작성된 내용이 보여진다.

   어떤 내용을 사용할지는 수동으로 작성해서 저장, 그리고 문서 작성을 마치면 add-commit-push 하면 됨!

   ---

    ![image-20200309150606843](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200309150606843.png)

   ---



##  12. 로그인 한 github 로그아웃하기
탐색기 열기(윈도우key+e) > 제어판 > 사용자 계정 > 자격 증명  관리자 > window 자격 증명 > 일반 자격 증명 > git 자격 증명 제거

## 13. 웹에서 내 사이트 보기

1. 작업 완료한 파일과 폴더를 git add - commit - push 한다.
2. 올린 파일들의 경로를 복사한다. b_coding/a_basic
3. 그리고나서 b_coding/a_basic 로 들어가서 상단에 settings 들어간다.
4. 중간~하단쯤에 있는 github pages 에 source를 master로 변경한다.
5. 빈칸에 2번에서 복사한 경로를 붙여넣는다. ??? 맞나????
6. 그 창이 초록색으로 변하면 성공적으로 된거고, 브라우저 주소창에 해당 주소를 붙여넣은 후 2번에 복사한 경로를 삽입한다. 





# **git의 개념**

git은 쉽게 말하면 클라우드같은 개념인데 버전관리를 위해 사용하는 시스템. 웹사이트 구축이라는 게 워낙 팀작업이고 다수의 제작자가 필요하기 때문에 복잡해질 가능성이 농후함. 그래서 쓰는거지.

기본적으로 git은 아래의 프로세스로 진행이 되고 있다.

**받기 - 상태 확인 - 첨부 - 설명 - 취소 - 보내기**
**clone/pull - status - add - commit - reset - push **



**< 참고자료 >**

- github [web_publlish_202002] 에 선생님 강의자료 업로드됨.

  https://github.com/xidoWeb/web_publish_202002

- git 책 

  https://git-scm.com/book/en/v2



---

# git 꼬였을 때 해결방법

---

## 상황

 git pull과 git push가 꼬여버렸다. git pull을 하자니 파일을 일일히 확인하기엔 무리인 거 같고, 그렇다고 git push가 불가한 상태. 그래서 그냥 웹상의 repository를 삭제하고, 기존에 로컬에 있는 폴더와 파일들을 웹상으로 올리고 싶다.

## 방법

1. 웹 상에서 해당 repository를 삭제한다.

   setting -> delete repository   ***백업은 필수!**

2. 해당 로컬 폴더에 있었던 .git 폴더를 삭제한다.

   폴더가 안 보일 시, 숨겨진 파일 보기로 봐야 보인다.

3. git-bash에 아래의 명령어를 차례대로 입력한다. 웹 상에 올리고자 하는 폴더 내부에서 git bash 실행

   ```shell
   git init  //이 명령어 수행 후, (master)이 떠야함
   git add *
   git commit -m "내용 설명"
   ```

4. 웹 상에서 새로운 repository 생성한다.

5. 그리고나서 아래의 명령어를 차례대로 입력한다.

   ```shell
   git remote add origin http://github.com/JINA-NA/practice
   git push origin master
   ```

   practice는 내가 새로 생성한 repository 이름

6. 웹에 잘 올라갔는지 확인하면 끝!