# java-lotto-precourse

## 간단한 로또 발매기

로또는 숫자 1~45에서 일치하는 번호6개 중에 로또 당첨 번호와 동일한 번호가 많을 수록 높은 금액을 획득한다.
로또는 장당 1000원에 구입할 수 있다.

입력으로 구입 금액과 당첨 번호를 입력하여 구매한 로또들로 얻을 수익을 계산한다.

금액 획득 규칙은 다음과 같다. (이때 하나의 보너스 번호를 맞추는 경우 상대적으로 높은 금액을 획득한다.)

- 1등: 6개 번호 일치 / 2,000,000,000원
- 2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원
- 3등: 5개 번호 일치 / 1,500,000원
- 4등: 4개 번호 일치 / 50,000원
- 5등: 3개 번호 일치 / 5,000원

예시

```
구입금액을 입력해 주세요.
8000

8개를 구매했습니다.
[8, 21, 23, 41, 42, 43]
[3, 5, 11, 16, 32, 38]
[7, 11, 16, 35, 36, 44]
[1, 8, 11, 31, 41, 42]
[13, 14, 16, 38, 42, 45]
[7, 11, 30, 40, 42, 43]
[2, 13, 22, 32, 38, 45]
[1, 3, 5, 14, 22, 45]

당첨 번호를 입력해 주세요.
1,2,3,4,5,6

보너스 번호를 입력해 주세요.
7

당첨 통계
---
3개 일치 (5,000원) - 1개
4개 일치 (50,000원) - 0개
5개 일치 (1,500,000원) - 0개
5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
6개 일치 (2,000,000,000원) - 0개
총 수익률은 62.5%입니다.
```

<hr>

## 기능 목록

### 로또 번호를 생성할 수 있다.

- 로또 번호는 총 6개이다.
- 로또 번호를 랜덤, 사용자 지정으로 생성할 수 도 있다.
- 로또 번호는 1부터 45까지 이다.
- 로또 번호가 6개가 아닌 경우 예외로 정의한다.

### 여러 당첨 종류가 있다

- 당첨 종류에 대해 관리한다.
- 당첨 종류는 같은 숫자의 갯수에 따라 달라진다.
- 보너스 번호와 같은 별도의 당첨도 있다.

### 로또는 당첨 번호와 주어진 번호를 통해 당첨을 판정하고, 당첨 종류을 반환한다

- 로또는 당첨을 결정할 수 있다.
- 당첨에 여러 종류가 있고, 가장 금액이 높은 당첨을 적용한다.
- 보너스 번호의 경우 하나만 맞더라도 당첨된다.

### 당첨 금액을 통해 수익률을 계산할 수 있다.

- 구매한 가격 대비 수익을 수익률이라고 정의한다.

### 금액에 따라 로또를 구매할 수 있다.

- 금액에 따라 로또 번호를 자동적으로 구매한다.

### 금액을 입력 받는다.

- 옳지 않은 금액 형식은 예외로 정의한다.