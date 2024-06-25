# [코코아팹] 마이크로비트 STEAM 키트 코딩활동 014

```ghost
input.onButtonPressed(Button.A, function () {
    사람수 += 1
    basic.showNumber(사람수)
})
input.onButtonPressed(Button.B, function () {
    사람수 = 0
    basic.showNumber(사람수)
})
let 사람수 = 0
basic.showNumber(사람수)
basic.forever(function () {
    사람수 += 1
    basic.showNumber(사람수)
})

```

```template
let 사람수 = 0
사람수 = 0
basic.showNumber(사람수)
```

## 버튼이란 무엇일까요?
* ``||input.버튼||``은 **손으로 눌렀을 때** 어떤 **일을 할 수 있게** 해줍니다.

## 마이크로비트에는 A, B 버튼 2개가 있습니다.
![버튼_2](https://github.com/kocoasolution/mytutorial/assets/170903760/4f8a9f9e-e1e2-480f-863c-7c3a1cb115b2)

## 마이크로비트 버튼을 사용하는 방법에 대해서 알아봅시다.
*  **A 버튼을 누르면** ``||input.A 버튼 누를 때||``블록이 실행됩니다.

*  **B 버튼을 누르면** ``||input.B 버튼 누를 때||``블록이 실행됩니다.

~hint 버튼 명령블록 보기
* 아래 **전구**버튼을 눌러보세요.
hint~

```blocks
input.onButtonPressed(Button.A, function () {

})
input.onButtonPressed(Button.B, function () {
    
})
```

## (1-1) A 버튼 누르면 사람 수 커지게 하기 
* ``||input.A 버튼 누를 때||``블록을 가져와 그 안에 ``||사람수 값 1 증가||``를 넣으세요.

* 이어서 ``||basic.숫자 출력(사람수)||``을 넣으세요.

```blocks
input.onButtonPressed(Button.A, function () {
    사람수 += 1
    basic.showNumber(사람수)
})
```



## (1-2) 완성된 코드를 실행해 보세요.
* 만든 코드를 ``|다운로드|`` 하세요.
* ``||input.A 버튼||``을 손으로 눌렀을 때 LED에 **숫자가 커지나요?**

## (2-1) B 버튼 누르면 사람 수 작아지게 하기
* ``||input.B 버튼 누를 때||``블록을 가져와 그 안에 ``||사람수 값 -1 증가||``를 넣으세요.

* 이어서 ``||basic.숫자 출력(사람수)||``을 넣으세요.

```blocks
input.onButtonPressed(Button.B, function () {
    사람수 += -1
    basic.showNumber(사람수)
})
```

## (2-2) 완성된 코드를 실행해 보세요.
* 만든 코드를 ``|다운로드|`` 하세요.
* ``||input.B 버튼||``을 손으로 눌렀을 때 LED에 **숫자가 작아지나요?**


## 개념 정리
* **A 버튼을 누르면** ``||input.A 버튼 누를 때||``블록이 실행됩니다.

* **B 버튼을 누르면** ``||input.B 버튼 누를 때||``블록이 실행됩니다.

```blocks
input.onButtonPressed(Button.A, function () {

})
input.onButtonPressed(Button.B, function () {
    
})
```

## 끝
* 마지막 페이지 입니다.
