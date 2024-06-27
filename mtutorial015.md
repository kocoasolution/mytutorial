# [코코아팹] 마이크로비트 STEAM 키트 코딩활동 015

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

```

```template
input.onButtonPressed(Button.A, function () {
    사람수 += 1
    basic.showNumber(사람수)
})
input.onButtonPressed(Button.B, function () {
    사람수 += -1
    basic.showNumber(사람수)
})
let 사람수 = 0
사람수 = 0
basic.showNumber(사람수)

```

## 디지털 계수기에 아래 2가지 기능을 추가해봅시다.
1. 숫자를 **0으로 되돌리는** 기능을 추가하세요.

2. 버튼을 누를 때마다 **소리**가 나오게 하세요.

## (1-1) "A버튼 누를 때"를 가져와, A+B로 바꾸기 
![버튼AB_2](https://github.com/kocoasolution/mytutorial/assets/170903760/92068c91-4f63-448d-859d-7c66cfe62d8a)

```blocks
input.onButtonPressed(Button.AB, function () {

})
```

## (1-2) A+B버튼을 누르면 사람수 0 되게 하기 
*  ``||input.A+B 버튼 누를 때||``블록 안에 ``||variable.사람수에 0 저장||``을 넣습니다.

* 이어서 ``||basic.숫자 출력(사람수)||``을 넣으세요. 

```blocks
input.onButtonPressed(Button.AB, function () {
    사람수 = 0
    basic.showNumber(사람수)
})
```

## (1-3) 코드를 다운로드 받고 실행해 봅시다. 
* 만든 코드를 ``|다운로드|`` 하세요.

* ``||input.A 버튼||``을 몇 번 누른 후, ``||input.A+B 버튼||``을 **동시에** 눌렀을 때 **0 이 되나요?**

```blocks
input.onButtonPressed(Button.A, function () {
    사람수 += 1
    basic.showNumber(사람수)
})
input.onButtonPressed(Button.AB, function () {
    사람수 = 0
    basic.showNumber(사람수)
})
input.onButtonPressed(Button.B, function () {
    사람수 += -1
    basic.showNumber(사람수)
})
let 사람수 = 0
사람수 = 0
basic.showNumber(사람수)

```

## (2-1) 이제 소리가 나오게 해봅시다. 
* 버튼 누를 때 **소리가 나오면** 디지털 계수기가 **잘 작동하는 지** 쉽게 알 수 있습니다.

* ``||input.A 버튼||``, ``||input.B 버튼||``, ``||input.A+B 버튼||``을 누를 때 **서로 다른 소리가** 나오게 해봅시다.

## (2-2) [음악] 도구상자에서 소리 크기 정하기
*  ``||music.음악||``에서 ``||music.음량을 (127)로 설정||``을 가져와 ``||basic.시작하면||``에 넣어주세요.

* 음량 숫자값 **127**을 **100**으로 바꾸세요.

~hint(음량 숫자의 뜻)
* 숫자가 클수록 소리도 커지고, 숫자가 작을수록 소리가 작아집니다.
hint~

```blocks
let 사람수 = 0
사람수 = 0
basic.showNumber(사람수)
music.setVolume(100)
```

## (2-3) A버튼을 누르면 "도"소리가 나오게 해보기
* ``||music.재생 (도)음을 1박자 동안 재생 [완료될 때까지]||``를 가져와 ``||input.A 버튼 누를 때||``안에 넣습니다.

* ``||music.[완료될 때까지]||``를 ``||music.[배경에서 실행]||``으로 바꿉니다.

~hint(배경에서 실행이란?)
* **배경에서 실행**은 소리가 끝날 때 까지 기다리지 않고 다른 명령블록과 거의 동시에 실행하는 설정입니다.
hint~

```blocks
input.onButtonPressed(Button.A, function () {
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.InBackground)
    사람수 += 1
    basic.showNumber(사람수)
})
```

## (2-4) B버튼을 누르면 "솔"소리가 나오게 해보기
* ``||music.재생 (도)음을 1박자 동안 재생 [완료될 때까지]||``를 가져와 ``||input.B 버튼 누를 때||``안에 넣습니다.

* ``||music.도||``를 ``||music.솔||``로 바꾸고, ``||music.[완료될 때까지]||``를 ``||music.[배경에서 실행]||``으로 바꿉니다.

```blocks
input.onButtonPressed(Button.B, function () {
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.InBackground)
    사람수 += -1
    basic.showNumber(사람수)
})
```

## (2-5) A+B버튼을 누르면 "시"소리가 나오게 해보기
* ``||input.A+B버튼||``을 누르면 **"시"** 소리가 나게 만들어 보세요.

~hint(힌트)
* 앞에 (2-4)를 다시 보세요.
hint~
```blocks
input.onButtonPressed(Button.AB, function () {
    music.play(music.tonePlayable(494, music.beat(BeatFraction.Whole)), music.PlaybackMode.InBackground)
    사람수 = 0
    basic.showNumber(사람수)
})
```

## (2-6) 이제 코드를 다운로드 받고 실행해 봅시다. 
* 만든 코드를 ``|다운로드|`` 하세요.

* ``||input.버튼A||``, ``||input.버튼B||``, ``||input.버튼A+B||``를 누를 때 소리가 잘 나오나요?

## 개념 정리
* **A와 B 버튼을 동시에 누르면** ``||input.A+B 버튼 누를 때||``블록이 실행됩니다.

* **도레미~ 소리를 내려면** ``||music.재생 (도)음을 1박자 동안 재생 [완료될 때까지]||``블록을 사용하면 됩니다.

```blocks
input.onButtonPressed(Button.A+B, function () {

})
music.play(music.tonePlayable(494, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
```

## 끝
* 마지막 페이지 입니다.
