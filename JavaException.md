# **Chương Package (Summary)**
## **Bài 15: Exception**
- Là cách xử lí lỗi cho một đoạn code nếu có lỗi xảy ra.
- Đoạn code khai báo:
```java
    try {
        // Đoạn code để thực hiện nếu đúng
    } catch (Exception e) {
        // Đoạn code xử lí lỗi nếu sai
    }
```
hoặc:
```java
    try {
        // Đoạn code để thực hiện nếu đúng
    } catch (Exception e) {
        // Đoạn code xử lí lỗi nếu sai
    } finally {
        // Đoạn code sẽ luôn luôn chạy kể cả có lỗi xảy ra ở catch
    }
```

- Từ khóa `throw` :
    + Dùng để trả ra một Exception cụ thể nào đó:
    + Cách dùng:
    ```java
    throw new (loạiException)("miêu tả về lỗi");
    // VD:
    throw new ArithmeticException("Phép toán này thực hiện không đúng");
    ```
