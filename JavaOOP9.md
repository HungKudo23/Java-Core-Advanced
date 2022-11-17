# **Chương OOP (Summary)**
## **Bài 9: Enumeration (Liệt kê cụ thể)**
- Từ khóa **`enum`** dùng để khai báo một class chỉ chứa duy nhất các biến dạng hằng (giống **`final`**)
- Cách khai báo:
```java
enum (tên enum) {
  // giá trị 1,
  // giá trị 2,
  // ...
}
```
VD:
```java
enum Level {
  LOW,
  MEDIUM,
  HIGH
}
```
( Giá trị nằm trong enum nên viết hoa toàn bộ các chữ để dễ nhận dạng. )
- Có thể dùng trong `switch...case` để kiểm tra giá trị tương ứng:
```java
enum Level {
  LOW,
  MEDIUM,
  HIGH
}

public class Main {
  public static void main(String[] args) {
    Level myVar = Level.MEDIUM;

    switch(myVar) {
      case LOW:
        System.out.println("Low level");
        break;
      case MEDIUM:
         System.out.println("Medium level");
        break;
      case HIGH:
        System.out.println("High level");
        break;
    }
  }
}
```
- `enum` cũng có thuộc tính và phương thức giống `class`, chỉ khác là:
    + `enum` chỉ có 3 dạng truy cập là:
        + `public`
        + `static`
        + `final`
    + `enum` không thể được sử dụng để tạo object, không thể kế thừa class khác, nhưng mà vẫn có thể triển khai `interface` 