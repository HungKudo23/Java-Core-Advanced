# **Chương Package (Summary)**
## **Bài 12: Date (Ngày/tháng/năm)**
- Đoạn code ví dụ:
```java
import java.time.LocalDateTime; // For showing the current date/time
import java.time.format.DateTimeFormatter; // For formating date/time

public class Main {
    public static void main(String[] args) {
        
        LocalDateTime Date1 = LocalDateTime.now();
        System.out.println("Before formatting: " + Date1);
        DateTimeFormatter fd = DateTimeFormatter.ofPattern("dd-MM-yyyy HH:mm:ss");

        String Date2 = Date1.format(fd);
        System.out.println("After formatting: " + Date2);
    }
}
```
Kết quả:
```
Before formatting: 2022-11-17T14:17:47.274223800
After formatting: 17-11-2022 14:17:47
```

* Giải thích đoạn code
    + Đầu tiên sẽ import class `LocalDateTime` từ package **`java.time`** và class `DateTimeFormatter` từ package **`java.time.format`** để hiển thị thời gian hiện tại đã được định dạng để dễ xử lý hơn.
    + Hiện ra thời gian hiện tại chưa được định dạng bằng phương thức `now()`, rồi gán cho object `Date1` của class `LocalDateTime`.
    + Thực hiện định dạng thời gian bằng cách thiết lập một pattern theo dạng thời gian phổ biến như `dd-MM-yyyy HH:mm:ss` bằng phương thức `ofPattern()`, rồi gán cho object `fd` của class `DateTimeFormatter`.
    + Cuối cùng tạo biến `Date2` để thực hiện lưu thời gian `Date1` đã được format theo pattern đã thiết lập sẵn và hiển thị như kết quả.
<br><br>
* Class phổ biến của package `java.time`:
    + `LocalDate`: Dùng để hiển thị ngày hiện tại.
    + `LocalTime`: Dùng để hiển thị thời gian hiện tại.
    + `LocalDateTime`: Dùng để hiển thị ngày và thời gian hiện tại.
    + `DateTimeFormatter`: Dùng để định dạng thời gian dưới dạng con người có thể hiểu.
        + Phương thức ofPattern() có thể hiểu một vài định dạng phổ biến như:
            + yyyy-MM-dd
            + dd/MM/yyyy
            + dd-MMM-yyyy
            + E, MMM dd yyyy

