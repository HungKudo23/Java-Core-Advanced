# **Chương OOP (Summary)**
## **Bài 3: Modifiers (từ khóa cấp bậc)**
### **Từ khóa cấp bậc truy cập**
- Với **`class`**:
    + *default*: Các class khác chỉ có thể truy cập class "này" khi ở cùng "package".
    + **`public`**: Class "này" có thể được truy cập bởi bất kì một class nào khác.
- Với **`thuộc tính, phương thức, hàm khởi tạo`**:
    + *default*: Các class khác chỉ có thể truy cập class "này" khi ở cùng "package".
    + **`public`**: Các class khác có thể sử dụng đoạn code trong các "thứ" trên.
    + **`private`**: Chỉ có những "thứ" có chứa đoạn code đó mới có thể sử dụng chính đoạn code nằm trong.
    + **`protected`**: Đoạn code có thể sử dụng khi ở cùng 1 package và các subclass.
### **Từ khóa không thuộc cấp bậc truy cập**
- Với **`class`**:
    + **`final`**: Class được khai báo kiểu này sẽ k thể được kế thừa từ các class khác.
    + **`abstract`**: Class có chứa từ khóa này k thể sử dụng để tạo một object mới.
+ Với **`thuộc tính, phương thức`**:
    + **`final`**: Giá trị của những "thứ" trên k thể bị ghi đè hoặc chỉnh sửa
    + **`static`**: Các "thứ" trên không thuộc về đối tượng mà sẽ thuộc về class đó luôn
    + **`abstract`**: Chỉ có thể được sử dụng thông qua phương thức nằm trong một class trừu tượng
    