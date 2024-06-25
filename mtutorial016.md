# [코코아팹] 마이크로비트 STEAM 키트 코딩활동 016

```ghost
input.onButtonPressed(Button.A, function () {
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.InBackground)
    사람수 += 1
    basic.showNumber(사람수)
})
input.onButtonPressed(Button.AB, function () {
    music.play(music.tonePlayable(494, music.beat(BeatFraction.Whole)), music.PlaybackMode.InBackground)
    사람수 = 0
    basic.showNumber(사람수)
})
input.onButtonPressed(Button.B, function () {
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.InBackground)
    사람수 += -1
    basic.showNumber(사람수)
})
let 사람수 = 0
사람수 = 0
basic.showNumber(사람수)
music.setVolume(100)
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
    basic.showString("Hello!")
    basic.pause(100)
})

```

## 연습문제(012~015)
* 다음 화면으로 넘어가면서 문제를 해결해 봅시다.

## [문제1] A,B버튼에 따라 표정이 달라지는 아래의 동작을 만들어 보세요.
![ch3_ex2](https://github.com/kocoasolution/mytutorial/assets/170903760/a9d39a4a-0d3b-445f-85af-2eee09289c23)

~hint(힌트)
* A 버튼 누를 때, B 버튼 누를 때를 사용합니다.
hint~

```blocks
input.onButtonPressed(Button.A, function () {
   "아이콘 출력(웃는 얼굴)"
})
input.onButtonPressed(Button.B, function () {
   "아이콘 출력(우는 얼굴)"
})
```

## [문제2] A 버튼을 누르면 상자개수가 커지는 동작을 만들어 보세요.
* ``||상자개수||``라는 **변수**를 만드세요. 이 변수 값은 **0부터 시작**합니다.

* **A 버튼을 누르면** ``||상자개수||``가 **1씩 커지고** **LED**에 변수 값이 나타나게 하세요.

```blocks
상자개수 = 0
input.onButtonPressed(Button.A, function () {
    상자개수 += 1
    "상자개수를 LED에 숫자로 출력하기 "
})
```

## [문제3] 앞 문제 2번에 이어서, B 버튼을 누르면 상자개수가 0이 되는 동작을 만들어 보세요.
* **B 버튼을 누르면** ``||상자개수||``가 **0이 되고** **LED**에 변수 값이 나타나게 하세요.

* **B 버튼을 누르면** 계이름 **"파"** 소리도 발생합니다.

```blocks
input.onButtonPressed(Button.B, function () {
    "파 소리가 난다."
    "상자개수 값이 0 이 된다. "
    "상자개수를 LED에 숫자로 출력한다. "
})
```

## 끝
* 마지막 페이지 입니다.
