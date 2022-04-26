**1. 데이터베이스 관리자가 권한을 부여하는 DCL 문을 작성하시오.**
```
• 관리자가 인사담당자 고길동에게 ‘직원’ 테이블에 대해 INSERT할 수 있는 권한을 부여.

• 대소문자를 구분하지 않음.
```

<details>
<summary><b>정답 확인</b></summary>
<div markdown="1">

GRANT INSERT ON 직원 TO 고길동;

</div>
</details>
</br>

**2. 다음은 도서와 도서가격 테이블이 있다. 아래 쿼리를 수행한 결과에 들어갈 숫자를 쓰시오.**

[도서]
|책번호|책명|
|:---:|:---:|
|11|정보처리기사|
|22|빅데이터분석기사|
|55|정보처리산업기사|

   
[도서가격]
|책번호|가격|
|:---:|:---:|
|11|30,000|
|22|35,000|
|33|25,000|
|44|20,000|

[쿼리]
```
SELECT MAX(가격)
    FROM 도서가격 A,
        (SELECT 책번호
        FROM 도서
        WHERE 책명='빅데이터분석기사') B
    WHERE A.책번호 = B.책번호
```

[결과]
|가격|
|:---:|
|(     )|




<details>
<summary><b>정답 확인</b></summary>
<div markdown="1">

35,000

</div>
</details>
</br>