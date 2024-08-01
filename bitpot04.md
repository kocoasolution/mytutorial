# 코코아팹 비트팟 코딩활동 04

```package
datalogger
```

```ghost
input.onButtonPressed(Button.A, function () {
    측정횟수 = 5
    남은횟수 = 측정횟수
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    datalogger.includeTimestamp(FlashLogTimeStampFormat.Seconds)
    for (let index = 0; index < 측정횟수; index++) {
        토양센서값 = pins.analogReadPin(AnalogPin.P0)
        datalogger.log(datalogger.createCV("soil", 토양센서값))
        basic.showNumber(남은횟수)
        남은횟수 += -1
    }
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.InBackground)
    basic.showIcon(IconNames.Yes)
})
input.onButtonPressed(Button.B, function () {
    music.play(music.tonePlayable(330, music.beat(BeatFraction.Whole)), music.PlaybackMode.InBackground)
    basic.showIcon(IconNames.No)
    datalogger.deleteLog(datalogger.DeleteType.Full)
    basic.clearScreen()
})
let 토양센서값 = 0
let 남은횟수 = 0
let 측정횟수 = 0
music.setVolume(50)


```

```template
input.onButtonPressed(Button.A, function () {
	
})
input.onButtonPressed(Button.B, function () {
    music.play(music.tonePlayable(330, music.beat(BeatFraction.Whole)), music.PlaybackMode.InBackground)
    basic.showIcon(IconNames.No)
    datalogger.deleteLog(datalogger.DeleteType.Full)
    basic.clearScreen()
})
let 남은횟수 = 0
let 측정횟수 = 0
music.setVolume(50)
측정횟수 = 0
남은횟수 = 0
let 토양센서값 = 0

```

## 이번 주제
* 이번에는 **토양수분센서** 데이터를 데이터 로그에 저장해 봅시다.

* 데이터 로그에 저장된 값들을 **표와 그래프**로 확인해 봅시다.

## 1.센서 측정 횟수는 총 5회로 하기 
* ``||input.A 버튼 누를 때||``안에 ``||variables.측정횟수에 (5) 저장||``을 넣습니다.

* 이어서 ``||variables.남은횟수에 (5) 저장||``을 넣습니다.

```blocks
input.onButtonPressed(Button.A, function () {
    측정횟수 = 5
    남은횟수 = 5
})
```

## 2.버튼이 눌렸는지 소리내기
* 이어서 ``||music.재생 (도)음을 (1박자) 동안 재생 [완료될 때까지]||``를 넣습니다.

* 표에 기록될 데이터의 첫 번째 열에 **"초"**가 기록되도록 ``||datalogger.타임스탬프 설정 (초)||``를 넣습니다.
```blocks
input.onButtonPressed(Button.A, function () {
    측정횟수 = 5
    남은횟수 = 5
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    datalogger.includeTimestamp(FlashLogTimeStampFormat.Seconds)
})
```

## 3.토양센서값 반복 측정 시작하기
* 이어서 ``||loops.(4) 번 반복||``을 가져와 ``||loops.(4)||``에 변수 ``||variables.측정횟수||``를 넣습니다.

* 이어서 변수 ``||variables.토양센서값||``에 ``||pins.(P0)의 아날로그 입력 값||``을 저장해 줍니다.

```blocks
input.onButtonPressed(Button.A, function () {
    측정횟수 = 5
    남은횟수 = 5
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    datalogger.includeTimestamp(FlashLogTimeStampFormat.Seconds)
    for (let index = 0; index < 측정횟수; index++) {
        토양센서값 = pins.analogReadPin(AnalogPin.P0)
    }
})
```

## 4.토양센서값 데이터 로깅
* 이어서 ``||datalogger.데이터 로깅 열(" ") 값(0)||``을 가져옵니다.

* ``||datalogger.열(" ")||``에 **soil** 을 입력하고, ``||datalogger.값(0)||``에 변수``||variables.토양센서값||``을 넣습니다.

```blocks
input.onButtonPressed(Button.A, function () {
    측정횟수 = 5
    남은횟수 = 5
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    datalogger.includeTimestamp(FlashLogTimeStampFormat.Seconds)
    for (let index = 0; index < 측정횟수; index++) {
        토양센서값 = pins.analogReadPin(AnalogPin.P0)
        datalogger.log(datalogger.createCV("soil", 토양센서값))
    }
})
```

## 5.남은 측정횟수 LED로 표시
* 남은 측정횟수를 LED로 표시하기 위해 ``||basic.숫자 출력()||``안에 ``||variables.남은횟수||``를 넣어 코딩해줍니다.

* 이어서 ``||variables.남은횟수 값 (-1) 증가||``를 넣어서 횟수가 1씩 줄어들게 해줍니다.

```blocks
input.onButtonPressed(Button.A, function () {
    측정횟수 = 5
    남은횟수 = 5
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    datalogger.includeTimestamp(FlashLogTimeStampFormat.Seconds)
    for (let index = 0; index < 측정횟수; index++) {
        토양센서값 = pins.analogReadPin(AnalogPin.P0)
        datalogger.log(datalogger.createCV("soil", 토양센서값))
        basic.showNumber(남은횟수)
        남은횟수 += -1
    }
})
```

## 6.측정의 끝을 알리기
* 센서 측정이 끝났음을 소리로 알리기 위해 ``||music.재생(도)음을 (1박자)동안 재생 [배경에서 실행]||``을 넣어줍니다.

* 이어서 ``||basic.아이콘 출력||``을 가져와 LED에 **V 표시**가 나타나게 해주세요.

```blocks
input.onButtonPressed(Button.A, function () {
    측정횟수 = 5
    남은횟수 = 5
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    datalogger.includeTimestamp(FlashLogTimeStampFormat.Seconds)
    for (let index = 0; index < 측정횟수; index++) {
        토양센서값 = pins.analogReadPin(AnalogPin.P0)
        datalogger.log(datalogger.createCV("soil", 토양센서값))
        basic.showNumber(남은횟수)
        남은횟수 += -1
    }
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.InBackground)
    basic.showIcon(IconNames.Yes)
})
```

## 8.코드 다운로드 하기
* 모든 코드를 완성했으니, ``|다운로드|``를 눌러 코드를 마이크로비트로 다운받으세요.

* **버튼 B**를 눌러 이전의 데이터를 지워주고, 토양수분센서를 물이나 화분에 꽂은 뒤 **버튼 A**를 눌러 센서값을 데이터로 기록하세요.

## 9.센서 데이터 확인하기
![그림1](https://github.com/user-attachments/assets/0f611afc-2ede-4502-99af-231fd5a90f32)

## 끝
* 마지막 페이지 입니다.
