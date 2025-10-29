<h1>Ex 1: Liệt kê và mô tả vai trò từng thành phần</h1>

<table>
    <tr>
        <th>Thành Phân</th>
        <th>Tên</th>
        <th>Vai Trò/Chức năng</th>
        <th>Kí hiệu</th>
    </tr>
    <tr>
         <td>Actor</td>
         <td>Khách Hàng</td>
         <td>Là người bên ngooài hệ thống, Khởi tạo và tương tác. Gửi Y/c "đăng Nhập", "thanh toán", "đặt hàng"</td>
         <td>Đc biểu diễn bởi hình người que</td>
    </tr>
    <tr>
         <td>Object</td>
         <td>Website</td>
         <td>Là thành phần nội bộ hệ thống, chịu trách nhiệm xử lý yêu cầu từ actor. Nhận Y/c hiện thị giao diện, gửi dữ liệu đến hệ thống</td>
         <td>Biểu diễn bằng hình chữ nhât</td>
    </tr>
    <tr>
         <td>Object</td>
         <td>Hệ thống thanh toán</td>
         <td>Là thành phần tham gia xử lý nghiệp vụ, thực hiện xác minh và phản hồi Kết quả thanh toán/td>
         <td></td>
    </tr>
    <tr>
         <td>LifeLine</td>
         <td>lifeline của từng Actor, Object</td>
         <td>Thể hiện thời gian tồn tại và tương tác của mỗi thành phần trong quá tình thực thi mỗi Message đc vẽ giữa các lifeline</td>
         <td>là đường thẳng dọc xuống dưới, kéo dài suất, TG, diễn ra tương tác</td>
    </tr>
</table>


<h1>Ex: 2 Nhận diện các loại thông điệp: synchronous, asynchronous, return.</h1>

```mermaid
    sequenceDiagram
        autonumber
        actor Customer
        participant Website
        participant PaymentSystem as "Hệ thống thanh toán"
        
        
        Customer ->> Website: nhập thông tin
        Website ->> PaymentSystem: Gửi yêu cầu xác minh tài khoản (Synchronous)
        PaymentSystem -->> Website: Trả kết quả xác minh (Return)
        Website -->> Customer: Hiển thị giao diện cá nhân hoặc thông báo lỗi (Return)
        
```

<h1>Ex 3: Hệ thống kiểm tra điều kiện. Nếu hợp lệ, ghi nhận đăng ký</h1>





```mermaid
    sequenceDiagram
    autonumber
    actor Customer as "Sinh Vien"
    participant System as "He thong"
    participant CSDL as "co So Du lieu"
    
    Customer ->> System : Gửi Y/c Đk Môn học
    System ->> CSDL: Kiem Tra ĐK ĐK
    CSDL -->> System: Ket qua kiem tra ĐK
    alt Hop le
        System ->> CSDL: Ghi Nhan DK thanh cong
        CSDL -->> System: Luu thanh cong
        System ->> Customer: Thong bao sinh vien
    else khong hop le
        System ->> Customer: Thong bao sinh vien  That bai
    end    
```


<h1>Ex 4: Người dùng thêm nhiều sản phẩm vào giỏ hàng</h1>


```mermaid
    sequenceDiagram
    autonumber
    actor Customer as "Khach Hang"
    participant System as "he thong dat hang"
    participant CSDL as "Co so Du lieu"
    participant Cart as "gio Hang"
  
    
    
    loop Lăp lại cho mỗi sảm phậm đc chọn
        Customer ->> System: Chọn SP
        System ->> CSDL: Kiểm tra tồn kho sản phẩm
        CSDL -->> System: Trả kết quả kiểm tra


        alt Con Hang 
            System ->> Cart : Nhận SP
            System -->> Customer: thong Bao them thanh cong
        else Het hang
            System  -->> Customer: Thong Bao het hang
        end
    end
        
```        

<h1>Ex 5: Dùng cấu trúc điều kiện trong Sequence.</h1>


```mermaid
    sequenceDiagram
    autonumber
    actor Customer as "Nguời dùng hệ thống"
    participant System as "He thong"
    participant Payment as "He thon thanh toan"
    Note over Customer, Payment: Chọn Phương thức thanh toán
    alt VNPay
        Customer ->> Payment: thanh toan
        alt Thanh toan Thành công + Xác Nhận đơn
            Payment -->> System:  thanh toán thành công
            System -->> Customer: thông báo thanh toán thành công
            System -->> Customer: Xác Nhận Đơn
        else Thanh toán thất bại
            Payment -->> System: thanh toán Thất bại
            System -->> Customer: thông báo thanh toán Thất bại
        end
    else COD + Xác Nhận Đơn
        System -->> Customer: Xác Nhận Đơn
    end
```




<h1>Ex 6: phân tích: Tài khoản người dùng.</h1>

```mermaid
    stateDiagram-v2
        [*] --> createAccount: Tạo Tài Khoản
        createAccount --> Active: "Kích Hoạt Tài Khoản"
        Active --> LookAccount : "Khoá Tài Khoản"
        LookAccount --> ActiveAgain: "Kích hoạt lại"
        ActiveAgain --> Active: Duyêt Kích Hoạt
        Active -->[*]: Xoá tài Khoản
```


<h1>Ex 7: phân tích:Đơn hàng online.</h1>

```mermaid
     stateDiagram-v2
     [*] --> createOder: Create new order
     createOder --> WaitingForPayment: Waiting
     WaitingForPayment --> delivering:  Success
     WaitingForPayment --> Cancel: failed
     delivering --> Cancel: Delivery Failed
     delivering --> Success: Success
     Success --> [*]
     Cancel --> [*]

```

<h1>Ex 8: phân tích: Sản phẩm</h1>

```mermaid
    stateDiagram-v2
        [*] --> WaitingForImport: Chờ nhập Hàng
    WaitingForImport --> InStock: Còn Hàng
    WaitingForImport --> SoldOut: Hêt Hàng
    InStock --> SoldOut: Bán Hêt Hàng
    SoldOut --> WaitingForImport: Nhập hàng mới
    InStock --> StopSelling: Quyết Định Ngừng bán
    SoldOut --> StopSelling: Ngừng bán
    StopSelling --> [*]

```


<h1>Ex 9: phân tích: Tài khoản người dùng.</h1>


```mermaid
    sequenceDiagram
        autonumber
        actor C as Customer
        participant viewProduct as ViewProduct
        participant addToCart as AddToCart
        participant order as Order
        participant payment as Payment
        participant EmailService as EmailService
        
        Note over viewProduct, order: (1) createOrder
        C ->> viewProduct: ViewProduct
        C ->> addToCart: Customer add product to cart
        C->> order: Customer Ordered
        alt: Card with at least 1 product
        order ->> payment: Paying
        alt: Success
        order ->> EmailService: SendEmail "Payment success"
        order -->> C: notice to customers on System  "Payment success"
        else: Failed
            order ->> EmailService: SendEmail "Payment Failed"
            order -->> C: notice to customers on System  "Payment Failed"
        end    
        
        
        else: without product in cart
            order -->> C: notice to customers on System "without product"
        end    
```                

<h1>Ex 10: phân tích: Hệ thống nộp bài tập.</h1>

```mermaid
    sequenceDiagram
        autonumber
        actor C as Student
        participant System as SystemElearning
     
        participant Teacher as Teacher
        participant DB as Database
        
        
        C ->> System: Login 
        System ->> DB: get Data Assignments
        DB -->> System: return Database
        C ->> System: SubmitAssignments
        System ->> DB: Submit and save to database
        DB -->> System: notice "Success"
        System -->> C:  notice "Success"
        
        Teacher ->> System: open list students
        System ->> DB: get Data Assignments
        DB -->> System: return Database
        Teacher ->>System: scoring
        System ->> DB: Update scored
        DB -->> System: return result
        System -->> Teacher: notice Success
        
        
    
```

```mermaid
      stateDiagram-v2
          [*] --> CDSL: Lấy Dữ liệu sinh viên
          CDSL --> ChuaNop : SV chưa nộp bài
          CDSL --> DaNop: đã Nộp bài
          DaNop --> ChamDiem : chấm điểm
          ChuaNop -->  [*]
          ChamDiem --> [*]
          
          
```

<h3>Logic tổng thể</h3>
<ul>
    <li>1. Hệ thống lấy thông tin bài tập từ CSDL hiện thị cho SV<</li>
    <li>2. Sinh viên có thể chọn bài tập và nộp bài và lưu và CSDL</li>
    <li>3. Giảng viên đăng nhập vào hệ thông, có thể xem bài tập và chấm điểm, hệ thông cập nhập và lưu điển</li>
</ul>

<h3> Mapping giữa Sequence Diagram và State Diagram </h3>
<table>
  <tr>
    <th>Sequence Step</th>
    <th>Sự kiện (Trigger)</th>
    <th>Trạng thái bị ảnh hưởng trong State Diagram</th>
  </tr>
  <tr>
    <td>(1–4) Sinh viên mở giao diện nộp</td>
    <td>Hiển thị bài tập</td>
    <td>Bắt đầu ở Chưa nộp (ChuaNop)</td>
  </tr>
  <tr>
    <td>(5–8) Sinh viên tải bài lên và lưu thành công</td>
    <td>Upload thành công</td>
    <td>Chuyển sang Đã nộp (DaNop)</td>
  </tr>
  <tr>
    <td>(9–12) Giảng viên mở và chấm bài</td>
    <td>Bắt đầu chấm</td>
    <td>Trạng thái Đã nộp → Chấm điểm (ChamDiem)</td>
  </tr>
  <tr>
    <td>Sau khi chấm xong</td>
    <td>Lưu điểm</td>
    <td>Chấm điểm → Đã chấm (DaCham)</td>
  </tr>
  <tr>
    <td>Kết thúc quy trình</td>
    <td>Hoàn tất</td>
    <td>Trạng thái cuối cùng [ * ]</td>
  </tr>
</table>



<h1>Ex: BTTH Phân Tích Hành Vi với Sequence & State Diagram </h1>

```mermaid
    sequenceDiagram
    autonumber
    actor C as Customer
    participant W as App
    participant I as Inventory
    participant P as Payment
    participant S as Shipping
    participant E as EmailSvc
    
    
    Note over C,W: (1) Create order 
    C ->> W: Create Oder
    W ->> I: CheckStockCart
    I -->> W: StockStatus( true )
    alt Stock OK
        W -->> C: showOrder + ProceedToPay $$
        Note over C,P: (2) Payment
        C->>P: Pay(orderId, amount, method)
        P-->>W: PaymentCallback(orderId, SUCCESS | FAIL)
        alt Payment SUCCESS
        W ->> E: SendEmailOrder
        W ->> S: CreateShipment(orderID, address)
        S --> W: ShipmentAccepted(trackingId)
        W --> C: Show (Payment Failed + retry option)
        else Payment Failed
        W ->> E: SendEmail(payment Failed, Error)
        W --> C: Show "Payment failed" + Retry Option
        opt Customer cancles
        C->>W: CancelOrder(orderId)
        W ->> E: SendEmail(orderID, "Cancelled")
        end
            
        end
            
    else shoutOut
    
    W ->> S: Show " Out of stock" Alternatives
    W ->> E: SendEmail(orderId, Cancelled)
    end
    
    Note over W,S:  (3) delivery
    
    S -->> W: ShipmentStatus(orderId, IN_TRANSIT)
    W -->> C: Notify "InDelivery" 
    
    S -->> W: ShipmentStatus(orderId, Delivered)
    W ->> E: SendEmail(OrderId, Completed )
    W -->> C: Show Delivered

```
