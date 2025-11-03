<h1>Ex1: Chụp và phân tích UI thực tế</h1>
<img width="1508" height="706" alt="image" src="https://github.com/user-attachments/assets/6aff5ae8-3009-4d4f-9302-976c4ba6f654" />
<img width="1512" height="756" alt="Screenshot 2025-11-03 at 14 30 41" src="https://github.com/user-attachments/assets/5cbfb73e-f876-44a9-89ec-805d11a95204" />


<h3>Đề Xuất Cải tiến</h3>

<table>
  <tr>
    <th>Mục</th>
    <th>Nội Dung Y/c</th>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
 <tr>
    <td>Nhận xét tổng quan</td>
    <td>Giao Diện tổng thể hiện thị đầy đủ thông tin, nhưng dối mắt, thiếu sự thống nhất về màu sắc, và khó tập chung vào nội dung chính. Các nút chức năng có màu quá chói, không theo hệ thống màu chủ đạo.
</td>
  </tr>
 <tr>
    <td>Phân tích lỗi UI/UX</td>
    <td>Màu sắc: Nhiều nút với lệch tông -> mất về mặt nhất quán thương hiệu;  Bố cục: Các khối “Thông tin lớp học”, “Giảng viên”, “Học viên” đặt sát nhau, thiếu khoảng trắng. - Typography: Tiêu đề và nội dung có cỡ chữ gần nhau, không tạo được phân cấp thị giác. - Icon: Các nút hành động không có chú thích (tooltip), khó hiểu với người mới. - Hành vi UX: Các nút “Thêm học viên” và “Chuyển lớp” đặt xa nhau, không cùng nhóm chức năng.

</td>
  </tr>
 <tr>
    <td>Nguyên nhân tiềm ẩn</td>
    <td>Thiết kế không tuân theo Design System chuẩn. - Mỗi module được phát triển riêng nên không đồng bộ UI. - Không có UX review trước khi phát hành giao diện.
</td>
  </tr>
 <tr>
    <td>Đề xuất cải tiến</td>
    <td>Chuẩn hóa màu sắc: Dùng tối đa 3 màu chính (Primary, Secondary, Danger). - Tăng khoảng trắng: Thêm padding giữa các section để dễ đọc hơn. - Cải thiện phân cấp chữ: Tiêu đề 20–24px, nội dung 14–16px. - Nhóm nút chức năng hợp lý: Gom “Thêm học viên” và “Chuyển lớp” vào một thanh công cụ. - Thêm tooltip cho icon: Hiển thị mô tả khi di chuột. - Responsive Design: Tối ưu hiển thị bảng học viên trên thiết bị nhỏ bằng dạng thẻ (card layout).
</td>
  </tr>
   <tr>
    <td>UI sau cải tiến (mô tả)
</td>
    <td>Ví dụ layout: `Tên lớp: HN-KS24-CNTT1
</td>
  </tr>
</table>
