# [코코아팹] 마이크로비트 STEAM 키트 코딩활동 021

```ghost
let 숫자 = 0
input.onGesture(Gesture.Shake, function () {
    if (input.logoIsPressed()) {
        숫자 = randint(0, 10)
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
        if (숫자 == 1) {
            basic.showIcon(IconNames.Scissors)
        } else if (숫자 == 2) {
            basic.showIcon(IconNames.SmallSquare)
        } else {
            basic.showIcon(IconNames.Square)
        }
    }
})

```

```template
let 숫자 = 0
input.onGesture(Gesture.Shake, function () {
    숫자 = randint(0, 10)
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
})

```

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

## (2) 조건문 가져오기 
* ``||logic.만약~이면,아니면||``을 가져와 **(+)버튼을 한 번 눌러** 조건창을 늘리세요.

```blocks
let 숫자 = 0
input.onGesture(Gesture.Shake, function () {
    숫자 = randint(1, 3)
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
    if (true) {
    	
    } else if (false) {
    	
    } else {
    	
    }
})
```
## (3) 가위,바위,보 모양은 아래와 같습니다.
![RPS_2](https://github.com/kocoasolution/mytutorial/assets/170903760/da4790ea-d809-4391-819b-072a1cff12e5)


## (4) 가위,바위,보 LED 아이콘 출력 
* **``||variable.숫자||``= 1은 가위, ``||variable.숫자||``= 2는 바위, ``||variable.숫자||``= 3은 보** 로 코딩합니다.

```blocks
let 숫자 = 0
input.onGesture(Gesture.Shake, function () {
    숫자 = randint(1, 3)
    music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
    if (숫자 == 1) {
        basic.showIcon(IconNames.Scissors)
    } else if (숫자 == 2) {
        basic.showIcon(IconNames.SmallSquare)
    } else {
        basic.showIcon(IconNames.Square)
    }
})
```

## (5) 잠깐 실행해보기
* 지금까지 만든 코드를 ``|다운로드|`` 합니다.
* 마이크로비트를 흔들었을 때 **가위,바위,보**가 잘 표현되나요?

## (6) 로고 터치시 작동되게 만들기
* 마이크로비트를 **조금만 흔들어도** 작동되는 것이 싫습니다.

* 마이크로비트 **로고를 손으로 누르면 작동**되게끔 ``|다음|``으로 넘어가서 조건을 더 추가합시다.

## (7) 만약~ 조건문 가져오기
* ``||input.흔들림 감지될 때||``안에 있는 모든 블록들을 ``||logic.만약<참>이면||``로 감싸줍니다.

```blocks
let 숫자 = 0
input.onGesture(Gesture.Shake, function () {
    if (true) {
        숫자 = randint(1, 3)
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
        if (숫자 == 1) {
            basic.showIcon(IconNames.Scissors)
        } else if (숫자 == 2) {
            basic.showIcon(IconNames.SmallSquare)
        } else {
            basic.showIcon(IconNames.Square)
        }
    }
})

```

## (8) 조건창에 "로고눌림" 넣기
* 마이크로비트 **로고가 눌리면** 실행되는 조건을 추가하겠습니다.

* ``||logic.만약<참>이면||``의 ``||<참>||`` 조건에 ``||input.로고 눌림||``을 넣으세요.

```blocks
let 숫자 = 0
input.onGesture(Gesture.Shake, function () {
    if (input.logoIsPressed()) {
        숫자 = randint(1, 3)
        music._playDefaultBackground(music.builtInPlayableMelody(Melodies.BaDing), music.PlaybackMode.InBackground)
        if (숫자 == 1) {
            basic.showIcon(IconNames.Scissors)
        } else if (숫자 == 2) {
            basic.showIcon(IconNames.SmallSquare)
        } else {
            basic.showIcon(IconNames.Square)
        }
    }
})
```


## (9) 마지막 실행해보기
* 지금까지 만든 코드를 ``|다운로드|`` 합니다.
* 마이크로비트 **로고를 누른 상태에서 흔들었을 때** 가위,바위,보가 잘 표현되나요?
* 마이크로비트 **로고를 안 누른 상태에서 흔들었을 때**는 작동이 안되는지 확인해 보세요.

## 끝
* 마지막 페이지 입니다.
