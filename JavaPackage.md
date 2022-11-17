# **Chương Package (Summary)**
## **Bài 10: Package (Gói)**
- Package có 2 loại:
    - Package có sẵn
    - Package tự tạo
- Về package có sẵn hãy tham khảo tại ( Phiên bản khuyên dùng hiện tại tại thời điểm viết là `17.0.5` )
    [https://docs.oracle.com/en/java/javase/17/docs/api/index.html](https://docs.oracle.com/en/java/javase/17/docs/api/index.html)
- Cách khai báo:
    + Package có sẵn:
    ```java
    import (tên_package);
    ```
    VD:
    ```java
    import java.util.*;
    // hoặc có thể chỉ định class cụ thể như lệnh sau: 
    import java.util.Scanner;
    ```
    + Package tự tạo:
    ```java
    package (tên_package);
    ```
- Note:
    + Dấu `*` nghĩa là sẽ import toàn bộ class trong package đó vào file 
    + Cách sử dụng package tự tạo:
        + Biên dịch file trước
        + Rồi biên dịch package bằng `-d .`
        + Chạy file bằng cú pháp trong Terminal:
        ```sh
        java (tên_package.tên_file)
        ```