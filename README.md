# 묵찌빠 프로젝트✊🏻✌🏻🖐🏻


# 묵찌빠 게임 Ground Rule

1. 코드컨벤션 
- 코드블록 끝날 때 한칸 띄우기
2. 활동학습 있는날에는 2시, 활동학습 없는날 9시반부터 시작
3. 커밋은 함수 단위로
4. 스크럼 9시반에 시작
- Todo List 작성


## STEP 1 소개
> 사용자가 가위, 바위, 보 중 하나를 고르면 랜덤하게 뽑은 컴퓨터의 패와 비교하여 승패를 정합니다.


STEP 1 요구사항
 - 최초 실행시 가위(1), 바위(2), 보(3)! <종료 : 0> 을 출력합니다.
 - 사용자에게 0, 1, 2, 3 중 한가지를 입력받아 결과를 출력합니다.
   - 0을 입력받은 경우 게임을 종료합니다.
   - 0~3이 아닌 값을 입력받은 경우 "잘못된 입력입니다. 다시 시도해주세요." 출력후 최초실행상태로 복귀합니다.
 - 랜덤하게 뽑은 컴퓨터의 패와 비교하여 승패를 정합니다.
   

## STEP 2 소개
> 가위, 바위, 보 게임에서 승패가 갈린 경우 묵찌빠 게임을 이어서 진행합니다. 사용자가 가위, 바위, 보 중 하나를 고르면 임의의 컴퓨터의 패와 비교하여 턴과 승패를 정합니다.

STEP 2 요구사항
- 최초 실행시 [*** 턴] 묵(1), 찌(2), 빠(3)! <종료 : 0> : 을 출력합니다.
- 가위, 바위, 보 게임에서 이겼거나 지난 턴에서 이긴 사람이 턴을 쥡니다.
- 만약 사용자가 잘못된 입력을 한 경우 컴퓨터에게 턴을 넘깁니다.
- 결과 출력시 아래와 같이 게임이 진행됩니다.
   - 사용자와 컴퓨터의 패가 같은 경우 : 턴을 쥐고 있는 쪽이 승리합니다.
     - “***의 승리!” 출력 후 게임을 종료합니다.
   - 사용자와 컴퓨터의 패가 다른 경우 : 이긴 쪽이 턴을 쥡니다.
     - “***의 턴입니다” 출력 후 묵, 찌, 빠 계속 실행합니다.
   - 0을 입력받은 경우 : 게임을 종료합니다.

---

## 팀원을 소개합니다 👀


|                                                                    리지                                                                    |                                                                           릴라                                                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------:|
| <img width="200" alt="image" src="https://user-images.githubusercontent.com/114971172/209290192-27c1d18e-fd9a-4d47-97cd-2151e29dcea7.png"> | <img width="200" alt="image" src=https://cdn.discordapp.com/attachments/1054218081787973662/1058207490296262665/KakaoTalk_Image_2022-12-23-11-04-10.png> |  

----

## 타임라인 🔍


| STEP  | 날짜             | 타임라인                                                                                                                                                                     |
| --------- | ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|STEP1| **2022.12.26** | - 게임메뉴출력 함수 생성 </br>- 게임시작 함수 생성 </br> - 입력값과 컴퓨터의 값 비교하는 함수 생성                                                                           |
|    STEP1   | **2022.12.27** | - 게임시작 함수 분리 </br>- 비교하는 함수 분리 (임의의 패 구현하는 함수, 오류처리 함수)</br>- 게임결과출력 함수 생성</br>- 게임종료로직 수정</br>- 전체적인 코드 컨벤션 수정 |
| STEP2 | **2022.12.28** | - 게임메뉴출력 및 턴확인 함수 생성</br>- 비교하는 함수 생성</br>- 오류처리하는 함수 생성</br>- 재활용되는 함수 프로토콜적용, class적용                                       |
|   STEP2    |**2022.12.29** | - 파일분리</br>- 재활용되는 함수 프로토콜 extension 적용                                                                                                                                                                            |
| STEP2  | **2022.12.30** | - 게임요구사항 중 턴확인하여 출력하는 함수 구현</br>- 파일 분리, 그룹나누기</br>- 전체적인 코드 컨벤션 수정                                                                                                                  |

-----

## 순서도 🔍⏩

__STEP 1__
![](https://i.imgur.com/bbuJz5m.png)

__STEP 2__
![](https://i.imgur.com/pTG5qtS.png)


---

## 구현할 함수

- STEP1 구현할 함수

>1. 실행함수 (startGame)
>2. 게임안내문 출력함수 (printGameMenu)
>3. 사용자 입력 받는 함수 (getUserInput)
>4. 입력받은 값 검증하는 함수 (checkAvailability)
>5. 오류처리하는 함수 (handleGameError)
>6. 컴퓨터 임의의 패 구현하는 함수 (makeRandomHandMotion)
>7. 컴퓨터와 내 패를 비교하는 함수 (compare)
>8. 게임결과출력하는 함수 (이긴경우, 진경우, 비긴경우) (printResult)

- STEP2 구현할 함수

>1. 이긴경우, 진경우에 묵찌빠 게임을 진행하는 함수
>2. 묵찌빠 게임 함수
>3. 묵찌빠 턴, 메뉴 출력 함수
>4. 턴을 확인하는 함수 (가위바위보 게임에서 이긴사람이 첫번째 턴)
>5. 턴을 넘겨주는 함수 (잘못된 입력을 한 경우 턴이 이동됨)
>6. 사용자 입력받는 함수 (묵찌빠 게임 입력)
>7. 게임 결과를 확인하는 함수 (동일한경우, 다른경우)
>8. 승리를 출력하는 함수 (이긴경우: 게임종료, 진경우: 다시게임 시작)




---
## 게임실행화면 🔍

![게임종료](https://i.imgur.com/EYlsP14.png)
<span style="background-color:#fff5b1;">게임종료</span>

---
![](https://i.imgur.com/lVuWbvA.png)
<span style="background-color:#fff5b1;">최초실행화면</span>

---
![](https://i.imgur.com/L4LddjH.png)
<span style="background-color:#fff5b1;">묵찌빠 게임결과</span>

---
![](https://i.imgur.com/pcuVEMk.png)
<span style="background-color:#fff5b1;">잘못된 입력으로 턴전환</span>







## 트러블슈팅 
### STEP1
**함수분리** 
- ```하나의 함수는 한가지 기능만 한다``` 이 관점으로 코드를 작성하도록 했습니다. 그래서 미션을 시작하기 전 요구사항을 천천히 읽어보면서 어떤 함수를 만드는게 좋을지 서로 의논하여 정리를 해보았습니다. 

**프로그램의 종료 시점**

 - 코드 작성시 오류를 던지고 처리하는 구문을 Result 구문으로 받았습니다. 
 Result 구문은 success 와 failure 두가지를 나눠서 처리를 하기 때문에 1,2,3을 받았을때는 success, 그 외의 값을 받으면 failure 로 받도록 처리했습니다.
 그런데 0 을 입력하면 게임 종료라는 새로운 변수가 생겼고 이를 받아 처리하는 부분이 고민되었습니다. 왜냐하면 0은 또 다른 옵션값이지 failure가 아니였기 때문입니다. 
 그래서 게임메뉴의 열거형 타입에 0이라는 새로운 case 를 넣어주고 success에서 조건문을 넣어 게임종료를 처리하도록 구현했습니다.
 ```swift
case .failure(_):
         print("잘못된 입력입니다. 다시 시도해주세요")
         startGame()
         return nil
     case .success(let handMotion):
         if handMotion == .endGame {
             print("게임종료")
             return nil
         }
         return handMotion
     }
```

**매직 넘버**
- 기존의 입력값을 사용자에게 0, 1, 2, 3 숫자로 입력을 받고 있었다. 그래서 숫자를 통해 값을 비교하는 표현을 사용했습니다.

```swift=
  if (computerInput == 1 && userInput == 2) ||
       (computerInput == 2 && userInput == 3) ||
       computerInput == 3 && userInput == 1 {
        print("이겼습니다!")
    }
```
그러나 코드를 작성하지 않은 사람이 이 코드만을 보았을때는 1, 2, 3이 무엇을 의미하는지 알아볼 수 없는 매직넘버라는 피드백을 받았습니다.
그래서 이부분을 새롭게 1, 2, 3 이 어떤 의미를 가지는지 Enum 타입을 사용해 명시적으로 보여주었습니다.
```swift=
    enum GameMenu: String {
    case scissor = "1"
    case rock = "2"
    case paper = "3"
    case endGame = "0"       
    }

```

**switch 구문활용**
- if 문을 연속적으로 사용하여 게임결과를 확인하도록 구현을 했었는데 코드의 길이가 길어지고 가독성이 떨어진다는 피드백을 받았습니다.
그래서 조금 더 간결하고 가독성이 좋은 switch 구문을 활용하여 아래와 같이 코드를 변경했습니다. 또한 비교하고자 하는 유저와 컴퓨터의 값을 튜플타입으로 받아서 코드의 가독성을 올리고자 했습니다.

```swift=
  switch (user, computer) {
        case (.scissor, .paper), (.rock, .scissor), (.paper, .rock) :
            mukjjibba.isUserWin = true
            return .win
        case (.scissor, .rock), (.rock, .paper), (.paper, .scissor) :
            mukjjibba.isUserWin = false
            return .lose
        default :
            return .draw
        }
```

### STEP2

**함수의 재사용**
- STEP1의 로직과 STEP2의 로직의 상당부분이 유사해서 코드를 추가적으로 작성하지 않고 다시 쓸 수 있는 방법이 없을까 많이 고민 해보았습니다. 그래서 내부 로직에서 가위바위보 모드인지 묵찌빠 모드인지 조건에 따라 처리를 한다면 하나의 함수로 두가지 경우를 다 쓸 수 있지 않을까 생각했습니다. 하지만 질리와 아얀의 피드백에서는 긍정적인 답변이 아니었습니다. 로직 내에서 분기에 따라서 다른 기능을 한다면 그것은 재활용이 아니라 다른 기능을 하는 함수라는 것이었습니다.

**추상화의 활용**
- 함수의 재사용을 고민하면서 로직이 유사한 함수와 아예 똑같은 함수를 구분해 보았습니다. 로직이 비슷하지만 세부적인 코드가 다른 함수들은 추상화 개념을 적용하여 protocol을 만들어 각 클래스에서 상속을 받게 했습니다. GameProtocol를 상속받은 RockScissorPaper 클래스와 Mukjjibba 클래스내에서 자신의 단계에서 맞는 로직을 구현했습니다.

**Extension**
- 아예 똑같은 함수들은 처음엔 공통요소라는 클래스를 만들어 각 게임이 상속받도록 함수를 구현했습니다. Protocol은 함수 body를 갖고있지 않기 때문에 클래스로 만들어주었는데, Extension을 사용하여 그 문제를 해결했습니다. Extension을 구현하니 공통된 요소를 따로 클래스로 만들어 상속받을 일이 불필요해졌고 더 깔끔한 코드가 되었습니다. 


```swift
protocol GameProtocol {
    func printGameMenu()
    func handleGameError(userInput: Result<GameMenu, GameError>) -> GameMenu?
    func compare(_ userInput: GameMenu?, with computerInput: GameMenu?) -> GameResult?
    func printResult(gameResult: GameResult)
    func startGame()
}

extension GameProtocol {
    func getUserInput() -> String? {
        let input: String? = readLine()
        return input
    }
    
    func checkAvailability(input: String?) -> Result<GameMenu, GameError> {
        guard let userInput: String = input,
              let userHandMotion: GameMenu = GameMenu(rawValue: userInput)
        else { return .failure(.invalidInput) }
        return .success(userHandMotion)
    }
    
    func makeRandomHandMotion() -> GameMenu? {
        guard let computerRandomNumber: String = ["1", "2", "3"].randomElement() else { return nil }
        let computerHandMotion: GameMenu? = GameMenu(rawValue: computerRandomNumber)
        return computerHandMotion
    }
}

```


## Reference📚

- [Protocol 공식문서](https://docs.swift.org/swift-book/LanguageGuide/Protocols.html)
- [Enumerations 공식문서](https://docs.swift.org/swift-book/LanguageGuide/Enumerations.html)
- [Control Flow 공식문서](https://docs.swift.org/swift-book/LanguageGuide/ControlFlow.html)



## 팀 회고 🤝🏻


**우리팀이 잘한 점**
- 단순히 돌아가는 코드가 아닌 원인과 결과가 있는 코드를 지향했습니다.
- '프로젝트 수행 중 핵심 경험' 을 확인하면서 같이 부족한 부분을 공부했습니다.
- 학습 내용 뿐만이 아니라 관련이 있는 사항까지 심층있게 공부했습니다.

**우리팀 개선할 점**
- 사전에 코드 컨벤션을 정했으나 간혹 한 두개씩 놓치는 부분이 있었습니다.
- 프로젝트의 요구 명세서를 정확히 숙지하지 않아 놓치는 부분이 있었습니다.
- 스크럼을 정했는데 정확히 지키지는 못했습니다. 

**팀원 서로 칭찬하기** 
- 리지 To 릴라
: 코드를 작성하면서 이해가 안되는 부분을 자세히 설명해주었습니다. 또한 릴라가 직접 질문 내용에 대한 공부를 해서 설명해주고 필요한 자료들을 공유해주었습니다. 그리고 질문방에 질문을 주저할때 릴라가 옆에서 힘을 넣어주었어요 그래서 자신있게 질문할 수 있었습니다! 마지막으로 늘 밝고 유쾌하여 일주일동안 재밌게 미션을 수행할 수 있었습니다!! ☺️



- 릴라 To 리지
: 리지는 코드의 완벽한 이해라는 목표를 가지고 프로젝트를 진행해, 간혹 저도 놓치고 있었던 부분을 같이 돌아볼 수 있었습니다.
저는 평소에 큰 흐름적인 이해만을 염두에 두고 공부를 했었기에 깊이가 다소 부족하다고 생각했습니다. 하지만 이번 한주 리지와 함께 프로젝트를 진행하면서 
저의 지식을 좀더 깊게 만들 수 있는 방법을 얻어간 것 같습니다 🥺
