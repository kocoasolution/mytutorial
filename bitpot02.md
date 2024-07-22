# 코코아팹 비트팟 코딩활동 02

```ghost

input.onButtonPressed(Button.A, function () {
music.setVolume(50)
music.play(music.tonePlayable(392, music.beat(BeatFraction.Half)), music.PlaybackMode.UntilDone)
})

```

```template
input.onButtonPressed(Button.A, function () {
})
```

## 음악 만들어 소리 내보기 
* 음악 블록을 이용해 **"나비야"** 음악 일부를 만들어 봅시다.


## 1.소리 크기 정하기 
* ``||music.음량을 (127)로 설정||``을 가져와 ``||input.A 버튼 누를 때||``안에 넣으세요.

* ``||music.음량 (127)||``을 ``||music.음량 (60)||`` 으로 바꿔 소리가 작게 나오게 해주세요.

```blocks
input.onButtonPressed(Button.A, function () {
    music.setVolume(60)
})

```


## 2.계이름 넣기(초반부)
* ``||music.재생 (도)음을 (1박자) 동안 재생 [완료될 때까지]||``를 가져와 ``||input.A 버튼 누를 때||``안에 이어서 **6개** 넣습니다.

* 6개 블록의 계이름을 **솔(1박자), 미(1박자), 미(2박자), 파(1박자), 레(1박자), 레(2박자)** 로 바꿉니다.

```blocks
input.onButtonPressed(Button.A, function () {
    music.setVolume(60)
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(330, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(330, music.beat(BeatFraction.Double)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(349, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(294, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(294, music.beat(BeatFraction.Double)), music.PlaybackMode.UntilDone)
})
```

## 3.계이름 넣기(후반부)
* ``||music.재생 (도)음을 (1박자) 동안 재생 [완료될 때까지]||``를 **추가로 6개** 더 가져옵니다.

* 추가 6개 블록의 계이름을 **도(1박자), 레(1박자), 미(1박자), 파(1박자), 솔(1박자), 솔(1박자), 솔(2박자)** 로 바꿉니다.

```blocks
input.onButtonPressed(Button.A, function () {
    music.setVolume(60)
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(330, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(330, music.beat(BeatFraction.Double)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(349, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(294, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(294, music.beat(BeatFraction.Double)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(294, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(330, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(349, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Double)), music.PlaybackMode.UntilDone)
})
```

## 4.최종 코드 다운로드 
* 지금까지 코딩한 것을 ``|다운로드|`` 하세요.

* 마이크로비트의 **A 버튼을 눌렀을 때** **"나비야" 노래**가 나오는 지 확인해 보세요.

## 끝
* 마지막 페이지 입니다.
