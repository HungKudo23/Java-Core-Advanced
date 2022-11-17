# **Chương OOP (Summary)**
## **Bài 1: Class và Object**
- Khai báo:
    + Class:
    ```java
        class (tên class){
            // Đoạn code sẽ được viết trong này...
        }
    ```
    + Object: 
    ```java
        (tên class) (tên object) = new (tên class)()
    ```
    VD:<br>
    ```java
        Main newObj = new Main();
    ```
- Cách sử dụng thuộc tính trong class đã khai báo:<br>
    `(tên object).(thuộc tính);`<br>
    VD:<br>
    ```java
    System.out.println(newObj.x);
    ```
- Giá trị của thuộc tính trong class cũng có thể được ghi đè hoặc chỉnh sửa khi đã truy cập thuộc tính của class đó


