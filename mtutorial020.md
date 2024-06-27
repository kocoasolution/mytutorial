# [코코아팹] 마이크로비트 STEAM 키트 코딩활동 020

```ghost
let 동전 = 0
input.onGesture(Gesture.Shake, function () {
    동전 = randint(1, 2)
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
    if (동전 == 1) {
        basic.showLeds(`
            # . . # .
            # . # . #
            # . # . #
            # . # . #
            # . . # .
            `)
    } else {
        basic.showLeds(`
            . . # . .
            . # # # .
            . . # . .
            . # # # .
            # # # # #
            `)
    }
})
```

```template
input.onGesture(Gesture.Shake, function () {
    
})
```

## 마이크로비트로 동전 던지기를 만들어 봅시다.
![coin](https://github.com/kocoasolution/mytutorial/assets/170903760/f2ada1a7-bd8c-4a62-888d-e738ed66c775)

## (1) 랜덤 숫자를 저장할 변수 만들기
*  ``||variable.동전||`` 변수를 하나 만드세요.

* ``||variable.동전에 (0)저장||``을 ``||input.흔들림 감지될 때||``에 넣습니다.

```blocks
let 동전 = 0
input.onGesture(Gesture.Shake, function () {
    동전 = 0
})
```

## (2) 마이크로비트를 흔들면 랜덤 숫자 저장하기
* ``||math.(0)부터 (10)사이 랜덤||``을 ``||variable.동전에 (0) 저장||``에 넣습니다.
* 동전은 앞/뒤, 이렇게 2가지만 있습니다.
* 그래서 ``||math.(0)부터 (10)사이 랜덤||``을 ``||math.(1)부터 (2)사이 랜덤||``으로 바꿉니다.

```blocks
let 동전 = 0
input.onGesture(Gesture.Shake, function () {
    동전 = randint(1, 2)
})
```

## (3) 흔들면 소리 나오게 하기 
* 이어서 ``||music.재생(멜로디 다다둠 멜로디) [배경에서 실행]||``을 넣습니다.

* ``||music.다다둠 멜로디||``를 ``||music.바 딩 멜로디||``로 바꿉니다.

```blocks
let 동전 = 0
input.onGesture(Gesture.Shake, function () {
    동전 = randint(1, 2)
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
})
```

## (4) 만약~ 조건문
* 랜덤 숫자가 **1이면 동전 뒷면**, **2면 동전 앞면**을 나타내기 위해 ``||logic.조건문||``이 필요합니다. 
* ``||logic.만약<참>이면, 아니면||``을 ``||input.흔들림 감지될 때||``안에 넣습니다.

```blocks
let 동전 = 0
input.onGesture(Gesture.Shake, function () {
    동전 = randint(1, 2)
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
    if (true) {
    	
    } else {
    	
    }
})
```
## (5) 동전 LED 표시 모습
![동전앞뒤면2](https://github.com/kocoasolution/mytutorial/assets/170903760/7d7769c3-8adc-4c24-87e4-a151331bba82)


## (6) 동전 뒷면 나타내기
* **``||variable.동전||``= 1 **이면 LED에 숫자 **10**을 나타냅니다.(동전 뒷면)
* **숫자 10**은 ``||basic.LED 출력||``으로 새롭게 만듭니다.

```blocks
let 동전 = 0
input.onGesture(Gesture.Shake, function () {
    동전 = randint(1, 2)
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
    if (동전 == 1) {
        basic.showLeds(`
            # . . # .
            # . # . #
            # . # . #
            # . # . #
            # . . # .
            `)
    } else {
    	
    }
})
```

## (7) 동전 앞면 나타내기 
* **``||variable.동전||``= 0 **이면 LED에 **다보탑**을 나타냅니다.(동전 앞면)
* **다보탑**은 ``||basic.LED 출력||``으로 새롭게 만듭니다.

```blocks
let 동전 = 0
input.onGesture(Gesture.Shake, function () {
    동전 = randint(1, 2)
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
    if (동전 == 1) {
        basic.showLeds(`
            # . . # .
            # . # . #
            # . # . #
            # . # . #
            # . . # .
            `)
    } else {
        basic.showLeds(`
            . . # . .
            . # # # .
            . . # . .
            . # # # .
            # # # # #
            `)
    }
})

```
## (8) 실행해보기
* 완성된 코드를 ``|다운로드|`` 합니다.
* 마이크로비트를 흔들었을 때 동전 앞, 뒤면이 랜덤하게 잘 표현되나요?

## 끝
* 마지막 페이지 입니다.
