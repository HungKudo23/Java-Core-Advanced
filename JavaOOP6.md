# **Chương OOP (Summary)**
## **Bài 6: Polymorphism (Tính đa hình)**
- Có thể hiểu rằng tính đa hình là cũng có thể sử dụng các class được kế thừa, chức năng thực hiện có thể giống nhưng cách thực hiện sẽ khác nhau.
- Đoạn code ví dụ:
```java
class Animal { // Class sẽ được kế thừa
  public void animalSound() {
    System.out.println("The animal makes a sound");
  }
}

class Pig extends Animal { // Class sẽ kế thừa
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}

class Dog extends Animal { // Class sẽ kế thừa
  public void animalSound() {
    System.out.println("The dog says: bow wow");
  }
}

class Main {
  public static void main(String[] args) {
    Animal myAnimal = new Animal();
    Animal myPig = new Pig();  
    Animal myDog = new Dog();  
    myAnimal.animalSound();
    myPig.animalSound();
    myDog.animalSound();
  }
}
```
- Giải thích sơ qua: Có thể thấy class `Dog` và `Pig` đã kế thừa class `Animal`, và mỗi class đã kế thừa đó sẽ thực hiện riêng "công việc" của riêng chúng, nhưng rõ ràng có ràng buộc với nhau ở phương thức `animalSound()`.