# TIL #15

글쓴이: 블루 blue
생성 일시: 2023년 7월 8일 오전 11:13
최종 편집 일시: 2023년 7월 8일 오전 11:39

# 프로그래머스 레벨0 정복기

- 홀짝 구분하기
    - 자연수 `n`이 입력으로 주어졌을 때 만약 `n`이 짝수이면 "`n` is even"을, 홀수이면 "`n` is odd"를 출력하는 코드를 작성해 보세요.

```tsx
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    n = Number(input[0]);
    if (n % 2 === 0) {
     answer = "even";
    } else {
     answer = "odd";
    }
    let result = `${n} is ${answer}`;
    console.log(result);
});
```

- 처음에 **Output size differs 오류가 생겨 매우 많은 시도를 했다. 삼항연산자도 써보고 구글링도 해보았다.**
- 해결방안을 찾다가 프로그래머스에서 이미 만들어진 원인은 이미 만들어진 readline에 코딩을 했어야했는데 나는 다 지우고 새로 하나 만들었기 때문에 생긴 오류였다.

```tsx
//1번
const result = Number(line) % 2 ? 'odd' : 'even'
    console.log(line, 'is', result)
```

- 예상대로 삼항연산자 혹은 if문을 사용하여 표현하였다.