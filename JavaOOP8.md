# **Chương OOP (Summary)**
## **Bài 8: Inner Classes (Các class trong class)**
- VD:
```java
class OuterClass {
  int x = 10;

  class InnerClass { // Đây là Inner Class
    int y = 5;
  }
}

public class Main {
  public static void main(String[] args) {
    OuterClass myOuter = new OuterClass();
    OuterClass.InnerClass myInner = myOuter.new InnerClass();
    System.out.println(myInner.y + myOuter.x);
  }
}

// Kết quả: 15 (5 + 10)
```
- Cách sử dụng thuộc tính của Inner class: Mặc định là sẽ chỉ cần nối giữa `class gốc và Inner class` bằng dấu **``.``**
- Inner class chỉ có thể được khai báo ở 3 dạng:
    + `private`
    + `protected`
    + `static` (Note: Khi ở dạng `static` thì sẽ không cần phải khởi tạo 1 object với class gốc mà chỉ cần khởi tạo thẳng 1 object nối tới `Inner class`)
