### @activities true


# [코코아팹] 마이크로비트 STEAM 키트 코딩활동 021

```ghost
input.onButtonPressed(Button.A, function () {
    strip.showColor(neopixel.colors(NeoPixelColors.Red))
})
let strip: neopixel.Strip = null
strip = neopixel.create(DigitalPin.P1, 4, NeoPixelMode.RGB)
basic.forever(function () {
	
})

```

```template
input.onButtonPressed(Button.A, function () {
})


```

## 오늘의 주제
### 오늘의 주제 @unplugged
이번시간에는 ooo에 대해서 알아보겠습니다.
![WS2812_LED](https://github.com/kocoasolution/mytutorial/assets/170903760/963b349f-9128-4ce1-9b62-f05f151cdfc2)


### 마이크로비트를 컴퓨터에 연결하기 @unplugged
* USB 케이블을 이용해 마이크로비트를 컴퓨터에 연결하세요
* 연결을 완료했으면 ``||logic.확인||``을 누르세요.


## 마이크로비트로 가위-바위-보를 만들어 봅시다.
* 아래와 같이 일부 코드가 만들어진 상태에서 시작합니다.
* 아래 ``||input.흔들림 감지될 때||``에서 코딩을 시작하면 됩니다.

## (1) 랜덤 숫자 1~3으로 범위 정하기 
*  **가위,바위,보 3가지 경우**가 있으므로, ``||math.1부터 3사이 랜덤||``으로 바꿔주세요.

* **``||variable.숫자||``= 1은 가위, ``||variable.숫자||``= 2는 바위, ``||variable.숫자||``= 3은 보** 입니다.

```blocks
let 숫자 = 0
input.onGesture(Gesture.Shake, function () {
    숫자 = randint(1, 3)
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
})
```


## (9) 마지막 실행해보기
* 지금까지 만든 코드를 ``|다운로드|`` 합니다.
* 마이크로비트 **로고를 누른 상태에서 흔들었을 때** 가위,바위,보가 잘 표현되나요?
* 마이크로비트 **로고를 안 누른 상태에서 흔들었을 때**는 작동이 안되는지 확인해 보세요.

## 끝
* 마지막 페이지 입니다.
