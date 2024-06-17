# 코코아팹 마이크로비트 코딩활동 011

```ghost
basic.forever(function () {
    basic.showIcon(IconNames.Square)
    basic.pause(100)
    basic.showIcon(IconNames.SmallSquare)
    basic.pause(100)
    basic.showLeds(`
        . . . . .
        . . . . .
        . . # . .
        . . . . .
        . . . . .
        `)
    basic.pause(100)
    images.createImage(`
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        . . . . .
        `).scrollImage(1, 200)
})
```


## 연습문제 (006~010)
* 다음 화면으로 넘어가면서 문제를 해결해 봅시다.

## [문제1] 미세먼지 상태를 LED 표정으로 나타내는 아래의 동작을 만들어 보세요.
![011_1](https://github.com/kocoasolution/mytutorial/assets/170903760/b053f307-af76-45a3-b693-51efb63c28c6)

## [문제2] 아래의 동작을 만들어 보세요.
* ```||basic.LED 출력||```을 먼저 사용하고, 없는 그림은 ```||basic.LED 출력||```으로 직접 그리세요.
* ![011_2](https://github.com/kocoasolution/mytutorial/assets/170903760/da3df46c-89d7-469c-aa64-cebb32ad71f9)

## [문제3] 아래와 같은 엘레베이터 화살표 동작을 만들어 보세요.
![011_3](https://github.com/kocoasolution/mytutorial/assets/170903760/e013f3e8-c426-4ae7-9948-785467e71221)

## 끝
* 모두 완료했습니다.
