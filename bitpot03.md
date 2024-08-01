# 코코아팹 비트팟 코딩활동 03

```ghost
function 멜로디3 () {
    music.play(music.stringPlayable("A F E F D G E F ", 120), music.PlaybackMode.UntilDone)
    music.play(music.stringPlayable("E B C5 A B G A F ", 120), music.PlaybackMode.UntilDone)
    music.play(music.stringPlayable("A F E F D G E F ", 120), music.PlaybackMode.UntilDone)
}
input.onLogoEvent(TouchButtonEvent.Pressed, function () {
 
})
input.onButtonPressed(Button.A, function () {
    if (순서 > 0) {
        순서 += -1
    }
    basic.showString("" + (순서))
})

input.onButtonPressed(Button.B, function () {
    
})
let 순서 = 0
music.setVolume(50)
basic.showString("" + (순서))

```

```template
function 멜로디3 () {
    music.play(music.stringPlayable("A F E F D G E F ", 120), music.PlaybackMode.UntilDone)
    music.play(music.stringPlayable("E B C5 A B G A F ", 120), music.PlaybackMode.UntilDone)
    music.play(music.stringPlayable("A F E F D G E F ", 120), music.PlaybackMode.UntilDone)
}

input.onButtonPressed(Button.A, function () {
    if (순서 > 0) {
        순서 += -1
    }
    basic.showString("" + (순서))
})
function 멜로디2 () {
    music.play(music.stringPlayable("C5 B A G F E D C ", 120), music.PlaybackMode.UntilDone)
    music.play(music.stringPlayable("C D E F G A B C5 ", 120), music.PlaybackMode.UntilDone)
    music.play(music.stringPlayable("C5 B A G F E D C ", 120), music.PlaybackMode.UntilDone)
}
function 멜로디1 () {
    music.play(music.stringPlayable("C C G G A A G - ", 120), music.PlaybackMode.UntilDone)
    music.play(music.stringPlayable("F F E E D D C - ", 120), music.PlaybackMode.UntilDone)
    music.play(music.stringPlayable("G G F F E E D - ", 120), music.PlaybackMode.UntilDone)
    music.play(music.stringPlayable("G G F F E E D - ", 120), music.PlaybackMode.UntilDone)
    music.play(music.stringPlayable("C C G G A A G - ", 120), music.PlaybackMode.UntilDone)
    music.play(music.stringPlayable("F F E E D D C - ", 120), music.PlaybackMode.UntilDone)
}
input.onButtonPressed(Button.B, function () {
    if (순서 < 2) {
        순서 += 1
    }
    basic.showString("" + (순서))
})
let 순서 = 0
music.setVolume(50)
basic.showString("" + (순서))

```

## 이번 주제
* 이번에는 **버튼 A, B로** 멜로디를 고르고, **로고 터치센서를** 누르면 멜로디가 흘러나오게 해봅시다.


## 1.로고 터치센서를 누를 때
* ``||input.로고 누를 때||``블럭을 가져옵니다.

```blocks
input.onLogoEvent(TouchButtonEvent.Pressed, function () {
	
})
```

## 2.첫번째 멜로디 재생
* **변수 ``||variables.순서||`` = 0 ** 이면 ``||function.함수호출 멜로디1||``을 실행합니다.

```blocks
input.onLogoEvent(TouchButtonEvent.Pressed, function () {
    if (순서 == 0) {
        함수호출_멜로디1_
    }
})
```

## 3.두번째, 세번째 멜로디 재생
* **변수 ``||variables.순서||`` = 1 **이면 ``||function.함수호출 멜로디2||``을 실행합니다.

* **변수 ``||variables.순서||`` = 2 ** 이면 ``||function.함수호출 멜로디3||``을 실행합니다.


```blocks
input.onLogoEvent(TouchButtonEvent.Pressed, function () {
    if (순서 == 0) {
        함수호출_멜로디1_
    }
    if (순서 == 1) {
        함수호출_멜로디2_
    }
    if (순서 == 2) {
        함수호출_멜로디3_
    }
})
```

## 코드 다운로드 하기
* 모든 코드를 완성했으니, ``|다운로드|``를 눌러 코드를 마이크로비트로 다운받으세요.

* **버튼 A, B**로 멜로디를 선택하고, **로고를 터치**하여 멜로디가 잘 나오는지 확인해 보세요.

## 끝
* 마지막 페이지 입니다.
