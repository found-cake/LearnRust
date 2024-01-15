# LearnRust

## Hello, Rust

러스트에서는 반드시  main 함수를 만들어야 함

println뒤에 !가 있어서 찾아보았는데 뒤에 !가 있으면 일반 함수가 아니라 매크로로 정의된 것
매크로에 대한 것은 나중에!!

```rust
fn main() {// main 함수!!!
    println!("Hello, Rust");
}
```

## Print

출력할 문자열 안에 변수를 넣어 출력할 부분을 `{}` 을 넣어주고 다음 파라미터에 순서대로 변수를 넣어주된다.

```rust
fn main() {
    let fruit = "바나나";
    let price = 300;
    println!("{} 가격 = {}원", fruit, price);
}
```

## 사칙연산

다른 언어와 같기 때문에 설명 생

```rust
fn main() {
    println!("{}", 10 + 20);
    println!("{}", 10 - 20);
    println!("{}", 10 * 20);
    println!("{}", 10 / 20);
    println!("{}", 10 % 20);
}
```

## if 문

rust에서 if else문을 보면 python과 유사하다는 느낌이 많이 든다. `:` 이 아닌 `{}` 으로 처리한다는 차이 정도만 있다.

논리를 처리할때 and를 하고 싶으면 && or을 하고 싶으면 ||을 사용하면 된다.

```rust
fn main() {
    let a = 10;
    let b = 20;

    if a == b {
        println!("a와 b는 같습니다.");
    } else if a < b {
        println!("a가 b보다 작습니다.");
    } else {
        println!("a가 b보다 큽니다.");
    }
}
```

## for 문

rust의 for문을 보면 약간 python에 for in range문이 생각난다. 

`range(1, 10)` 으로 했던 것을 `1..10` 이런식으로 하면 된다.

```rust
fn main() {
    for i in 1..10 {
        print!("{}", i)
    }
}
```

```bash
123456789
```

### for문을 활용한 구구단

```rust
fn main() {
    for y in 1..10 {
        for x in 2..10 {
            print!("{} * {} = {:2}\t", x, y, x * y)
        }
        println!()
    }
}
```


## FizzBuzz

지금까지 공부한 것 가지고 문제를 한 번 풀어보자

```
3의 배수일때는 Fizz
5의 배수일때는 Buzz
두 조건 만족시 FizzBuzz를 출력
위 조건을 만족하는 1에서 100까지 순서대로 출력하는 프로그램을 작성
```
[풀이](https://github.com/found-cake/FizzBuzz-rust)
