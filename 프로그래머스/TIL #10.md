# TIL #10

글쓴이: 블루 blue
생성 일시: 2023년 7월 1일 오후 6:52
최종 편집 일시: 2023년 7월 2일 오후 3:44

# 프로그래머스 레벨 0 정복하기

> 정수찾기
> 
- 정수 리스트 `num_list`와 찾으려는 정수 `n`이 주어질 때, `num_list`안에 `n`이 있으면 1을 없으면 0을 return하도록 solution 함수를 완성해주세요.
- 내 풀이

```jsx
function solution(num_list, n) {
    var answer = 0;

    for(let i of num_list){
        if(i==n){
            return 1;
        }
    }

    return answer;
}
```

- 다른 사람 풀이

```jsx
//1번
const solution=(l,n)=>+(l.includes(n))

//2번
const solution = (num_list, n) => num_list.includes(n) ? 1 : 0

//3번
function solution(num_list, n) {
    let result = 0;

    result = num_list.find((el)=>el === n);

    result = result === undefined ? 0 : 1;

    return result;
}

//4번
function solution(num_list, n) {
    return num_list.indexOf(n) >= 0 ? 1 : 0
}

```

- 느낀점
    - 내가 풀던 방식과는 다르게 내장함수를 사용하여 푼 사람들이 많았다. 자바스크립트의 내장 함수에 대해 좀더 면밀히 공부할 필요가 있는 것같다. 그 중에 많이 보이던 find와includes, some을 정리하고 봐야할 것 같다.

- find() : 주어진 판별 함수를 만족하는 **첫 번째 요소**의 **값**을 반환합니다. 그런 요소가 없다면 `[undefined](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/undefined)`를 반환합니다.
- includes() : 배열이 특정 요소를 포함하고 있는지 판별합니다.
- some() :  배열 안의 어떤 요소라도 주어진 판별 함수를 적어도 하나라도 통과하는지 테스트합니다. 만약 배열에서 주어진 함수가 true을 반환하면 true를 반환합니다. 그렇지 않으면 false를 반환합니다. 이 메서드는 배열을 변경하지 않습니다.