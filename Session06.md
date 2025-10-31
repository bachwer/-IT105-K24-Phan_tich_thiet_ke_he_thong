<h1>Ex 1: Chức năng mô tả nghiệp vụ: Hệ thống đặt vé xem phim online.</h1>

```mermaid
    flowchart TD
        C1[User]
        C2[Hệ thống thanh toán]
        
        A[Đặt chỗ]
        B[Chọn Nghế]
        C[Thanh Toán]
        D[Huỷ vé]
        E[Xem vé Đã đặt]
        
        
        C1 --> E
        C1 --> A
        A -.-> |<<include>>| B
        B -.-> |<<include>>| C
        E <-.- |<<extend>>|D
        C2 --> C
        
```

<h1>Ex2: Vẽ sơ đồ lớp (Class Diagram) </h1>

```mermaid
    classDiagram
        class Customer{
            -string idUser
            -string name
            -string address
            -string numberPhone
            +login()
            +signOut()
        }
        
        class ViewProduct{
            -string idProduct
            -string category
            -Double price
            -String name
            +getInfor()
            +AddTocart()
        }
        
        class Order{
            -String idOrder
            -String date
            -Boolean status
            +getInfor()
            +changeStatus()
        }
        
        class Payment{
            -String IdPay
            -String Data
            -Boolean Status
            +getData()
            +ViewHistory()
        }
        
        class contact{
            -String IdCon
            -String numberPhone
            -Boolean Status
            +call()
        }
        
        Customer --> ViewProduct
        ViewProduct --> Order
        Order --> Payment
        Customer --> contact


```

<h1>Ex 3: Chức năng mô tả nghiệp vụ: Hệ thống bán khóa học trực tuyến (E-learning).</h1>
<table>
    <tr>
        <th>Stakeholder</th>
        <th>Role</th>
        <th>Nguồn Y/c</th>
    </tr>
    <tr>
         <td>Student</td>
         <td>Người sử dụng chính, tham gia các khoá học, làm bài tập, và xem video bài giảng</td>
         <td>Mong muốn học tập trực tuyến, truy cập linh hoạt</td>
    </tr>
    <tr>
         <td>Giảng viên</td>
         <td>Có Trách nghiêm, nghiên cứu thêm sửa các bài giảng, video, bài kiểm tra đánh giá học viên, chấm điểm</td>
         <td>Cần công cụ dễ dùng, thao tác nhanh ngọn, quản lý nội dung và chấm diểm</td>
    </tr>
    <tr>
         <td>Admin</td>
         <td>Quản lý người dùng, khoá học, sử lý báo cáo và đảm bảo an toàn dữ liệu</td>
         <td>Cần hệ thống ổn định, bảo mật dễ bảo trì</td>
    </tr>
    <tr>
         <td>Bộ phận IT</td>
         <td>Giám sát hoạt động hệ thống, tài nguyên hệ thống, Sử lý lỗi kĩ thuật</td>
         <td>Cân khả năng theo dõi, log và phục hồi nhanh khi có sư cố</td>
    </tr>
</table>


<h3> Y/c Chứng năng (function requirement )</h3>
<table>
    <tr>
        <th>Y/c Chứng năng</th>
        <th>Mô tả</th>
    </tr>
    <tr>
        <td>Đăng Kí / nhập</td>
        <td>Hệ thống cho phép người dùng đăng kí và nhập để truy cập khoá học</td>
    </tr>
    <tr>
        <td>Tìm kiếm thông tin khoá học</td>
        <td>Người dùng có thể tìm kiếm được theo tên, chủ dề</td>
    </tr>
    <tr>
        <td>Đăng Kí khoá học</td>
        <td>cho phép người dùng có thẻ dăng kí khoá học phù hợp</td>
    </tr>
    <tr>
        <td>Làm bài kiểm tra Quiz</td>
        <td>Học viên có thể thực hiện bài kiểm tra trắc nghiệm</td>
    </tr>
    <tr>
        <td>theo dõi tiến trình học tập</td>
        <td>Học viên có thể xem phần trăm hoàn thanh khoá học</td>
    </tr>
    <tr>
        <td>Hệ thông thông báo</td>
        <td>Gửi thông báo khi có bài Ktra, sư kiện ..</td>
    </tr>
</table>

<h3> Y/c ko Chứng năng (non-function requirement )</h3>
<table>
    <tr>
         <th>Y/c Chứng năng</th>
        <th>Mô tả</th>
    </tr>
    <tr>
        <td>Hiệu suất</td>
        <td>Hệ thống phải hỗ trợ đc nhiều người dùng đăng nhập cùng lúc</td>
    </tr>
    <tr>
        <td>Bảo mật</td>
        <td>Mọi thông tin người dùng đều đc mã hoá</td>
    </tr>
    <tr>
        <td>Khả năng mở rộng</td>
        <td>Cho phép mở rộng sever khi lượng lớn học viên</td>
    </tr>
    <tr>
        <td>Khả năng Bảo trì</td>
        <td>Mã nguồn đc tổ chức module hoá, dễ nâng cấp, và sủa lỗi</td>
    </tr>
</table>


<h1>Ex 4: Nhận biết các loại hệ thống thông tin và mô hình phát triển phù hợp.</h1>

<table>
    <tr>
        <th>Loại hệ thống</th>
        <th>Vai trò hệ thống</th>
        <th>Giải Thích</th>
    </tr>
    <tr>
        <td>TPS(Transaction Processing System)</td>
        <td>Cối lõi của hệ thống</td>
        <td>Ghi nhập các xử lý giao dịch như tạo đơn, cập nhập trạng thái, xác nhận Giao Hàng</td>
    </tr>
    <tr>
        <td>MIS(Management Information System)</td>
        <td>Phân tích và báo cáo</td>
        <td>Cung cấp các báo cáo tổng hợp về số lượng đơn, hiệu suất nhân viên giao hàng, tỉ lệ giao hàng thành công..</td>
    </tr>
    <tr>
        <td>DSS (Decision Support System)</td>
        <td>Tối ưu tuyến đường va ra quyết định</td>
        <td>Hỗ trợ phân tích tuyến đường, dự báo nhu cầ vận chuyển, gợi ý cách phận bổ hàng</td>
    </tr>
    <tr>
        <td>EIS (Executive Information System)</td>
        <td>Phục Vụ Quản lý cấp cao</td>
        <td>Tồn hợp chỉ số KPI, biểu đồ hiệu suất, và xu hướng kinh doanh, để lãnh đạo ra quết định chiến lươc</td>
    </tr>
</table>


<h3>Mô hình phát triển Phần mền</h3>

<table>
  <tr>
        <th>Mô Hình</th>
        <th>Đặc điểm chính</th>
        <th>Ưu điểm</th>
        <th>Kết Luận</th>
    </tr>   
 <tr>
        <td>Waterfall</td>
        <td>Phát triển theo giai đoạn cố định: phân tích -> thiết kế -> Lập trình -> kiểm thử -> triển khai</td>
        <td>Phù họp cho dự án ổn định, ít that đổi, yêu cầu.Tuy nhiên logistics có nhiều biến động thực tế.</td>
        <td>Ko Phù hợp</td>
    </tr>
    <tr>
        <td>Agile/Scrum</td>
        <td>Phát triên linh hoạt theo từng chu kì ngắn (Sprint) có thể cập nhập tính năng theo phàn hồi người dùn</td>
        <td>Rất Phù hợp với ngành logisticsơi yêu cầu thay đổi liên tục (ví dụ: thêm phương thức giao, tích hợp bản đồ GPS mới).
 </td>
        <td>Khuyến nghi dùng</td>
    </tr>
    <tr>
        <td>Spiral Model</td>
        <td>Tập trung vào quản lý rủi ro, phát triển theo vòng lặp (iteration).
</td>
        <td>Phù hợp với các dự án phức tạp, rủi ro cao (ví dụ: tích hợp hệ thống AI route optimization).
</td>
        <td>Có thể áp dụng song song với Agile nếu hệ thống quy mô lớn.
</td>   
    </tr>
</table>


<h1>Ex 5: Vẽ sơ đồ lớp (Class Diagram) để biểu diễn các đối tượng trong hệ thống: Sinh viên, Lớp học, và Môn học.</h1>

```mermaid
    classDiagram
        class Student{
            -String idStudent
            -String Name
            -String Age
            -String class
            +showInfor()
            +showClass()
            
        }
        
        class Class{
            -String IdClass
            -String Name
            -String Teacher
            +getInfor()
            
        }
        
        class Subject{
            -String Name
            -String IdSub
            -String Class
            -int CreditOfNumber
            +getInfor()
            
        }
        Student "N" -->"N" Class : THam Gia
        Class "N" --> "n" Subject: giangDay
        
        
```


<h1>Ex 6: hệ thống quản lý thư viện trực tuyến</h1>

```mermaid
    flowchart TD
        A1[User]
        A2[Admin]
        
        UC1((đăng kí tài khoản))
        UC11((Đăng Nhập))
        UC2((Tìm Kiếm Sách))
        UC3((Mượn Sách))
        UC4((Trả Sách))
        UC5((Quản Lý Sách)) 
        
        
        A1 --> UC1
        A1 --> UC11
        UC11 --> UC2
        UC2 --> UC3
        UC2  -.-> |<<include>>| UC4

        A2 --> UC5
        A2 --> A1
```

```mermaid
    classDiagram
        class User{
            -String idUser
            -String Name
            -String Address
            -String numberPhone
            +Login()
            +signOut()
        }
        
        class Admin{
            -String IdAdmin
            -String Name
            -List<User> User
            +AddBook()
            +EditBook()
            +DeleteBook()
        }   
        
        class Book{
            -String IdBook
            -String Name
            -Boolean Status
            +getInfor()
            +ChangeStatus()
        }
        
        class BookLoanSlip{
            -String Id
            -String dateBorwing
            -String DateReturn
            +createNew()
            +update()
        }
        
        User "1" --> "N" BookLoanSlip: Create
        BookLoanSlip "1" -->"1" Book
        Admin "1" --> "0..*" Book : quản lý >
        Admin "1" --> "0..*" User : quản lý >
```

<h3>3. Giải thích logic chuyển đổi từ Use Case -> Class</h3>
<ol>
    <li>Xác Định Actor Chính, người dùng, admin  -> lớp người dùng, adnin</li>
    <li>Mỗi UseCase chính phương thức đăng kí đăng nhập</li>
    <li>Thực thể sác, phiếu mượn</li>
    <li>Include / Extend trong Use Case</li>
    <li>......</li>
</ol>


<h1>Ex 7: Vẽ Sequence Diagram </h1>

```mermaid
sequenceDiagram
    autonumber
    actor U as User
    participant S as Hệ thống
    participant DB as Cơ sở dữ liệu
    participant Cart as Giỏ hàng
    participant Ord as Đơn hàng
    participant Pay as Cổng thanh toán

    %% 1) Đăng nhập
    U ->> S: Đăng nhập(username, password)   %% Synchronous
    S ->> DB: verifyCredentials(username, password)
    DB -->> S: Kết quả xác thực (userInfo/failed)

    alt Đăng nhập thành công
        %% 2) Tìm sản phẩm
        U ->> S: Tìm sản phẩm(từ khóa)
        S ->> DB: searchProducts(keyword)
        DB -->> S: Danh sách sản phẩm
        S -->> U: Hiển thị kết quả

        %% 3) Thêm sản phẩm vào giỏ (lặp)
        loop Mỗi sản phẩm muốn thêm
            U ->> S: addToCart(productId, qty)
            S ->> DB: upsertCart(userId, productId, qty)
            DB -->> S: Cart updated
            S -->> U: Xác nhận đã thêm
        end

        %% 4) Đặt hàng
        U ->> Ord: Tạo đơn hàng từ giỏ
        Ord ->> DB: createOrder(userId, cart)
        DB -->> Ord: orderId, amount
        Ord -->> U: Yêu cầu thanh toán(orderId, amount)

        %% 5) Thanh toán
        U ->> Pay: Thanh toán(orderId, amount)
        Pay -->> U: Kết quả tạm thời (pending)

        Note over Pay,S: Webhook callback (asynchronous)
        Pay -->> S: notifyPayment(orderId, status)   %% Asynchronous callback
        S ->> DB: updateOrderStatus(orderId, status)
        DB -->> S: OK

        alt Thanh toán thành công
            S -->> U: Xác nhận đơn hàng & biên nhận
        else Thanh toán thất bại
            S -->> U: Thông báo thất bại & hướng dẫn thử lại
        end
    else Đăng nhập thất bại
        S -->> U: Thông báo sai thông tin đăng nhập
    end
```
<h1>Ex 8: Chức năng mô tả nghiệp vụ: Quản lý sinh viên</h1>

```mermaid
    flowchart TD
        A[Admin]
        
        UC1((AddStudent))
        UC2((EditStudent))
        UC3((DeleteStudent))
        UC4((ViewAllStudents))
        
        A --> UC1
        A --> UC2
        A --> UC3
        A --> UC4

```

```mermaid
    classDiagram
        class Student{
            -String idStudent
            -String Name
            -String Class
            -String Address
            +getInfor()
        }
        
        class Teacher{
            -String IdTeacher
            -String Name
            -String Address
            +getInfor()
            +getClass()
        }
        
        class Admin{
            List<Student> Student
            List<Teacher> Teacher
            +getAddStudent(Student)
            +Delet(IdStudent)
            +Update(Student)
            +getAddStudent(Student)
            ...()
        }
        
        
        Admin "1" -->  "N" Student
        Admin "1" --> "N"Teacher

```



```mermaid
    sequenceDiagram
        autonumber
        actor C as admin
        participant System as Hệ thống
        participant CSDL as Cơ sở dữ liệu
        
        C ->> System: Đăng Nhập
        System ->> CSDL: Kiểm tra Tài Khoản
        CSDL -->> System: trả kết quả
        
        alt Đăng Nhập Thành công
            C ->> System : Tương Tác Thêm Sinh viên
            System ->> CSDL: Gửi Y/c Validate và lưu vào DB
            CSDL -->> System: Send Success
            System -->> C: Thông báo thêm thành công
        else Đăng Nhập Thất bại
            System -->> C: Thông báo đăng nhập thất bại
        end
```

<ul>
    <h3>Class → Sequence</h3>
    <li>“Add/Edit/Delete/View” <-> phương thức của StudentManagementSystem (addStudent, updateStudent, deleteStudent, listStudents).</li>
    <li>Actor Admin <-> đối tượng gọi (caller) dùng Admin.</li>
    <li>Thực thể Student/Teacher ↔ lớp dữ liệu (Student, Teacher) </li>
    <h3>Class -> Sequence</h3>
    <li>Lời gọi addStudent(Student) trong lớp admin được triển khai bằng luồng tuần tự:</li>

</ul>

