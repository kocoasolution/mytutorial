# [코코아팹] 마이크로비트 STEAM 키트 코딩활동 019

```ghost
input.onGesture(Gesture.Shake, function () {
    걸음수 += 1
    basic.showNumber(걸음수)
})
input.onButtonPressed(Button.AB, function () {
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.InBackground)
    걸음수 = 0
    basic.showNumber(걸음수)
})
let 걸음수 = 0
걸음수 = randint(0, 10)
basic.forever(function () {
	
})

```


## (1) 12면체 디지털 주사위 만들기
* 흔들면 **1~12**까지 숫자가 표시되는 **12면체 주사위**를 마이크로비트로 만들어 보세요.
![12면체_2](https://github.com/kocoasolution/mytutorial/assets/170903760/a528343a-1e87-47b6-b8fe-6c4bdf2c5ccc)


## (2) 흔들면 랜덤하게 소리 나오기
* 아래 **전구모양**을 클릭하고, 코드를 따라 만들어 봅시다.
* **랜덤 숫자**의 범위를 **131(낮은도) ~ 988(높은시)**로 바꾸고 ``|다운로드|``한뒤, 마이크로비트를 흔들어 봅시다.

```blocks
input.onGesture(Gesture.Shake, function () {
    music.play(music.tonePlayable(randint(0, 10), music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
})```

## 끝
* 마지막 페이지 입니다.
