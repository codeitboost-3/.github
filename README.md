# 🌌 기억 저장 및 공유 서비스, 조각집

## 선택한 기술 스택 및 사용 라이브러리
- FE : React
- BE : Node.js, Express

## 프로젝트 폴더 구조

## 컨벤션
### 프론트 코딩 컨벤션

- space와 tab 혼용하지 않기
- 한 줄에 하나의 문장만 허용
- 문장 종료 시 세미콜론 반드시 사용
- 변수와 함수의 이름은 카멜 케이스 사용
- 클래스와 컴포넌트의 이름은 파스칼 케이스 사용
- 변수 선언할 때 const와 let 사용
- 린팅-ESLint, 포매팅-Prettier 사용

   참고: [코딩컨벤션 | TOAST UI :: Make Your Web Delicious!](https://ui.toast.com/fe-guide/ko_CODING-CONVENTION)

### 백 코딩 컨벤션

- 코드 앞 뒤에 공백 사용하기 (연산자 등)
- 콤마 뒤에는 띄어쓰기

```jsx
//bad
app.listen(3000,()=>console.log('Server Started'))

//good
app.listen(3000, () => console.log('Server Started'));
```

- 작은 따옴표 사용하기

```jsx
// bad
const a = "No"

// good
const b = 'Yes';
```

- 중괄호 열기 전에 줄 바꾸지 않기
- 중괄호 닫기 전에 줄 바꾸기

```jsx
if (n < 0) {
  alert(`Power ${n} is not supported`);
};
```

- 모든 구문 끝에 세미콜론 붙이기
- 공백 2칸 들여쓰기

```jsx
//bad
async function getColorSurvey(id) {
    const res = await axios.get(`https://learn.codeit.kr/api/color-surveys/${id}`)
  return res.data
}

//good
async function getColorSurvey(id) {
  const res = await axios.get(`https://learn.codeit.kr/api/color-surveys/${id}`);
  return res.data;
};

```

- 가로 길이 너무 길게 하지 않기

네이밍 정리 

- 쓰임새 드러나는 이름 쓰기
- 카멜케이스 : 변수, 함수 등 (myName, getColor)
- 파스칼 표기법: 클래스 (UserProfile)
- 스네이크 표기법 + 대문자 : 상수 (DEFAULT_LANGUAGE)

변수 

- const를 기본으로 사용, 필요시 let 사용 ( var 사용하지 않기 )
- 한 번에 변수 하나만 선언하기

```jsx
// bad
var a = 1, b = 2;

// good
const a = 1;
const b = 2;
```

함수 

- arrow function 문법(`=>`)과 비교 연산자 (`<=`, `>=`)를 함께 사용할 경우, 소괄호(`()`)를 이용하여 표현하기

```jsx
// bad
const itemHeight = item => item.height > 256 ? item.largeSize : item.smallSize;

// good
const itemHeight = (item) => {
  const { height, largeSize, smallSize } = item;
  return height > 256 ? largeSize : smallSize;
};
```

- 함수 이외의 블록 (if나 while같은) 안에서 함수를 선언하지 않기

```jsx
// bad
let i;
for (i = 10; i; i--) {
    (function() { 
      return i; 
    })();
}

// bad
while(i) {
    let a = function() {
      return i;
    };
    a();
}

// good
const a = function() {};
let i;
for (i = 10; i; i--) {
    a();
}
```

- 파라미터 기본값은 가장 뒤에 위치하기

## 역할 분담

- 이연수 : 그룹/댓글 FE
- 장다현 : 게시글(추억)/배지 기능 FE
- 유수빈 : 게시글(추억) BE
- 장지인 : 그룹 BE, 팀장
- 한정현 : 댓글/배지 BE

## 파트별 레포 링크
### FE 
https://github.com/codeitboost-3/FE
### BE
https://github.com/codeitboost-3/BE
