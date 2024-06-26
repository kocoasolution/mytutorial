# [코코아팹] 마이크로비트 STEAM 키트 코딩활동 018

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
걸음수 = 0
```

```template
let 걸음수 = 0
걸음수 = 0
```

## 디지털 만보기를 만들어 봅시다.
![그림2](https://github.com/kocoasolution/mytutorial/assets/170903760/0fbb33fe-b73f-4e88-8138-0eeddbea1cae)

## (1) 흔들림을 감지하는 블록 가져오기
* ``||input.흔들림 감지될 때||``을 가져오세요.

* 이 블록은 마이크로비트가 **흔들리면** 실행됩니다.

```blocks
input.onGesture(Gesture.Shake, function () {

})
```


## (2) 걸음수 세기
* 마이크로비트가 **흔들림이 감지되면** 변수 ``||variable.걸음수||``값이 증가되어야 합니다.

* ``||variable.걸음수 값 (1)증가||``를 가져와 ``||input.흔들림 감지될 때||``안에 넣습니다.

```blocks
input.onGesture(Gesture.Shake, function () {
    걸음수 += 1
})
```

## (3) 걸음수 세기
* **걸음수**를 LED에 숫자로 나타내기 위해 ``||basic.숫자 출력(0)||``을 가져와 넣습니다.

* 그리고  ``||basic.(0)||``부분에 변수 ``||variable.걸음수||``를 넣으세요.

```blocks
input.onGesture(Gesture.Shake, function () {
    걸음수 += 1
    basic.showNumber(걸음수)
})
```

## (4) A+B 버튼 누를 때
* **A,B버튼을 동시에 누르면** ``||variable.걸음수||``를 **0부터 다시 시작**하게 해봅시다.

* ``||input.A 버튼 누를 때||``를 가져와 ``||input.A+B 버튼 누를 때||``로 바꾸세요.

```blocks
input.onButtonPressed(Button.AB, function () {

})
```

## (5) 소리 내기 
* ``||music.재생 (도)음을 1박자 동안 재생 [완료될 때까지]||``을 가져오세요.

* ``||music.[완료될 때까지]||``를 ``||music.[배경에서 실행]||``으로 바꾸고 ``||input.A+B 버튼 누를 때||``에 넣습니다.

~hint("배경에서 실행"의미)
* "완료될 때까지"로 하면, 음악소리가 다 끝날때까지 다른 명령블록이 실행되지 않습니다.
* "배경에서 실행"을 하면, 음악소리가 끝나지 않아도 다른 명령블록이 같이 실행됩니다.
hint~

```blocks
input.onButtonPressed(Button.AB, function () {
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.InBackground)
})
```

## (6) 걸음수 0부터 다시 시작
* ``||variable.걸음수에 (0) 저장||``을 ``||input.A+B 버튼 누를 때||``에 넣습니다.

* 그 다음 ``||basic.숫자 출력(0)||``도 넣고 ``||basic.(0)||``에 변수``||variable.걸음수||``를 끼워 넣습니다.

```blocks
input.onButtonPressed(Button.AB, function () {
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.InBackground)
    걸음수 = 0
    basic.showNumber(걸음수)
})
```
## (7) 이제 다운로드해서 실행해 봅니다.
* 코드를 ``|다운로드|``합니다.
* 마이크로비트를 흔들때 걸음수가 LED에 나타나는지 확인하세요.
* ``||input.A+B 버튼||``을 누르면 **걸음수가 0이 되는지** 확인하세요.

## (8) 휴대해서 걸어보기
* 마이크로비트에 **건전지를 연결하고 주머니에 넣어** 걸어봅시다.
* 걷기가 끝난 후, 마이크로비트에 나타난 걸음수를 확인해 봅시다.

~hint(걸음수 비교하기)
* 내가 센 걸음수와 마이크로비트에 표시된 걸음수가 똑같나요? 다르다면 왜 그럴까요?
hint~


## 끝
* 마지막 페이지 입니다.
