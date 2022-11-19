# **Chương Package (Summary)**
## **Bài 14: HashMap**
- HashMap khá giống ArrayList và LinkedList, chỉ khác ở việc HashMap lưu bằng cặp `key/values`.
- Đoạn code ví dụ:
```java
import java.util.HashMap; // For using HashMap

public class Main {
  public static void main(String[] args) {

    // Tạo object chứa key kiểu string và value kiểu int
    HashMap<String, Integer> people = new HashMap<String, Integer>();

    // Thêm từng key và giá trị của key
    people.put("John", 32);
    people.put("Steve", 30);
    people.put("Angie", 33);

    // Hiển thị ra màn hình console.
    for (String i : people.keySet()) {
      System.out.println("Key: " + i + ", " + "Value: " + people.get(i));
    }
  }
}
```

Kết quả:
```
Key: Angie, Value: 33
Key: Steve, Value: 30
Key: John, Value: 32
```

- Hàm riêng của HashMap:
    + Add (thêm mới): `put(key, value)`
    + Access (truy cập): `get(key)`
    + Remove (loại bỏ)
        + Loại bỏ một cặp: `remove(key)`
        + Loại bỏ tất cả các cặp: `clear()`
    + Kiểm tra số lượng cặp: `size()`
    + Chỉ hiện thị key: `keySet()` (thường dùng trong vòng lặp)
    + Chỉ hiển thị value: `values()` (thường dùng trong vòng lặp)