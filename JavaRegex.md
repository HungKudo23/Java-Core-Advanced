# **Chương Package (Summary)**
## **Bài 16: Regular Expression in Java (Biểu thức điều kiện)**
- ( Về kiến thức cơ bản của biểu thức điều kiện hãy vào đường link:
[https://regexr.com/](https://regexr.com/) )
- ( Hoặc chi tiết về cách sử dụng của chúng trong Java:
[https://www.w3schools.com/java/java_regex.asp](https://www.w3schools.com/java/java_regex.asp) )

- Đoạn code ví dụ:
```java
import java.util.regex.Matcher; // For searching a pattern
import java.util.regex.Pattern; // For defining a new pattern

public class Main {
    public static void main(String[] args) {
        // Tạo một pattern rồi gắn cho flag k phân biệt chữ hoa, chữ thường.
        Pattern pattern = Pattern.compile("java", Pattern.CASE_INSENSITIVE);
        // Tạo một trình kiểm tra (matcher) để kiểm tra xem liệu regex phía trên có nằm
        // trong dữ liệu input không.
        Matcher matcher = pattern.matcher("Xin chào Java");
        if (matcher.find()) { // Nếu regex nằm ở trong input của matcher ...
            System.out.println("Đã tìm thấy sự trùng khớp.");
        } else {
            System.out.println("Không tìm thấy sự trùng khớp.");
        }
    }
}
```
Kết quả:
```
Đã tìm thấy sự trùng khớp.
```
- Flag ( cờ ) của phương thức **`compile()`**:
    + `Pattern.CASE_INSENSITIVE`: DÙng để loại bỏ kiểm tra chữ hoa, chữ thường.
    + `Pattern.LITERAL`: Kí tự đặc biệt trong pattern sẽ không mang nghĩa gì đặc biệt và sẽ được coi là kí tự bình thường khi thực hiện tìm kiếm pattern.
    + `Pattern.UNICODE_CASE`: Kết hợp với flag `Pattern.CASE_INSENSITIVE` để loại bỏ trường hợp kí tự nằm ngoài bảng chữ cái tiếng Anh.