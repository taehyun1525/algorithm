# TIL #12

글쓴이: 블루 blue
생성 일시: 2023년 7월 4일 오전 10:34
최종 편집 일시: 2023년 7월 4일 오전 11:48

# 프로그래머스 레벨 0 정복하기

- 문자열 정수의 합
    - 한 자리 정수로 이루어진 문자열 `num_str`이 주어질 때, 각 자리수의 합을 return하도록 solution 함수를 완성해주세요.
    
    - 내 코드
    
    ```jsx
    function solution(num_str) {
        return [...num_str].reduce((acc, cur) => acc+ Number(cur),0);
    }
    ```
    
    - 스프레드 연산자로 배열을 끌고와서
    - reduce 매개변수로 초기값 숫자열 0에
    - 더할 값을 Number함수로 숫자열로 변환해서 더해줌
    - for문을 사용하려다가 reduce와 스프레드 연산자를 공부할 겸 사용해보았다. 중간에 하다가 잘 몰라서 다른 사람코드를 살짝 인용하였다.
    
    - 다른 사람 코드
    
    ```jsx
    //1번
    function solution(num_str) {
        var answer = 0;
    
        num_str.split("").map((a)=>answer+=Number(a))
    
        return answer;
    }
    
    //2번
    
    function solution(num_str) {
        return [...num_str].reduce((a, c) => a + +c, 0)
    }
    
    //3번
    
    function solution(num_str) {
        var answer = 0;
    
        num_str.split('');
    
        for(let i = 0; i < num_str.length; i++){
            answer += parseInt(num_str[i])
        }
    
        return answer;
    }
    ```
    

### 부분 문자열

- 어떤 문자열 A가 다른 문자열 B안에 속하면 A를 B의 부분 문자열이라고 합니다. 예를 들어 문자열 "abc"는 문자열 "aabcc"의 부분 문자열입니다. 문자열 `str1`과 `str2`가 주어질 때, `str1`이 `str2`의 부분 문자열이라면 1을 부분 문자열이 아니라면 0을 return하도록 solution 함수를 완성해주세요.

- 제한 사항
    - 1 ≤ `str1` ≤ `str2` ≤ 20
    - `str1`과 `str2`는 영어 소문자로만 이루어져 있습니다.
    
- 

```jsx
function solution(str1, str2) {
    return str2.includes(str1) ? 1:0;
}
```