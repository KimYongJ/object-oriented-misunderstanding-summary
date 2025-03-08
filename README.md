# 목차

- [1장. 협력하는 객체들의 공동체](https://github.com/KimYongJ/object-oriented-misunderstanding-summary/blob/main/summary/1%EC%9E%A5.%20%ED%98%91%EB%A0%A5%ED%95%98%EB%8A%94%20%EA%B0%9D%EC%B2%B4%EB%93%A4%EC%9D%98%20%EA%B3%B5%EB%8F%99%EC%B2%B4.md)

- [2장. 이상한 나라의 객체](https://github.com/KimYongJ/object-oriented-misunderstanding-summary/blob/main/summary/2%EC%9E%A5.%20%EC%9D%B4%EC%83%81%ED%95%9C%20%EB%82%98%EB%9D%BC%EC%9D%98%20%EA%B0%9D%EC%B2%B4.md)

- [3장. 타입과 추상화](https://github.com/KimYongJ/object-oriented-misunderstanding-summary/blob/main/summary/3%EC%9E%A5.%20%ED%83%80%EC%9E%85%EA%B3%BC%20%EC%B6%94%EC%83%81%ED%99%94.md)

- [4장. 역할, 책임, 협력](https://github.com/KimYongJ/object-oriented-misunderstanding-summary/blob/main/summary/4%EC%9E%A5.%20%EC%97%AD%ED%95%A0%2C%20%EC%B1%85%EC%9E%84%2C%20%ED%98%91%EB%A0%A5.md)

- [5장. 책임과 메시지](https://github.com/KimYongJ/object-oriented-misunderstanding-summary/blob/main/summary/5%EC%9E%A5.%20%EC%B1%85%EC%9E%84%EA%B3%BC%20%EB%A9%94%EC%8B%9C%EC%A7%80.md)

- [6장. 객체지도](https://github.com/KimYongJ/object-oriented-misunderstanding-summary/blob/main/summary/6%EC%9E%A5.%20%EA%B0%9D%EC%B2%B4%EC%A7%80%EB%8F%84.md)

- [7장. 총정리](https://github.com/KimYongJ/object-oriented-misunderstanding-summary/blob/main/summary/7%EC%9E%A5.%20%EC%B4%9D%EC%A0%95%EB%A6%AC.md)

---


- 이 책은 객체지향 설계 방법에 대해 깊이 있게 설명하는 책입니다. 1장에서 6장까지는 객체지향 설계의 기초와 핵심 원칙들을 다루고, 7장에서는 실제 객체지향 설계 과정을 예시로 들어 설명합니다. 특히, 커피 전문점 내에서 일어나는 다양한 상황들을 모델로 사용하여 객체지향 설계가 실제로 어떻게 적용되는지 구체적으로 보여줍니다. 아래는 책에서 소개하는 객체지향 설계 순서를 간단히 정리한 것입니다.

<br>

## 객체지향 설계 순서

<br> 

### 1. 도메인(객체) 정하기
- 손님 객체, 메뉴 항목 객체, 메뉴판 객체, 바리스타 객체, 커피 객체

   <br> 
   
### 2. 객체들 간의 관계 정하기
- 메뉴 항목은 메뉴판에 속하고, 메뉴판은 손님과 관계하고, 손님은 바리스타와 관계하고, 바리스타는 커피 객체와 관계한다.

   <br> 
   
### 3. 협력 찾기
- 협력 설계시 객체가 메시지를 선택하는게 아니라 메시지가 객체를 선택해야 한다. 이 말은 메시지를 먼저 정하고, 그 후에 메시지를 수신하기에 적절한 객체를 찾아야 한다는 의미이다. ‘커피를주문하라’ 는 메시지는 손님 객체에게 할당해야 한다. 그러면 손님은 커피 종류를 알아야 하기 때문에 메뉴판 객체와 협력한다. 아래 그림과 같이 완성된다.

   ![image](https://github.com/user-attachments/assets/05e2bb89-365b-4e4c-aa80-694d64a24b9b)


<br> 

### 4. 인터페이스 정리하기
- 위와 같이 협력과 메시지를 정하면, 객체가 수신한 메시지가 객체의 인터페이스를 결정한다. 손님 객체가 ‘커피를 주문하라’는 메시지를 수신하면 손님 객체 안에서 그것을 수행하는 오퍼레이션을 제공해야 한다. 각 메시지 당 그에 따른 오퍼레이션을 정의한다.

   <br> 
   
### 5. 구현하기
- 클래스의 인터페이스 식별 후 이제 오퍼레이션을 수행하는 방법을 메서드로 구현한다. 이 과정에서 인터페이스가 변경될 수 있다. 위의 작업들은 설계 단계이기 때문에 실제 구현시 변경되며, 설계에 시간을 쏟기 보다는 최대한 빨리 코드를 구현해서 설계에 이상이 없는지, 구현 가능한지를 판단하는것이 중요하다.
