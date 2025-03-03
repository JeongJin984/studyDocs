## OOP

### Why OOP?

코드를 볼 때 중요하게 생각해야하는 것들이 몇가지 있다. Reusablity, Scalablity다. 순전히 내 생각이지만 이 2가지를 지키기 위해 나온 여러 프로그래밍 기법 중 가장 효율적이라고 생각되어 나온 것이 OOP(객체지향 프로그래밍)이라고 생각한다.

사실 OOP는 단일 개념으로 알고있는 것 보다 design pattern과 엮어서 알고 있는 것이 더 효율적이라고 생각된다.

### 4 Principles

> **Encapsulation(캡슐화)**

Restricting Direct Access to data and controll access via methods. 즉 데이터를 숨기고 접근에 대해 메서드를 통해 컨트롤하라는 뜻이다. 

경험상 보통 레거시 코드에서 무분별한 getter, setter를 통해서 이 원칙이 파괴된 모습을 보곤하는데 사실 에러가 발생하는 부분은 도메인으로 바껴야 하는 데이터를 전체적으로 수정하는 것이아닌 서비스에 적힌 메서드를 직접 수정해야하기 때문에 로직 수정에 누락이 발생할 수 있다는 부분이다.

> **Abstraction(추상화)**

hiding complex implementation details and exposing only necessary functionalities. 즉 복잡한 부분은 숨기고 필요한 부분만 보이라는 것이다.

사실 이 부분은 적당한 타협이 필요하다고 생각한다. 간단하게 하나의 Vendor로 구현되는 비교적 로직이 간단한 서비스의 경우 추상화를 진행하기에는 효율적이지 않다고 생각한다. 하지만 하나의 서비스가 여러 개의 Vendor Module로서 구현되거나 하는 경우 필요한 부분은 Abstract 클래스나 Interface로 묶어서 구현하는 것이 맞다고 생각한다.

> **Inheritance(상속성, 재사용)**

inherit properties and behavior from another class. 즉 기존의 기능을 재사용하거나 새로운 기능을 추가(확장)할 수있게 한다는 것이다.

코드가 중복으로 생성되는 것을 막는다. 수정에 있어 중복적인 작업을 하지 않게 해준다.

> **Polymorphism(Polymorphism)**

one method or function to take different forms. 기존의 기능을 상속을 통해 수정하는 것이다. 이는 같은 함수가 타입에 따라서 다르게 동작하도록 할 수 있다.