# 코코아팹 비트팟 코딩활동 01

```ghost
let 토양수분센서값 = 0
basic.forever(function () {
    토양수분센서값 = pins.analogReadPin(AnalogPin.P0)
    basic.showString("" + (토양수분센서값))
    if (토양수분센서값 < 700) {
        basic.showIcon(IconNames.Happy)
    } else if (토양수분센서값 < 800) {
        basic.showIcon(IconNames.Asleep)
    } else {
        basic.showIcon(IconNames.Sad)
    }
})

```
## 토양의 수분 상태를 LED 아이콘 표정으로 나타내 봅시다. 
![4](https://github.com/kocoasolution/mytutorial/assets/170903760/76cd0868-1db3-4ca4-9773-853f9ae99076)

## 전체 알고리즘
* 1.토양의 수분상태를 ``||토양수분센서||`` 변수에 저장합니다.

* 2.``||토양수분센서||``값의 크기에 따라 ``||basic.아이콘 출력||``으로 표정을 나타냅니다.

## (1-1) 변수 만들기 
* ``||토양수분센서||`` 변수를 만드세요.

* ``||토양수분센서에 0 저장||``블록을 ``||basic.무한반복||``안에 넣으세요.

```blocks
let 토양수분센서 = 0
basic.forever(function () {
    토양수분센서 = 0
})
```

## (1-2) 변수에 센서값 저장하기 
* 토양의 수분 측정은 ``||pins.P0의 아날로그 입력 값||``블록으로 합니다.

* 그래서 ``||pins.P0의 아날로그 입력 값||``블록을 ``||토양수분센서에 0 저장||`` 블록에 넣으세요.

```blocks
let 토양수분센서 = 0
basic.forever(function () {
    토양수분센서 = pins.analogReadPin(AnalogPin.P0)
})
```

## (1-3) 변수를 LED로 출력하기 
* ``||basic.문자열 출력("Hello!")||``블록을 **``||basic.무한반복||``**에 넣으세요.

* ``||토양수분센서||`` 변수를 ``||basic.문자열 출력("Hello!")||``블록에 끼워 넣으세요.

```blocks
let 토양수분센서 = 0
basic.forever(function () {
    토양수분센서 = pins.analogReadPin(AnalogPin.P0)
    basic.showString("" + (토양수분센서))
})
```

## (1-4) 센서 테스트를 위한 코드 다운로드 
* 지금까지 코딩한 것을 ``|다운로드|`` 하세요.

## (1-5) 아래 그림처럼 센서를 물컵에 담궈서 센서값 확인해보기
![bitpot02](https://github.com/kocoasolution/mytutorial/assets/170903760/9b06a8be-5f08-409b-8d94-3dda5c7f1622)

## (1-6) 센서의 기준값을 정해 봅시다.
* **센서**가 **물 밖**에 있을 때와 **물 안**에 담궜을 때 각각 센서값이 얼마인가요?

* 위 두 경우의 값의 **가운데 값**을 계산하고 기록해 둡니다.

~hint(가운데 값 구하기 예시)
* 물 밖 센서값 = 1000,  물 안 센서값 = 400
* 가운데 값 = (1000 + 400) / 2 = 700
hint~

## (2-1) 계속 이어서, 만약~아니면 블록 가져오기
* 도구상자 **[논리]** 에서 ``|만약 <참>이면, 아니면|``을 가져와 **``||basic.무한반복||``**안에 넣으세요.

```blocks
let 토양수분센서 = 0
basic.forever(function () {
    토양수분센서 = pins.analogReadPin(AnalogPin.P0)
    basic.showString("" + (토양수분센서))
    if (true) {
    	
    } else {
    	
    }
})
```

## (2-2) (+)클릭해서 비교 횟수 추가하기
![bitpot03](https://github.com/kocoasolution/mytutorial/assets/170903760/af331e5f-b9cc-4ca3-9856-42316384f822)

```blocks
let 토양수분센서 = 0
basic.forever(function () {
    토양수분센서 = pins.analogReadPin(AnalogPin.P0)
    basic.showString("" + (토양수분센서))
    if (true) {
    
    } else if (false) {
    	
    } else {
    	
    }
})
```

## (2-3) 물이 충분하면 웃는 얼굴
* 여기에서는 **가운데 값 = 700** 으로 가정합니다.(여러분들만의 가운데 값을 사용하세요)

* 변수 ``||토양수분센서||``가 **700 보다 작으면** ``||basic.아이콘 출력(웃는얼굴)||`` 실행하기

```blocks
let 토양수분센서 = 0
basic.forever(function () {
    토양수분센서 = pins.analogReadPin(AnalogPin.P0)
    basic.showString("" + (토양수분센서))
    if (토양수분센서 < 700) {
        basic.showIcon(IconNames.Happy)
    } else if (false) {
    	
    } else {
    	
    }
})
```

## (2-4) 물이 중간 정도면 무표정 얼굴
* 변수 ``||토양수분센서||`` **700 이상 800 보다 작으면** ``||basic.아이콘 출력(무표정)||`` 실행하기

* 가운데 값 + 100 을 기준값으로 무표정 얼굴이 나오게 합니다.
```blocks
let 토양수분센서 = 0
basic.forever(function () {
    토양수분센서 = pins.analogReadPin(AnalogPin.P0)
    basic.showString("" + (토양수분센서))
    if (토양수분센서 < 700) {
        basic.showIcon(IconNames.Happy)
    } else if (토양수분센서 < 800) {
        basic.showIcon(IconNames.Asleep)
    } else {
    	
    }
})
```

## (2-5) 물이 모자라면 우는표정 얼굴
* 변수 ``||토양수분센서||`` **800 이상 이면** ``||basic.아이콘 출력(우는표정)||`` 실행하기

```blocks
let 토양수분센서 = 0
basic.forever(function () {
    토양수분센서 = pins.analogReadPin(AnalogPin.P0)
    basic.showString("" + (토양수분센서))
    if (토양수분센서 < 700) {
        basic.showIcon(IconNames.Happy)
    } else if (토양수분센서 < 800) {
        basic.showIcon(IconNames.Asleep)
    } else {
        basic.showIcon(IconNames.Sad)
    }
})
```

## (2-6) 최종 코드 다운로드 
* 지금까지 코딩한 것을 ``|다운로드|`` 하세요.

* 센서를 **화분**이나 **물 컵**에 넣어서 마이크로비트 ***LED의 표정변화**를 관찰해 보세요.

## 끝
* 마지막 페이지 입니다.
