" **행동이 상태를 결정**한다. "

" **객체 지향은 현실의 모방이 아닌, 은유이다.** "



## 객체, 그리고 소프트웨어 나라

### 상태(State)

- 상태를 확인함으로써, 과거의 모든 이력을 확인할 필요가 없어졌다.

- 상태는 정적인 프로퍼티(Property)와 동적인 프로퍼티 값(Property Value)으로 구성되어있다.

- #### 프로퍼티(Property)

  - 프로퍼티란 **상태를 구성하는 모든 특징** 이다.

  - 프로퍼티는 링크(Link)와 속성(Attribute)로 표현할 수 있다.

    - ##### 링크(Link)

      - 객체와 객체 사이의 의미있는 연결
      - "객체가 다른 객체를 알고 있다."를 의미한다.

    - ##### 속성(Attribute)

      - 객체를 구성하는 단순한 값이다.

### 행동(Behavior)

- **행동은 상태를 변화**시킨다.
  - Side Effect를 발생시킬 수 있다.
- **행동의 결과는 상태에 의존적**이다.
- 외부의 **요청(Request) 또는 수신된 메시지(Recieved Message)**에 **응답(Response)**하기 위해 **동작하고 반응**하는 활동이다.

### 캡슐화(Encapsulation)

- **상태를 외부에 노출시키지 않**고, **행동을 경계로 캡슐화**한다.
  -  외부에서 객체의 상태를 변경할 수 없다.
  - 메시지를 전달 받은 객체가 행동을 함으로써, 상태를 변경한다.
  - 메시지에 대한 처리는 수신자(Reciever)의 자율적인 판단에 따른다.
  - 캡슐화를 통하여 자율성을 높인다.

```swift
struct Ellice {
  
	func drink(beverage: Beverage) {
    
    self.height -= 10
   	beverage.drunken(quantity)
  }
}
```

## 식별자

### 값(Value)

- Immutable State
- 동등성(Equality) : 값이 같은지 판단하는 성질 
- ﹦Value Object

### 객체

- Mutable State
- 동일성(Identical) : 식별자를 기반으로 객체가 같은 지 판단하는 성질
- ﹦Reference Object, Entity

## 기계로서의 객체

- 쿼리(Query) : 객체의 상태를 조회하는 작업
- 명령(Command) : 객체의 상태를 변경하는 작업                                                                                                                                                                                                                                                                        
- e.g. 사용자는 버튼을 누른다. (메시지의 전송)
  - 기계는 어떤 방식으로 동작할지 결정한다. (수신된 메시지의 처리 방법에 대해 자율적인 객체)

## 행동이 상태를 결정한다

- 상태를 먼저 결정하지 마라.
  - 캡슐화가 저해된다.
  - 객체의 협력성을 떨어트린다.
  - 재사용성이 저하된다.
- **행동**은 객체가 **협력에 참여하기 위한 유일한 방법**이다.
  - 객체가 적합한지를 결정하는 것은 상태가 아닌 행동이다.

## 은유와 객체

- **소프트웨어 객체는** 실제의 객체를 단순화 혹은 추상화하는 것이 아닌 **특성이 전혀 다른 어떠한 것**이다.

### 의인화(Anthropomorphism)

- 소프트웨어 객체는 능동적으로 작동할 수 있다.

### 은유(Metaphor)

- 실제 객체의 의미 일부가 소프트웨어 객체로 전달된다.
  - 따라서, **소프트웨어 객체는 실제 객체에 대한 은유**이다.



## Additionals

- [Roles, Responsibilities, Collaborations - 조영호](https://www.slideshare.net/baejjae93/roles-responsibilities-collaborations)
- Q. RDD(Responsibility-Driven Design)이란 무엇인가?
- Q. 책임의 분리는 어떻게 하는가? 객체는 여러개의 역할을 가질 수 있다. 좋은 방식인가?

