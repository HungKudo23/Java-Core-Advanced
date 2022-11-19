# **Chương Package (Summary)**
## **Bài 17: Thread ( Luồng )**
- Luồng cho phép chương trình thực hiện tối ưu hơn bằng việc thực hiện nhiều công việc cùng một lúc và có thể sử dụng để thực hiện các tác vụ khó nhằn khác mà không ảnh hưởng tới chương trình chính.
- Cách tạo luồng:
    + Kế thừa lớp `Thread` và dùng phương thức `run()`:
    ```java
    public class Main extends Thread {
        public void run() {
            System.out.println("Đoạn code đang sử dụng luồng.");
        }
    }
    ```

    + Hoặc có thể triển khai giao diện `Runnable` và dùng phương thức `run()`:
    <br>
    ```java
    public class Main implements Runnable {
        public void run() {
            System.out.println("Đoạn code đang sử dụng luồng.");
        }
    }
    ```
- Điểm khác nhau giữa 2 cách:
    + Nếu dùng cách 1 thì sẽ không thể kế thừa bất kì lớp nào khác.
    + Nếu dùng cách 2 thì vẫn có thể kế thừa các class khác.
- Note:
    + Luồng trong Java có thể sẽ xảy ra lỗi luồng thực hiện đồng thời với nhau khiến cho việc kiểm soát giá trị của biến trở nên khó hơn, do đó hãy sử dụng phương thức `isAlive()` để kiểm soát luồng đang thực hiện:
    <br><br>
    ```java
    public class Main extends Thread {
        public static int amount = 0;

        public static void main(String[] args) {
            Main thread = new Main();
            thread.start();
            // Chờ luồng hiện tại thực hiện xong
            while (thread.isAlive()) {
                System.out.println("Waiting...");
            }
            // Cập nhật giá trị cho biến
            System.out.println("Main: " + amount);
            amount++;
            System.out.println("Main: " + amount);
        }

        public void run() {
            amount++;
        }
    }
    ```

