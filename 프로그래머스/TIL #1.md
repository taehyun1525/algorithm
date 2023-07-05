# TIL #1

글쓴이: 블루 blue
생성 일시: 2023년 6월 6일 오전 11:16
최종 편집 일시: 2023년 6월 7일 오후 12:00

# 프로그래머스 레벨 0 정복하기

- flag에 따라 다른 값 반환하기

[](https://school.programmers.co.kr/learn/courses/30/lessons/181933?language=javascript)

- 내 코드

```jsx

- 내가 생각한 코드

```jsx
function solution(a, b, flag) {
    flag = true;
    let result = 0;
    if (flag) {
        return result = a + b
    } else {
        return result = a - b
    }
}
```

- 다른 사람 코드

```jsx
function solution(a, b, flag) {
    return flag ? a+b : a-b
}
```

궁금한 점은 다른 사람 코드는 조건부 연산자로 사용한 것이고 제가 사용한건 if절인데 그거 말고는 다른게 없는 것 같은데 정답과 결과가 다르다는 점이 왜 그런가에 대해 궁금합니다.
```

- flag 매개변수
- let flag로 true 값을 줘버려서 아무리 else를 써도 false 값이 들어오지 않았음.
- if에서 조건을 걸었어야함.