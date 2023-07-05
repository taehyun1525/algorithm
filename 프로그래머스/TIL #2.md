# TIL #2

글쓴이: 블루 blue
생성 일시: 2023년 6월 7일 오전 11:45
최종 편집 일시: 2023년 6월 7일 오후 12:05

- 문자열을 정수로 변환하기

[](https://school.programmers.co.kr/learn/courses/30/lessons/181848)

- 코드

```jsx
function solution(n_str) {
    return Number(n_str);
}
```

- Number() 함수 : 문자열을 숫자로 변환하는 함수이다.

- 공배수

[](https://school.programmers.co.kr/learn/courses/30/lessons/181936)

```jsx
function solution(number, n, m) {
    var answer = 0;
    if(number % n == 0 && number % m ==0){
        return 1;
    } else {
        return 0;
    }
}
```

- 느낀점
    
    최소공배수 같은 문제는 많이 접해봤기 때문에 어렵지 않게 풀 수 있었습니다.