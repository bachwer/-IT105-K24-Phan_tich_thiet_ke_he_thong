<h1>Ex 1: Xác định danh sách các lớp phù hợp</h1>
    <h3>1. Book</h3>
        - Vài trò: Lớp thực thể chính <br>
        - Đại diện cho thông tin của từng quyển sách
    <h3>2. Reader</h3>
        -Vai trò: Lớp thực thể, mô tả người dùng hệ thống <br>
        -Lưu Chữ thông tin về độc giả - những người có liên quan mượn và trả sách
    <h3>3. Librarian</h3>
        -Vai Trò: Lớp điều hành/ Quạn trị hệ thống <br>
        -Quản lý sách và hỗ trợ độc giả ( mượn, trả sách )

```mermaid
    classDiagram
    class Book {
    -String bookID
    -String title
    -String author
    -String publishYear
    -Boolean status
    +getStatus()
    +setStatus(Boolean newStatus)

    }

    class reader {
        -String userID
        -String FullName
        -String address
        -String phoneNumber
        +borrowBook(Book Book)
        +return(book book)
    }
    
    
    class Librarian {
        -String userID
        -String fullName
        -String position
        +addBook(Book Book)
        +managerBorrowing(Reder reader, Book Book)
    }

```


<h1>Ex 2: Nhận diện loại quan hệ và giải thích.</h1>
<table>
    <tr>
         <th>Mối Quan Hệ</th>
         <th>Loại Quan Hệ</th>
         <th>Giải thích</th>
         <th>Ký hiệu UML</th>
    </tr>
    <tr>
         <td>Một Giáo Viên Giảng Dạy nhiều lớp học</td>
         <td>Association</td>
         <td>Giáo Viên vào lớp học có mối quan hệ logic với nhau: Một Giáo viên có thẻ dạy nhiều lớp, và một lớp có thể có nhiều giáo viên</td>
         <td>Đường nối Đơn </td>
    </tr>
    <tr>
         <td>Một Đơn hàng gồm nhiều sp</td>
         <td>Aggregation</td>
         <td>Đơn hàng chứa nhiều sp, nhưng sp vẫn tồn tại đôc lập, nếu đơn hàng bị xoá, đây là mối quan hệ có nhưng ko phụ thuộc</td>
         <td>Đường nối có hình kim cương rỗng ở phía đơn hàng</td>
    </tr>
    <tr>
        <td>Một cơ thể gồm nhiều bộ phận không thể tách rời</td>
         <td>Composition</td>
         <td>các bộ phận là thành phân bắt buộc của cơ thể. Nếu cơ thể không tồn tại, thì các bộ phận cx ko tồn tại, không thể hoạt động độc lập</td>
         <td>Đường nối có hình kim cương đặc ở phía cơ thể</td>
    </tr>
</table>


<h1>Ex 3: Áp dụng các phạm vi truy cập truy cập (public, private, protected)</h1>

<table>
    <tr>
        <th>Thành Phần</th>
        <th>Modifier</th>
        <th>Giải Thích</th>
    </tr>
    <tr>
        <td>UserName</td>
        <td>Private</td>
        <td>Vì UserName Là thông tin người dùng, => được bảo mật</td>
    </tr>
    <tr>
         <td>PassWord</td>
         <td>Private</td>
         <td>Vì PassWord cùng là thông tin người dùng cần đc bảo mật</td>
    </tr>
     <tr>
         <td>Login</td>
         <td>Public</td>
         <td>Vì Login là hành động truy cập từ bên ngoài => công khai các lơp để gọi và đăng nhập</td>
    </tr>
     <tr>
         <td>resetPassword</td>
         <td>Public</td>
         <td>Là hành động công khai, Người dùng có thể gọi để đôi mk khi cần</td>
    </tr>
     <tr>
         <td>lastLoginTime</td>
         <td>Protected</td>
         <td>thông tin đăng nhập cuối cùng, để kiểm tra hoạt động người dùng, => Không lên công khai cho lớp khác</td>
    </tr>
</table>



<h1>Ex 4:Diễn tả sơ đồ Class gồm 2–3 lớp có quan hệ đơn giản </h1>

```mermaid
    classDiagram
    class Customer {
    -String userID
    -String Name
    -String phoneNumber
    -Boolean status
    +placeOrder(Order order)
    }
    
    
    class Order {
        -string orderId
        -string date
        +addProduct(Product d)
        +caculateTotal()
    }
    
    class Product{
        -string productID
        -string name
        -double price
        +getInfor()
    }
    
    Customer "1" --> "n"Order
    Order "n" --o "n" Product
    
    
```

<h1>Ex 5:Trình bày danh sách thuộc tính và phương thức dưới dạng bảng hoặc mô hình UML đơn giản </h1>

```mermaid
    classDiagram
    class Order{
        -string orderID
        -String date
        -double totalAmount
        -String Status
        +addProduct(Product p) void
        +calculateTotal() double
        +updateStatus(Status s) void
        +printOrderInfor() void
        
    }
```

<h1>Ex 6: Biểu diễn quan hệ 1–1, 1–N, N–N đúng cú pháp UML.</h1> 

```mermaid
classDiagram
    class Teacher
    class Course
    class Student

    Teacher "1" --> "N" Course 
    Course "N" --> "N" Student
```



<h1>Ex 7: </h1>

```mermaid
classDiagram
    class Customer{
        -String: userId
        -String: userName
        -String: address
        -String phoneNumber
        +placeOder(o Order) void
 }
 
    class Order{
        -String: orderID
        -String: date
        -Double: totalAmount
        -String: Status
        +addProduct(Product p) void
        +calculateTotal() double
        +updateStatus(Status s) void
        +printOrderInfor() void
    }
    
    class ProductView{
        -String: productId
        -String name
        -Double price
        +getInfor() String
    }
    
    class PayMent{
        -Boolean: PayStatus
        +payNow(Double n) void
    }
    
    
    
    
    Customer "1" --> "n" ProductView
    Customer "1" --> "n" Order
    Order "1" --> "1" PayMent
    

```

<h1>Ex 8: Thiết kế mô hình lớp cho hệ thống đăng ký học phần</h1>

```mermaid
    classDiagram
        class User { 
            -Stirng email
            -String password
            -String role
            +Login()
            +Logout()
        }
        
        class Student{
            -String studentId
            -String studentCode
            -String Name
            +registration(subject s) void
        }
        
        class Teacher{
            -String teacherID
            -String Name
            +ClassInCharge()
        }
    class PhongDaoTao {
            -String code
            -String tenPhong
            -String truongPhong
            -String soDienThoai
            -String email
            -String diaChi
            -List~MonHoc~ danhSachMonHoc
            -List~LopHoc~ danhSachLopHoc
            -List~GiangVien~ danhSachGiangVien
            -String keHoachDaoTao
            -int namHocHienTai
            +themMonHoc(MonHoc m)
            +xoaMonHoc(String maMon)
            +themLopHoc(LopHoc l)
            +phanCongGiangVien(GiangVien gv, MonHoc m)
            +xemKeHoachDaoTao()
    }
        
        
        class Class{
            -String classId
            -int QuantityStudent
            -string Date
            -String teacherName
            +getListStudent()
        }
        
        class Subject{
            -String subId
            -String name
            -String Date
            -int NumberOfCredit
            -String teacherName
            +getInfor()
        }
        
        class Registration{
            -string SubjecId
            -String Date
            -String SutudentCode
            +Submit()
        }
        
        
        
        
        User <|-- Student : kế thừa
        User <|-- Teacher : kế thừa
        
        
        Student "1" <--  "n" Registration
        
        Teacher "1" --> "n" Class
        
        
        Student "n" --> "n " Class

        Subject "1" --> "n " Class
        
        
        PhongDaoTao "1" --o Class : Aggregation
        PhongDaoTao "1" --o Subject: Aggregation
        

        

```




<h1>Ex 9: Vẽ lại sơ đồ Class cải tiến</h1>

```mermaid
    classDiagram
        class User{
            -String Username
            -String password
            -string email
            +login()
            +resetPassword()
        }
        class Order{
            -string OrderId
            -string orderDate
            -string totalAmount
            +caculateTotal()
 }
 
 User "1" --o "n" Order

```

<h3>Giải thích</h3>
<ul>
    <li>Lỗi quan hệ giữa các lớp ( có thể ): Nếu chỉ mô tả User có thể đặt hàng, thì ( không cần quản lý vòng đợi thì có thể dùng Association ) nếu muốn quản lý vòng đời oder để thông kê, order tồn tại riêng biệt thì dùng Aggregation</li>
    <li>Lỗi multiplicity: Vì Một User có thể, có nhiều order => 1 -> "n" order</li>
    <li>Lỗi modifier: các thuộc tích bên trong class user, order cần được để private, vì đó là thông tin ca nhân của 1 user "-"</li>
</ul>

<h1>Ex 10: thiết kế Class Diagram cho hệ thống E-learning</h1>



```mermaid
    classDiagram
        class User{
            -String userName
            -String password
            -String email
            +login()
        }
        
        class Student{
            -String studentId
            -String studentCode
            -String Gender
            -String Name
            
        }
        
        class Teacher{
            -String TeacherID
            -String name
            -String Gender
        }
        
        class Course{
            -String courseID
            -String Name
            -String quanityStudent
            -String date
            -int NumberOfCredit
            +getInfor()
        }
        
        class Lesson{
            -String lessonId
            -String Name
            +getInfor()
        }
        
        class Document{
            -String documentId
            -String Name
            +getInfor()
        }
        class Quiz{
            -String quizId;
            -int quanityQuiz
            +getData()
        }


    User <|-- Student : kế thừa
    User <|-- Teacher : kế thừa
    
    
    Course "1" --o "N" Lesson
    
    Lesson "1" *-- "N"Document
    Lesson "1" *-- "N" Quiz
    
    
    
    Student "N" --> "N" Course
    Teacher "1" --> "N" Course
    
    
    
    

```

