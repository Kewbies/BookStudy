" 객체의 **역할**, **책임**, **협력**에 집중하라. **객체 지향은** 클래스를 지향하는 것이 아닌, **객체를 지향한다.** "



## 역할, 책임, 협력

### 역할(Role)

- 협력(Collaboration)에 참여하는 **특정한 객체의 책임(Responsibility)이나 임무를 의미**한다.
  - 역할 != 책임, 역할 ⊃ 책임
    - 책임 : 범죄자를 검거할 책임
    - 역할 : 책임(범죄자를 검거할)을 갖는 경찰관
- 여러 객체는 동일한 역할을 수행할 수 있다. 
  - 역할을 수행하는 주체는 대체될 수(suitable) 있다.
- 하나의 객체가 여러 역할을 수행할 수 있다.

### 책임(Responsibility)

- 책임을 수행하는 방법은 자율적으로 선택할 수 있다.

### 협력(Collaboration)

- 협력은 **요청(Request)**와 **응답(Response)**으로 구성된다.
- 요청(Request)은 연쇄적으로 발생한다.
  - 요청(Request)에 대한 응답(Response) 역시 역방향으로 연쇄적으로 전달된다.

## 협력 속에 사는 객체

### 객체(Object)

- 객체는 충분히 **협력적**이어야한다. 그렇지 않다면, 복잡도를 증대시킨다.

  - 단, 객체는 요청에 응답할 뿐이다.
- 객체는 **자율적**이어야한다.
    - 요청에 대한 응답의 방식, 응답 여부 또한 객체가 결정한
- 상태(State)와 행동(Behavior)를 지닌다.
    - 협력에 참여하기 위하여 행동을 해야한다.
    - 행동을 하는 데 필요한 상태도 지니고 있는다.

### 메시지(Message)

- 객체간의 유일한 의사소통 수단

```swift
someObject.doSomething()

// someObject is Reciever
// doSomething is Message
// `someObject` recieve `doSomething()` message
```

### 메서드(Method)

- 객체가 수신된 **메시지를 처리하는 방법**
  - Message != Method
- Message와 Method의 분리는 자율성을 증진시킨다.
  - a.k.a 캡슐화(Encapsulation)

