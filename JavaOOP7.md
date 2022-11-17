# **Chương OOP (Summary)**
## **Bài 7: Abstraction (Tính trừu tượng)**
- **`Data abstraction`** ( dịch ra là **Trừu tượng hóa dữ liệu** ) với mục đích sẽ ẩn đi một số chi tiết nhất định và chỉ hiển thị thông tin cần thiết tới người dùng.
- `Class trừu tượng`: Là loại class mà sẽ không cho phép người dùng tạo object bên trong chúng.
- `Phương thức trừu tượng`: Là phương thức chỉ có thể được truy cập và sử dụng khi ở trong `Class trừu tượng`, và là loại phương thức không có phần thân.
- Đoạn code ví dụ:
```java
abstract class Animal { // Class trừu tượng
  public abstract void animalSound(); // Phương thức trừu tượng
  public void sleep() {
    System.out.println("Zzz");
  }
}

class Pig extends Animal {
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}

class Main {
  public static void main(String[] args) {
    Pig myPig = new Pig(); 
    myPig.animalSound();
    myPig.sleep();
  }
}
```
- Giải thích:
    + Phương thức `animalSound()` ở class `Animal` được khai báo với từ khóa **`abstract`** nên để có thể viết code cho phương thức đó thì sẽ phải có class khác kế thừa class `Animal` để có thể thực hiện viết code cho phương thức `animalSound()` đó, từ đó mới có thể sử dụng phương thức đó cho các class k phải trừu tượng khác
<br><br><br>

- Từ khóa `interface`:
  + là class trừu tượng đặc biệt mà chỉ chứa các phương thức mà không có đoạn code bên trong khi khai báo.
  + Cách truy cập phương thức nằm trong `interface`:
      + Khai báo class mới với từ khóa **`implements`** thay vì **`extends`** của "tính thừa kế"
  + Note:
      + `interface` cũng không thể tạo một object mới giống như các class trừu tượng.
      + Khi thực hiện `implement (triển khai)` một `interface` thì bạn buộc phải ghi đè tất cả phương thức nằm trong `interface` đó.
      + Từ khóa truy cập mặc định của **phương thức** nằm trong `interface` là: **`abstract`** và **`public`**.
      + Từ khóa truy cập mặc định của **thuộc tính** nằm trong `interface` là: **`static`** , **`public`** , **`final`**.
      + Một `interface` không thể có hàm khởi tạo 