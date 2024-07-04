# [코코아팹] 마이크로비트 STEAM 키트 코딩활동 022

```ghost
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        music.play(music.tonePlayable(262, music.beat(BeatFraction.Half)), music.PlaybackMode.InBackground)
        basic.showIcon(IconNames.Heart)
        music.play(music.tonePlayable(349, music.beat(BeatFraction.Half)), music.PlaybackMode.InBackground)
        basic.showIcon(IconNames.SmallHeart)
    }
    basic.clearScreen()
})
```

```template
music.setVolume(90)

```

## 소리내며 하트를 움직이는 동작을 4번 반복해 봅시다.
![steam22_1](https://github.com/kocoasolution/mytutorial/assets/170903760/666c8411-df17-43a9-8601-9e0794750a4e)

## (1) A 버튼 입력으로 시작
*  ``||input.A버튼 누를 때||``를 가져오세요.

* ``||loops.4번 반복 실행||`` 블록을 ``||input.A버튼 누를 때||``안에 넣으세요.

```blocks
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
      
    }
})
```

## (2) "도" 소리 넣기  
* ``||music.재생 (도)음을 1박자 동안 재생[완료될 때까지]||``를 가져와 ``||loops.4번 반복 실행||`` 블록안에 넣습니다.

```blocks
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    }
})
```

## (3) "도" 소리 설정 바꾸기  
* ``||music.재생 (도)음을 1박자 동안 재생[완료될 때까지]||``에서 ``||music.1박자||``를 ``||music.1/2박자||``로 바꾸세요. 
* ``||music.완료될 때까지||``를 ``||music.배경에서 실행||``으로 바꾸세요.

```blocks
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        music.play(music.tonePlayable(262, music.beat(BeatFraction.Half)), music.PlaybackMode.InBackground)
    }
})
```

## (4) 큰 하트 넣기
* 이어서 ``||basic.아이콘 출력||``를 넣고 **큰 하트 모양**으로 선택하세요.

```blocks
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
        basic.showIcon(IconNames.Heart)
    }
})
```

## (5) "파" 소리 넣기  
* 이어서 ``||music.재생 (파)음을 1박자 동안 재생[완료될 때까지]||``를 가져와 넣습니다.

* ``||music.1박자||``를 ``||music.1/2박자||``로, ``||music.완료될 때까지||``를 ``||music.배경에서 실행||``으로 바꾸세요.

```blocks
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
        basic.showIcon(IconNames.Heart)
        music.play(music.tonePlayable(349, music.beat(BeatFraction.Half)), music.PlaybackMode.InBackground)
    }
})
```

## (6) 작은 하트 넣기
* 이어서 ``||basic.아이콘 출력||``를 넣고 **작은 하트 모양**으로 선택하세요.

```blocks
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
        basic.showIcon(IconNames.Heart)
        music.play(music.tonePlayable(349, music.beat(BeatFraction.Half)), music.PlaybackMode.InBackground)
        basic.showIcon(IconNames.SmallHeart)
    }
})
```

## (7) 실행해보기
* 지금까지 만든 코드를 ``|다운로드|`` 합니다.
  
* ``||input.A버튼||``을 손으로 눌렀을 때, LED 하트와 소리가 4번 반복해서 나오는지 관찰해 보세요.

```blocks
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
        basic.showIcon(IconNames.Heart)
        music.play(music.tonePlayable(349, music.beat(BeatFraction.Half)), music.PlaybackMode.InBackground)
        basic.showIcon(IconNames.SmallHeart)
    }
})
```

## 끝
* 마지막 페이지 입니다.
