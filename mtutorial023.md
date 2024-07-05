# [코코아팹] 마이크로비트 STEAM 키트 코딩활동 023

```ghost
input.onButtonPressed(Button.B, function () {
    타이머 = 10
    while (타이머 > 0) {
        music.play(music.tonePlayable(262, music.beat(BeatFraction.Eighth)), music.PlaybackMode.InBackground)
        타이머 += -1
        basic.showNumber(타이머)
        basic.pause(500)
    }
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.PowerDown), music.PlaybackMode.UntilDone)
})
let 타이머 = 0
music.setVolume(90)
```

```template
let 타이머 = 0
music.setVolume(90)

```

## 10초 타이머를 만들어 봅시다.
![steam22_2](https://github.com/kocoasolution/mytutorial/assets/170903760/fbffd249-132f-4f9c-96b5-d9cd39075e92)

## (1) B 버튼 입력으로 시작
*  ``||input.A 버튼 누를 때||``를 가져오고, ``||input.B 버튼 누를 때||``으로 바꾸세요.

```blocks
input.onButtonPressed(Button.B, function () {

})
```

## (2) 변수 "타이머"에 10 저장하기
* ``||input.B 버튼 누를 때||``안에 ``||variable.타이머에 0 저장||``를 넣습니다.

* **10초부터 시작**하기 위해 ``||variable.0 저장||``을 ``||variable.10 저장||`` 으로 바꿉니다.

```blocks
input.onButtonPressed(Button.B, function () {
    타이머 = 10
})
```

## (3) 반복하기 블록 
* 이어서 ``||loops.<거짓>인 동안 실행||``을 가져와 넣습니다.

```blocks
input.onButtonPressed(Button.B, function () {
    타이머 = 10
    while (false) {
    	
    }
})
```

## (4) 타이머 > 0 검사하며 반복하기
* ``||variable.타이머||``값이 10 ~ 0 까지 1씩 줄어들어, **0보다 클 때까지 반복**해야 합니다.

* 그래서 ``||loops.<거짓>||``에 ``||variable.타이머||`` ``||logic.> 0||``을 넣습니다.

```blocks
input.onButtonPressed(Button.B, function () {
    타이머 = 10
    while (타이머 > 0) {
    	
    }
})
```

## (5) 소리나게 하기
* 소리가 나게 하기 위해 ``||재생 (도)음을 1박자 동안 재생 [완료될 때까지] ||``를 가져와 넣습니다.
* ``||재생 (도)음을 1박자||``를 ``||재생 (도)음을 1/8박자||``로 바꿔 소리가 좀 짧게 나오게 해주세요.
* 다른 명령블록도 동시에 실행되기 위해 ``||[완료될 때까지]||``를 ``||[배경에서 실행]||``으로 바꾸세요.
```blocks
input.onButtonPressed(Button.B, function () {
    타이머 = 10
    while (타이머 > 0) {
        music.play(music.tonePlayable(262, music.beat(BeatFraction.Eighth)), music.PlaybackMode.InBackground)
    }
})
```

## (6) 변수 타이머 1씩 작아지게 하기
* 이어서 ``||variable.타이머 값 1 증가||``를 넣고 ``||variable.1||``을 ``||variable.-1||``로 바꿉니다.

* 이렇게 하면 변수 ``||variable.타이머||``가 **1씩 작아집니다.**

```blocks
input.onButtonPressed(Button.B, function () {
    타이머 = 10
    while (타이머 > 0) {
        music.play(music.tonePlayable(262, music.beat(BeatFraction.Eighth)), music.PlaybackMode.InBackground)
        타이머 += -1
    }
})
```

## (7) 변수 타이머 숫자값을 LED에 나타내기
* 이어서 ``||basic.숫자 출력(0)||``을 가져옵니다.

* ``||basic.숫자 출력(0)||``에 ``||variable.타이머||``변수를 넣어 **LED에 타이머 숫자값이 나오게** 합니다.

```blocks
input.onButtonPressed(Button.B, function () {
    타이머 = 10
    while (타이머 > 0) {
        music.play(music.tonePlayable(262, music.beat(BeatFraction.Eighth)), music.PlaybackMode.InBackground)
        타이머 += -1
        basic.showNumber(타이머)
    }
})
```

## (8) 잠깐 기다리는 "일시중지" 블록 넣기
* 이어서 ``||basic.일시중지(100)ms||``를 가져옵니다.
* ``||basic.100||``을 ``||basic.500||``으로 바꿔 **LED 표시가 좀 더 길어지게** 해줍니다.
* 100 = 0.1초, 500 = 0.5초 
```blocks
input.onButtonPressed(Button.B, function () {
    타이머 = 10
    while (타이머 > 0) {
        music.play(music.tonePlayable(262, music.beat(BeatFraction.Eighth)), music.PlaybackMode.InBackground)
        타이머 += -1
        basic.showNumber(타이머)
        basic.pause(500)
    }
})
```

## (9) 타이머가 끝난것을 소리로 알리기
* ``||loops.반복||``블록이 끝난 다음에 ``||music.재생 멜로디 (다다둠) 멜로디 [배경에서 실행]||``을 가져와 넣습니다.
* 멜로디 ``||music.(다다둠)||``을 ``||music.(전원 끄는)||``으로 바꾸어 타이머가 끝나는 느낌이 나게 해주세요.

```blocks
input.onButtonPressed(Button.B, function () {
    타이머 = 10
    while (타이머 > 0) {
        music.play(music.tonePlayable(262, music.beat(BeatFraction.Eighth)), music.PlaybackMode.InBackground)
        타이머 += -1
        basic.showNumber(타이머)
        basic.pause(500)
    }
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.PowerDown), music.PlaybackMode.InBackground)
})
```

## (10) 다운로드 및 실행
* 지금까지 완성한 코드를 마이크로비트에 ``|다운로드|``합니다.

* 마이크로비트의 ``||input.B 버튼||``을 눌러 타이머 10초가 잘 작동하는 지 확인해 보세요.

## 끝
* 마지막 페이지 입니다.
