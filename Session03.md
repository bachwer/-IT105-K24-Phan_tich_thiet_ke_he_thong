## Session 03: Use Case Diagram minh hoạ

<h1>Ex 1 + 2</h1>
Mô tả:<br>
- << include >> Quan hệ bao hàm, chỉ ra rằng Use Case chính gọi đến phụ <br>
Use Case chính là "xem chi tiết phim" và "đặt hàng" của 2 use case dưới<br>
Khi user chọn Case chính thì có thể thực hiện thêm các bước ở case phụ
  
```mermaid
flowchart TD
    A1["👤User (Ex 1)"] --> B1((Xem chi tiết phim))
    B1 -.->|<<include>>| C1((Xem trailer))
    B1 -.->|<<include>>| D1((Xem bình luận))

    A2["👤User (Ex 2)"] --> B2((Đặt Hàng))
    B2 -.->|<<include>>| C2((Kiểm Tra Giỏ Hàng))
    B2 -.->|<<include>>| D2((tính Phí vận Chuyển))

```


<h1>Ex 3: Xác định mối quan hệ giữa các Use Case (association, include hay extend)</h1>
<ul>
   <li>inlcude : Nghĩa là chức năng phụ bắt buộc được thực hiện mỗi khi chức năng chính chạy.</li>
   <li>Association:  User có liên kết trực tiếp (association) với chức năng chính</li>
   <li>extend: Nghĩa là chức năng phụ không bắt buộc, chỉ mở rộng hành vi chính.</li>
</ul>
<table>
  <tr>
     <th>Use Case A</th>
     <th>Use Case B</th>
     <th>Mối quan hệ</th>
     <th>Giải thích</th>
  </tr>
  <tr>
    <td>Đặt Hàng</td>
    <td>Kiểm tra giỏ hàng</td>
    <td>include</td>
    <td>Vì trước khi đặt hàng, user phải kiểm tra giỏ hàng ( xem số lượng, chẹc lại đơn ) do đó KT giỏ hàng là bước bắt buộc bao hàm trong đặt hàng</td>
  </tr>
  <tr>
    <td>Đặt Hàng</td>
    <td>Đề xuất Hoá đơn</td>
    <td>inlcude</td>
    <td>Sau khi đặt hàng hệ thống luôn tạo/ đề xuất hoá đơn, để user xác nhận thanh toán, và đây là hành vi luôn xảy ra khi đặt hàng</td>
  </tr>
   <tr>
    <td>Đặt hàng</td>
    <td>Xem đánh giá</td>
    <td>extend</td>
    <td>Bởi vì đây là hành vi mở rộng, ko bắt buộc, người dùng có thêm trước và sau khi đặt hàng</td>
  </tr>
   <tr>
    <td>Kiểm tra giỏ hàng</td>
    <td>User</td>
    <td>asociation</td>
    <td>User có thể truy cập trực tiếp vào giỏ hàng bất cứ lúc nào, mối quan hệ giữa Actor và Use Case</td>
  </tr>
   <tr>
    <td>Đặt Hàng</td>
    <td>User</td>
    <td>asociation</td>
    <td>User thực hiện hành vi đặt hàng, mối quan hệ giữa Actor và Use Case</td>
  </tr>
   <tr>
    <td>Xem Đánh giá</td>
    <td>User</td>
    <td>asociation</td>
    <td>User thực hiện hành vi Xem, mối quan hệ giữa Actor và Use Case</td>
  </tr>
</table>


<h1>Ex 4: Vẽ Use Case Diagram Hệ thống quản lý thư viện</h1>

```mermaid
flowchart TD
    %% === ACTORS ===
    A1[👤 Nhân viên thư viện]
    A2[👤 Độc giả]

    %% === USE CASES ===
    B1((Đăng nhập))
    B2((Tìm sách))
    B3((Mượn sách))
    B4((Trả sách))

    %% === RELATIONS ===
    %% Association
    A1 --> B1
    A2 --> B1
    A2 --> B2
    A2 --> B3
    A2 --> B4

    %% Include
    B3 -.->|<<include>>| B2
    B4 -.->|<<include>>| B1

```


<h1>Ex 5: Phân loại Actor theo vai trò (primary, secondary) </h1>
<p>Mô tả: Cho tình huống: Xây dựng app giao đồ ăn online</p>
<table>
  <tr>
     <th>Actor</th>
     <th>Loại</th>
     <th>User Case</th>
  </tr>
  <tr>
    <td>Cusomter</td>
    <td>Primary</td>
    <td>Tương tác: đặt hàng, xem đánh giá, tìm món, thanh toán đơn hàng ... </td>
  </tr>
   <tr>
    <td>Driver</td>
    <td>Secondary</td>
    <td>Nhận đơn, giao hàng, hoành thành, xem đánh giá dịch vụ</td>
  </tr>
   <tr>
    <td>Saller</td>
    <td>Primary</td>
    <td>nhận đợn từ khách hàng, xác nhận, hoành thành, xem đánh giá dịch vụ</td>
  </tr>
   <tr>
    <td>Admin</td>
    <td>Secondary</td>
    <td>Quản lý người dùng: tài xế, khách hàng, chủ cửa hàng, xem thống kê doanh thu ...</td>
  </tr>
</table>


<h1>Ex 6: Diễn đạt Use Case Description đầy đủ Đặt hàng </h1>
  <ul>
    <li><strong>Tên: </strong>Đặt Hàng</li>
    <li><strong>Actor: </strong>Khách Hàng</li>
    <li><strong>Mục Tiêu: </strong>Khác Hàng thực hiện chọn món xác nhận thông tin để hê thông ghi nhận dữ liệu và xác nhận đặt hàng</li>
    <li><strong>Luồng Chính: </strong>Khách hàng -> đăng nhập -> tìm kiếm & chọn món -> mở giỏ hàng -> tiến hành đặt hàng -> hệ thống xác nhận & tạo đơn -> hiện thị thông báo đặt hàng thành công</li>
    <li><strong>Luồng Lỗi: </strong>Hệ thống thông báo chưa chọn món, Y/c Nhập đầy đủ thông tin ( STĐ ,đia chỉ, ...), Thanh toán thất bại, cưa hàng đóng cửa || dừng hoạt động, lỗi hệ thống ..</li>
    
  </ul>


<h1>Ex 7: Vẽ sơ đồ Use Case có include, extend, ghi rõ Actor - Use Case </h1>


```mermaid
flowchart TD
    %% === ACTORS ===
    A1[👤 Khách Hàng]
    A2[👤 Tài Xế]
    A3[👤 Hê thống thanh Toán]


   %% === Use Case === Đặt xe, Xem vị trí tài xế, Thanh toán, Nhận khuyến mãi
   B1((Đặt xe))
   B2((Xem vị trí tài xế))
   B3((Thanh Toán))
   B4((Nhận Khuyến mãi))
     
  
   %% === Relations ===
    A1 --> B1
    A1 --> B4
    B1 -.-> |<<include>>| B2
    B1 -.-> |<<include>>| B3
    A3 --> B3
    A2 --> B2

```

<h1>Ex 8:  Use Case Diagram cho app shoope </h1>

```mermaid
flowchart TD
    %% === ACTORS ===
    A1[ Người mua]
    A2[Người bán]
    A3[Hệ thống thanh toán]


    %% === USE CASES ===
    B1((Đăng nhập))
    B2((Tìm kiếm & Xem sản phẩm))
    B3((Đặt hàng))
    B4((Thanh toán đơn hàng))
    B5((Quản lý đơn hàng))

    %% === RELATIONS ===

    A1 --> B1
    
    A2 --> B1
  
    A3 --> B4

    %% Bao gồm đăng nhập cho tất cả
    B2 -.->|<<include>> role Khách hàng| B1
    B3 -.->|<<include>> role Khách hàng| B1
    B5 -.->|<<include>> role Người bán| B1

    
    B3 -.->|<<include>>| B4
```


<h1>Ex 9:   Hệ thống đăng ký môn học  </h1>

```mermaid
flowchart TD
    %% === ACTORS ===
    A[ User]

    B1((Đăng Nhập))
    B2((Đăng Kí Môn Học))
    B3((Kiểm tra lịch Học))
    B4((Xem môn học trùng))
    B5((Xác nhận đăng kí))



    A --> B1


    B1 -.->|<<include>>| B2
    B1 -.->|<<include>>| B3

    B2 -.->|<<include>>| B5
    B3 -.->|<<extend>>| B4

```


<h1>Ex 10:   hệ thống quản lý đào tạo online  </h1>

```mermaid
flowchart TD
    %% === ACTORS ===
    A1[ Học Viên]
    A2[ Giảng Viên]
    A3[ Quản Trị Viên]

    %% === USE CASES HỌC VIÊN ===
    B1((Đăng ký học))
    B2((Học online))
    B3((Xem khóa học))
    B4((Làm bài kiểm tra))
    B5((Xem điểm))
    B6((Làm đơn xin nghỉ))
    B7((Xem thống kê kết quả học cá nhân))

    %% === USE CASES GIẢNG VIÊN ===
    B8((Xem môn đang dạy))
    B9((Chấm bài))
    B10((Xem thống kê lớp học))

    %% === USE CASES QUẢN TRỊ ===
    B11((Xem đơn học viên))
    B12((Duyệt đơn))
    B13((Thống kê kết quả học toàn khóa))
    B14((Quản lý tài khoản))

    %% === RELATIONS ===
    %% HỌC VIÊN
    A1 --> B1
    A1 --> B3
    A1 --> B2
    A1 --> B4
    A1 --> B5
    A1 --> B6
    A1 --> B7

    %% GIẢNG VIÊN
    A2 --> B8
    A2 --> B9
    A2 --> B10

    %% QUẢN TRỊ
    A3 --> B11
    A3 --> B12
    A3 --> B13
    A3 --> B14

    %% INCLUDE / EXTEND RELATIONSHIPS
    B2 -.-> |<<include>>| B4
    B4 -.-> |<<include>>| B5
    B7 -.-> |<<extend>>| B5
    B11 -.-> |<<include>>| B12
    B10 -.-> |<<extend>>| B9
