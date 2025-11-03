<h1>Ex 1: Phân tích kiến trúc của hệ thống bán hàng đa nề tảng</h1>
<p>Hệ thống bán hàng đc triển khai theo mô hình 3-tier acrchieture gồm:</p>
<ul>
    <li>Frontend: Giao Diện người dùng</li>
    <li>Backend: sử lý logic nghiệp vụ, API</li>
    <li>Database: Lưu trữ dữ liệu, CSDL</li>
</ul>

<h3>Các thành phần chính/h3>
<ul>
    <li><strong>Frontend:</strong> Đăng kí /nhâp; tìm kiếm sp, xem chi tiết thanh toán và quản lý đơn hàng</li>
    <li><strong></strong></li>
    <li></li>
    <li></li>
    <li></li>
</ul>

<h3>Sơ đồ kiến trúc tổng thể</h3>
```mermaid
    flowchart TB
    subgraph Client["Frontend Layer"]
        Web[Web App React / Angular]
        Mobile[Mobile App Flutter / React Native]
    end
    
    subgraph Backend["Backend Layer"]
        API[API]
        Logic["Logic Hệ thống"]
        Auth["Bảo mật dữ liệu"]
    end
    
    subgraph DB["Database Layer"]
        SQL[(CSDL)]

    end
    
    subgraph EX["External Services"]
        Pay["Payment Gateway"]
        Ship["Shipping services"]
        Email["Email, notification"]
    end


    Client --> |HTTP/ JSON| API
    API --> Auth
    API --> Logic
    Logic --> SQL
    Logic --> Pay
    Logic --> Ship
    Logic --> Email
```


<h1>Ex2: Tổng quan về kiến trúc 3 tầng</h1>


    
```mermaid
    flowchart TD
    subgraph Presentation["Presentation Tier (Giao diện)"]
        UI["Web/Mobile App\n(React, Flutter)"]
    end

    subgraph Business["Business Logic Tier (Xử lý nghiệp vụ)"]
        Service["Warehouse Service\n(Quản lý nghiệp vụ)"]
        Controller["Controller / API\n(REST / GraphQL)"]
    end

    subgraph Data["Data Access Tier (Truy cập dữ liệu)"]
        DAO["Data Access Object\n(ProductDAO, SupplierDAO, InventoryDAO)"]
        DB[(MySQL / PostgreSQL)]
    end

    UI --> Controller --> Service --> DAO --> DB

```
<h3>Phân tầng chi tiết</h3>
<ul>
    <li><strong>Presentation: </strong>Là nơi, người dùng tương tác với hệ thống, hiện thị danh sánh sp, nhà cung , tồn kho ...</li>
    <li><strong>Business Logic: Xử lý logic trung gian, kiểm tra dữ liệu đkien nghiệp vuj, tính toán tồn kho, kết hợp dữ liệu từ Data</strong></li>
    <li><strong>Data Access Tier: </strong>Là tầng giao tiếp trực tiếp với CDSL, thực hiện truy vấn CRUD, cung cấp interface</li>
</ul>


<h1>Ex3 :L sơ đồ package/module của hệ thống đặt vé máy bay.</h1>

```mermaid
    flowchart TD
        subgraph UI["Module: Giao diện người dùng"]
            SearchUI["Tìm kiếm chuyến bay"]
            BookingUI["Đặt vé"]
            PaymentUI["Thanh toán"]
            AccountUI["Quản lý tài khoản"]
        end
        
        subgraph Logic["Module: Sử lý nghiệp vụ"]
            SearchService["SearchService"]
            BookingService["BookingService"]
            PaymentService["PaymentService"]
            AccountService["AccountService"]
        end
        
        subgraph Data["Module: truy Cập dữ liệu"]
            FlightDAO["FlightDAO"]
            BookingDAO["BookingDAO"]
            PaymentDAO["PaymentDAO"]
            UserDAO["UserDAO"]
            Database[(CSDL - MySQL/PostgreSQL)]
        end

    SearchUI --> SearchService --> FlightDAO --> Database
    BookingUI --> BookingService --> BookingDAO --> Database
    PaymentUI --> PaymentService --> PaymentDAO --> Database
    AccountUI --> AccountService --> UserDAO --> Database


```

<h1>Ex4: Hệ thống bán hàng online </h1>

```mermaid
    flowchart TD
        subgraph UI 
            orderUI["OrderController"]
        end
        
        subgraph Logic 
            orderSV["OrderService"]
        end
        
        subgraph DB 
            OrderR[OrderRepository]
            DB[(Database)]
        end

    orderUI --> orderSV --> OrderR --> DB
        
```
<h3>UML Class Diagram</h3>

```mermaid
   classDiagram
       class Order{
           -int id
           -String date
           -double totalAmount
           -String status
           -List~OrderItem~items
           +calculateTotal() Double
       }
        
        class OrderItem{
            -int id
            -String productName
            -int quantity
            -double price
            +getSubTotal() double
            
        }
    class OrderService {
        -OrderRepository orderRepo
        +createOrder(Order)boolean
        +getOrderById(int) Order
        +updateOrderStatus(int, String)boolean
        +calculateTotalAmount(Order) double
    }

    class OrderRepository {
        +save(Order) boolean
        +findById(int) Order
        +updateStatus(int, String) boolean
        +delete(int) boolean
    }

    OrderService --> OrderRepository
    Order --> OrderItem
        

```

<h1>Ex5: Hệ thống blog cá nhân,</h1>
<h3>1.Presentation: </h3>
<ul>
    <li>PostController: Quản lý yêu cầu tạo, sửa đọc bài viết</li>
    <li>CommentController: xử lý y/c thềm sửa xoá bình luận</li>
    <li>UserController: xử lý đăng nhập, đăng kí, quản lý Tk</li>
    <li><strong>Vai trò</strong>: Nhận request từ client, gọi business layer, trả response HTML JSON ..</li>
</ul>

<h3>2.Business Layer </h3>
<ul>
    <li>PostService: xử lý nghiệp vụ bài viết</li>
    <li>CommentService: sử lý nghiệp vụ bình luận</li>
    <li>UserService: Xác thực đăng nhập, đăng kí..</li>
    <li><strong>Vai trò</strong>: thực hiện quy tác nghiệp vụ, ko có phép xoá bình luận của ngkach gọi data để dọc ghi dữ liệu</li>
</ul>
<h3>Dada Access Layer</h3>
<ul>
    <li>PostRepository: CRUD bài viết</li>
    <li>CommentRepository: CRUD bình luận</li>
    <li>UserRepository: CRUD người dùn, xác thực ĐN</li>
    <li><strong>Vai trò:</strong> Giao tiếp với CSDL, thực thi câu lệnh SQL..</li>
</ul>

```mermaid
    flowchart TD
        subgraph Presentation["Giao Diện Hệ Thống"]
            Post["Post"]
            Comment["Comment"]
            User["User"]
        end
        
        subgraph BusinessLayer["Logic nghiệp vụ"]
            Post1["PostService"]
            Comment1["CommentService"]
            User1["UserService"]
        end
        
        subgraph DataAccessLayer["data"]
            PostRepository
            CommentRepository
            UserRepository
            CSDL[(CSDL)]
        end

    Post --> Post1 --> PostRepository -->CSDL
    Comment --> Comment1 --> CommentRepository -->CSDL
    User --> User1 --> UserRepository -->CSDL
```

```mermaid
classDiagram
    class Post {
        -int id
        -String title
        -String content
        -User author
        -Date createdAt
        -List~Comment~ comments
        +editContent(String): void
    }

    class Comment {
        -int id
        -String text
        -User author
        -Date createdAt
        +editText(String): void
    }

    class User {
        -int id
        -String username
        -String password
        -String role
        +checkPermission(String): boolean
    }

    class PostService {
        -PostRepository postRepo
        +createPost(Post): boolean
        +updatePost(Post): boolean
        +deletePost(int): boolean
        +getPostById(int): Post
        +getAllPosts(): List~Post~
    }

    class CommentService {
        -CommentRepository commentRepo
        +addComment(Comment): boolean
        +editComment(Comment): boolean
        +deleteComment(int): boolean
        +getCommentsByPostId(int): List~Comment~
    }

    class UserService {
        -UserRepository userRepo
        +register(User): boolean
        +login(String, String): boolean
        +updateUser(User): boolean
    }

    class PostRepository {
        +save(Post): boolean
        +update(Post): boolean
        +delete(int): boolean
        +findById(int): Post
        +findAll(): List~Post~
    }

    class CommentRepository {
        +save(Comment): boolean
        +update(Comment): boolean
        +delete(int): boolean
        +findByPostId(int): List~Comment~
    }

    class UserRepository {
        +save(User): boolean
        +findByUsername(String): User
        +update(User): boolean
    }

    PostService --> PostRepository
    CommentService --> CommentRepository
    UserService --> UserRepository
    Post --> Comment
    Post --> User
    Comment --> User
```


<h1>Ex6: Hệ thống bán lẻ  </h1>

```mermaid
    flowchart TD
        subgraph Presentation["Giao Diện hệ thống"]
            Application[Application]
        end
        
        subgraph BusinessLayer["Logic Hệ thống"]
            Api["Api Getway"]
        
        
           subgraph BM["Business Module"]
                PaymentService["xử lý Thanh toán"]
                EmailService["Gửi xác nhận Email"]
                InventoryService["Quản lý tồn kho"]
                OrderService["xử lý đơn hàng"]
               end
        end
        
        subgraph Data["DataAccessLayer"]
            SQL[(Database)]
        end
        
        subgraph ExternalService["ExternalService"]
            VPN[VNPay Service]
            Email[Email SMTP]
        end

    Application --> Api

    Api -->PaymentService --> VPN
    Api -->EmailService --> Email
    Api -->InventoryService --> SQL
    Api --> OrderService --> SQL
    
        

```

<h1>Ex7: mô tả nghiệp vụ: Một hệ thống học trực tuyến</h1>
<ul>
    <li>Đăng kí tài khoản -> UserManagement -> xử lý tạo tài khoản, lưu thông tin người dùng, xác thục email</li>
    <li>Đăng Nhập -> Authentication -> xử lý xác thực tài khoản, tạo token truy cập, phân quyền người dùng</li>
    <li>Xem Khoá Học -> courseManagement -> quản lý danh sách khoá, hiện thị nội dung và thông tin, chi tiết khoá học</li>
    <li>Làm Bài Quiz -> QuizManagement -> Quản lý câu hỏi, lưu kết quản lý..</li>
    <li>Xem kết quả -> ResultManagement -> hiện thị điểm, lưu diểm, tổng hợp kết quả môn học,..</li>
</ul>

```mermaid
   flowchart TB
        subgraph Frontend["Frontend Layer (Tầng giao diện)"]
            FE_UI[Web/Mobile interface]
            FE_Course[Course]
            FE_Quiz[Quiz]
        end
        
        subgraph Backend["Backend Layer"]
            UM["User Management"]
            AUTH["Authentication"]
            CM["Course Management"]
            QM["Quiz Management"]
            RM["Result Management"]
        end
        
        subgraph DB[Database layer]
            DB_User["User Table"]
            DB_Course["Course Table"]
            DB_Quiz["Quiz Table"]
            DB_Result["Result Table"]
        end


FE_UI --> UM --> DB_User
FE_UI --> AUTH --> DB_User
FE_UI --> RM --> DB_Result


FE_Course --> CM --> DB_Course
FE_Quiz --> QM --> DB_Quiz


```




<h1>Ex8: Hệ thống bán hàng online </h1>

```mermaid
    flowchart TB
        subgraph Frontend["Giao Diện người dùng"]
            FE_MP["Quản lý SP"]
            FE_MQ["Quản lý Order"]
            FE_SG["Đăng Nhập"]
            FE_DT[Xem báo cáo doanh thu]
        end

        subgraph  BusinessLogicLayer["xử lý nghiệp vụ"]
            ViewR[View revenue reports]
            Product[Product Management]
            Order[Order Management]
            Auth[Authentication]
        end
        
        subgraph DataAccessLayer[Database]
            SQL[(SQL)]
            
        end
    FE_MP --> Product --> SQL
    FE_MQ --> Order --> SQL
    FE_SG -->  Auth --> SQL
    FE_DT --> ViewR --> SQL



```

<ul>
     <li>Presentation: Lớp Giao Diện người dùng</li>
     <li>Business Logic Layer: Lớp xử lý logic nhiệp vụ</li>
     <li>DataAccessLayer: lớp data, lưu data hệ thống, User</li>
</ul>



<h1>Ex9: Hệ thống thương mại điện tử </h1>

```mermaid
    flowchart TB
    subgraph UserManagement["User Management"]
        UM1[UserService]
        UM2[AuthService]
        UM3[UserRepository]
    end

    subgraph ProductManagement["Product Management"]
        PM1[ProductService]
        PM2[ProductRepository]
    end

    subgraph CartManagement["Cart Management"]
        CM1[CartService]
        CM2[CartRepository]
    end

    subgraph OrderManagement["Order Management"]
        OM1[OrderService]
        OM2[OrderRepository]
    end

    subgraph PaymentManagement["Payment Management"]
        Pay1[PaymentService]
        Pay2[PaymentGateway]
    end

    UserManagement --> CartManagement
    ProductManagement --> CartManagement
    CartManagement --> OrderManagement
    UserManagement --> OrderManagement
    OrderManagement --> PaymentManagement
    PaymentManagement --> OrderManagement
```


<h3>🔗 3. Quan hệ phụ thuộc (Dependency)</h3>
<ul>
    <li>Order Management → User Management: để lấy thông tin khách hàng.</li>
    <li>Order Management → Product Management: để lấy dữ liệu sản phẩm khi tạo đơn.</li>
    <li>Cart Management → Product Management: để hiển thị thông tin sản phẩm trong giỏ.</li>
    <li>Payment Management → Order Management: để thanh toán cho đơn hàng đã tạo.</li>
    <li>Payment Management → User Management: để xác thực tài khoản người thanh toán.</li>
</ul>

<h3> 4. Lý do phân chia gói</h3>
<ul>
    <li>Tăng khả năng mở rộng (Scalability): Có thể phát triển từng module độc lập.</li>
    <li>Dễ bảo trì (Maintainability): Khi thay đổi logic thanh toán, không ảnh hưởng module khác.</li>
    <li>Tái sử dụng (Reusability): Mỗi package có thể được dùng trong hệ thống tương tự (ví dụ: User Management có thể dùng lại cho hệ thống khác).</li>
    <li>Phân tầng hợp lý (Layer separation): Gắn kết theo chức năng, giảm phụ thuộc chéo.</li>
</ul>



<h1>Ex10: </h1>

```mermaid
flowchart TB

subgraph Presentation_Layer[" Presentation Layer (Tầng giao diện)"]
    A1["Student UI"]
    A2["Lecturer UI"]
    A3["Admin UI"]
end

subgraph Business_Layer["️ Business Logic Layer (Tầng xử lý nghiệp vụ)"]
    B1["Student Management Module"]
    B2["Lecturer Management Module"]
    B3["Course Management Module"]
    B4["Schedule Management Module"]
    B5["Grade Management Module"]
end

subgraph Data_Access_Layer[" Data Access Layer (Tầng truy cập dữ liệu)"]
    C1["StudentDAO"]
    C2["LecturerDAO"]
    C3["CourseDAO"]
    C4["ScheduleDAO"]
    C5["GradeDAO"]
    DB["Database"]
end

%% Dependencies
A1 --> B1
A2 --> B2
A3 --> B3
B1 --> C1
B2 --> C2
B3 --> C3
B4 --> C4
B5 --> C5
C1 --> DB
C2 --> DB
C3 --> DB
C4 --> DB
C5 --> DB

```

```mermaid
    classDiagram
    class SinhVien {
        - String maSV
        - String hoTen
        - String email
        - String lop
        + dangKyMonHoc(MonHoc)
        + xemLichHoc()
        + xemDiem()
    }

    class GiangVien {
        - String maGV
        - String hoTen
        - String email
        - String boMon
        + taoLichHoc()
        + chamDiem(SinhVien, MonHoc, double)
    }

    class MonHoc {
        - String maMon
        - String tenMon
        - int soTinChi
        - String lichHoc
        + capNhatDiem(SinhVien, double)
        + hienThiThongTin()
    }

    SinhVien --> MonHoc : "đăng ký"
    GiangVien --> MonHoc : "giảng dạy"
```










