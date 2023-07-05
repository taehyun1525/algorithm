# TIL #13

글쓴이: 블루 blue
생성 일시: 2023년 7월 5일 오전 11:29
최종 편집 일시: 2023년 7월 5일 오전 11:40

### 글자 이어 붙여 문자열 만들기

- 문자열 `my_string`과 정수 배열 `index_list`가 매개변수로 주어집니다. `my_string`의 `index_list`의 원소들에 해당하는 인덱스의 글자들을 순서대로 이어 붙인 문자열을 return 하는 solution 함수를 작성해 주세요.

### 입출력 예

| my_string | index_list | result |
| --- | --- | --- |
| "cvsgiorszzzmrpaqpe" | [16, 6, 5, 3, 12, 14, 11, 11, 17, 12, 7] | "programmers" |
| "zpiaz" | [1, 2, 0, 0, 3] | "pizza" |
- 1 ≤ `my_string`의 길이 ≤ 1,000
- `my_string`의 원소는 영소문자로 이루어져 있습니다.
- 1 ≤ `index_list`의 길이 ≤ 1,000
- 0 ≤ `index_list`의 원소 < `my_string`의 길이

- 코드

```jsx
function solution(my_string, index_list) {
    return index_list.reduce((acc, cur) => acc+my_string[cur], "")
}
```

- 다른 사람 코드

```jsx
//1번
function solution(my_string, index_list) {
    var answer = '';

    index_list.map((a)=>{
        answer += my_string[a]
    })

    return answer;
}

//2번
const solution = (my_string, index_list) => {
    const result = [];
    for(let i=0; i<index_list.length; i++){
        result.push(my_string[index_list[i]]);
    }
    return result.join('');
}

//3번
function solution(my_string, index_list) {
    var answer = '';
    for(var i=0; i<index_list.length; i++){
        answer += my_string[index_list[i]];
    }
    return answer;
}
```

- 리듀스를 사용한 방법이 엄청 많았는데 좀 더 빠르게 적용하는 방법을 터특해야겠다.
- 푸시와 조인, 스프릿으로 푸는 방법도 여럿 있었다. 좀 더 연마해야겠다.
- 나는 스프레드 연산자로 문자열을 배열로 만들어서 for문을 돌려 인덱스의 값을 찾으려고 구성하였는데 사람들이 푸는 방식과 매우 흡사했다.