MarkDown & Git
===

마크 다운 방법에 대해서 공부하며 동시에 깃도 같이 공부하여 기재해본다.

[MarkDown 바로가기](#MarkDown)

[Git 바로가기](#Git)


***

# MarkDown

마크다운은 웹상에서 글작성을 하는 모든 사람들을 위한 글쓰기 도구 입니다.

1.제목
---
* 1.1 메인 제목(Main Title)

    Main Title 
    ===

    ```
    Main Title
    ===
    ```
* 1.2 서브 제목(Sub Title)

    Sub Title 
    ---

    ```
    Subs Title
    ---
    ```

2.글씨 크기
---
* 2.1 H1 ~ H6 크기

    # H1
    ## H2
    ### H3
    #### H4
    ##### H5
    ###### H6

    ```
    # H1
    ## H2
    ### H3
    #### H4
    ##### H5
    ###### H6
    ```
3.BlockQuote
---
이메일에서 사용하는 블럭인용문자

> 오잉
>   > 오잉
>   >   > 오잉

```
> 오잉
```

4.목록
---
* 4.1 순서있는 목록
    ```
    1. 첫번째
    2. 두번째
    3. 세번째
    ```
    1. 첫번째
    2. 두번째
    3. 세번째

* 4.2 순서없는 목록
    ```
    * 테
        * 스
            * 트

    + 테
        + 스
            + 트

    - 테
        - 스
            - 트
    ```
    * 테
        * 스
            * 트

    + 테
        + 스
            + 트

    - 테
        - 스
            - 트

5.강조
---
* 5.1 기울인 텍스트
    ```
    *기울어짐*
    ```
    *기울어짐*

* 5.2 굵은 글씨 텍스트
    ```
    **굵어짐**
    ```
    **굵어짐**
    __ㅇ__

* 5.3 취소 텍스트
    ```
    ~~취소~~
    ```
    ~~취소~~

6.링크
---
* 6.1 주소
    ```
    [구글](https://google.ca)

    [네이버](https://naver.com "링크에 대한 주석 작성은 큰따음표로")

    [Git 메인페이지로](../../)

    [참조 링크][reference Link]

    [reference Link]: http://naver.com "네이버입니다."
    ```
    [구글](https://google.ca)

    [네이버](https://naver.com "링크에 대한 주석 작성은 큰따음표로")

    [Git 메인페이지로](../../)

    [참조 링크][reference Link]

    [reference Link]: http://naver.com "네이버입니다."

7.이미지
---
* 7.1 이미지
    ```
    ![대체 텍스트 입력](이미지주소 "이미지 주석은 여기로")
    <img src="이미지 경로" width="길이" height="높이" title="설명" alt="alt값"></img>
    ```
    ![대체 텍스트 입력](https://vignette.wikia.nocookie.net/aokana/images/5/50/Wiki-background/revision/latest?cb=20180128203228 "이미지 주석은 여기로")

    <img src="https://vignette.wikia.nocookie.net/aokana/images/5/50/Wiki-background/revision/latest?cb=20180128203228" width="500" height="272" title="이미지 <img> 사용" alt="aokana"></img>

***

# Git

Git은 제일 큰 사용 이유는 버전 관리 이며 다른 개발자와의 빠른 협업환경을 조성 하기 위함입니다.
SVN(파일단위 관리 시스템) 과는 달리 누가, 언제, 무엇을, 왜, 어떻게 수정했는지 코드 리뷰가 가능합니다.
대부분의 IDE에서 지원하며 누구든 사용가능 합니다.

1.Git의 역할
---
* 소스코드 병합 (Merge, Rebase)
* 소스코드 리비전 관리 (Reset, Commi, Branch)
* 소스코드 릴리즈 (Push)
* 소스코드 태깅 (Tag)
* 소스코드 변경사항 검토 (Diff, Log)

2.Git
---
초기 생성
```
git init
```

원격 주소 설정
```
git remote add https://github.com/nkwoo/MarkDownAndGit.git
```

원격지에서 깃 받아오기 
```
git clone https://github.com/nkwoo/MarkDownAndGit.git
```

로컬에서 작업 후 로컬 깃에 추가하기
```
git add *
git add index.html
```

로컬 깃에 파일 추가후 커밋 작성하기<br>
깃 메시지 수정할때는 --amend 옵션추가
```
git commit -m "커밋 메시지 작성"
git connit -m "커밋 메시지 재수정" --amend
```

로컬 깃에서 원격지 깃에 업로드 하기
```
git push -u origin master
```

로컬 깃 현재 상태 조회
```
git status
```

원격지 깃에서 깃 파일 가져오기<br>
pull 과 fetch의 차이점은 merge를 하느냐 안하느냐 차이<br>
pull : fetch + merge
```
git pull origin master
git fetch origin master
```

***

출처
[**마크다운 사용법**](https://gist.github.com/ihoneymon/652be052a0727ad59601#21-%ED%97%A4%EB%8D%94headers)
[**Git 사용방법**](https://github.com/KennethanCeyer/tutorial-git)