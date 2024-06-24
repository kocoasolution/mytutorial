# 코코아팹 마이크로비트 코딩활동 017

```ghost
input.onGesture(Gesture.Shake, function () {
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
    basic.showNumber(randint(1, 6))
})
```

```template
basic.forever(function () {
	
})
```

## 디지털 주사위를 만들어 봅시다.
* (그림1)

## (1-1) 마이크로비트 흔들림 감지 블록 가져오기
* 마이크로비트는 **흔들림**을 감지 할 수 있습니다.

* ``||input.흔들림 감지될 때||`` 블록을 가져옵니다.

```blocks
input.onGesture(Gesture.Shake, function () {
   
})
```

## (1-2) 숫자 출력 블록 넣기
* ``||input.흔들림 감지될 때||`` 블록안에 ``||basic.숫자 출력(0)||`` 블록을 넣어주세요.

```blocks
input.onGesture(Gesture.Shake, function () {
    basic.showNumber(0)
})
```

## (1-3) 랜덤숫자를 LED에 출력해 줍니다.
* ``||Math.0 부터 10 사이 랜덤||``을 가져와 ``||basic.숫자 출력(0)||`` 블록의 ``||basic.0||`` 안에 넣어줍니다.

* ``||Math.0 부터 10 사이 랜덤||``블록의 ``||Math.0||``=>``||1||``로,  ``||Math.10||``=>``||6||``으로 바꿔서 주사위 **1~6** 사이의 랜덤수가 나오게 해주세요.  

```blocks
input.onGesture(Gesture.Shake, function () {
    basic.showNumber(randint(1, 6))
})
```

## (1-4) 주사위 코드가 모두 완성되었습니다.
* 완성된 코드를 ``|다운로드|``하세요.
* 마이크로비트를 **흔들어** 보세요. **1~6** 사이의 LED 숫자가 **랜덤**하게 나오나요?

```blocks
input.onGesture(Gesture.Shake, function () {
    basic.showNumber(randint(1, 6))
})
```

## (기능추가) 소리가 나오게 해봅시다. 
* ``||music.재생 멜로디 다다둠 멜로디 [배경에서 실행]||``을 가져와 ``||input.흔들림 감지될 때||`` 블록 **첫번째** 줄에 넣으세요.

* ``||music.다다둠 멜로디||``를 ``||music.바 딩 멜로디||``로 바꿔주세요.

* 코드를 ``|다운로드|``하고 마이크로비트를 **흔들었**을 때 **소리가 같이 나오는지** 확인해 보세요.

```blocks
input.onGesture(Gesture.Shake, function () {
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
    basic.showNumber(randint(1, 6))
})
```

## 끝
* 마지막 페이지 입니다.
