<h1>Ex1: Quản Lý thư viện</h1>
<table>
  <tbody>
		<tr>
      <th>Role (Vai trò)</th>
      <th>Stakeholder (Bên liên quan)</th>
      <th>Description / Responsibility (Mô tả / Trách nhiệm)</th>
    </tr>
    <tr>
      <td rowspan="2">End User (Người dùng cuối)</td>
      <td>Độc giả / Thành viên thư viện</td>
      <td>Sử dụng hệ thống để tìm kiếm, mượn/trả sách, gia hạn, đặt chỗ, truy cập tài nguyên số.</td>
    </tr>
    <tr>
      <td>Thủ thư (Librarian)</td>
      <td>Quản lý kho sách, biên mục, hỗ trợ độc giả, xử lý mượn–trả, phạt trễ hạn, báo cáo.</td>
    </tr>
    <tr>
      <td rowspan="2">Sponsor (Nhà tài trợ / Quản lý)</td>
      <td>Ban quản lý thư viện / Trường học</td>
      <td>Cấp kinh phí, đặt mục tiêu, phê duyệt kế hoạch và giám sát triển khai hệ thống.</td>
    </tr>
    <tr>
      <td>Cơ quan nhà nước / Tổ chức giáo dục</td>
      <td>Ban hành quy định, tiêu chuẩn; có thể tài trợ đề án chuyển đổi số thư viện.</td>
    </tr>
    <tr>
      <td rowspan="2">Professional Expert (Chuyên gia nghiệp vụ)</td>
      <td>Chuyên gia Thông tin – Thư viện học</td>
      <td>Tư vấn điều hành, luồng nghiệp vụ, chính sách lưu thông.</td>
    </tr>
    <tr>
      <td>UX/UI Designer / Nhà phân tích dữ liệu</td>
      <td>Thiết kế giao diện dễ dùng, phân tích hành vi và thống kê mượn/trả để tối ưu trải nghiệm.</td>
    </tr>
    <tr>
      <td rowspan="2">Technical Department (Bộ phận kỹ thuật)</td>
      <td>Nhóm phát triển phần mềm</td>
      <td>Phân tích – thiết kế – phát triển – kiểm thử – triển khai và bảo trì phần mềm LMS.</td>
    </tr>
    <tr>
      <td>Quản trị hệ thống / IT Support</td>
      <td>Quản lý máy chủ, CSDL, sao lưu/khôi phục, cấp quyền, bảo mật và giám sát vận hành.</td>
    </tr>
    <tr>
      <td rowspan="2">Third Party (Bên thứ ba)</td>
      <td>Nhà cung cấp sách / Nhà xuất bản</td>
      <td>Cung cấp dữ liệu biên mục, metadata, dịch vụ tích hợp mua sắm và cập nhật kho.</td>
    </tr>
    <tr>
      <td>Dịch vụ hạ tầng đám mây / Tích hợp bên ngoài</td>
      <td>Hosting (AWS/Azure/GCP), CDN, xác thực liên kết (SSO), cổng thanh toán, công cụ chống đạo văn.</td>
    </tr>
  </tbody>
</table>


<h1>Ex2: Hệ Thống App Ngân Hàng</h1>
<h3>Yêu cầu chứng năng ( function requirement )</h2>
<li>Chức năng đăng Nhập hệ thống tài khoản mật khẩu</li>
<li>Chức năng chuyển tiền giưa các tài Khoản</li>
<li>Chức năng Xem lịch sử giao dịch, xem chi tiết, sao ke ...</li>
<h3>Phi chứng năng ( non - function requirement )</h2>
<li>Hiệu năng hệ thống ( chịu tải được cùng lúc nhiều user )</li>
<li>Bảo mật dữ liệu người dùng ...</li>
<li>Khả năng mở rộng khi hệ thống có nhiều user ..</li>

<h1>Ex3:các yếu tố thuộc môi trường hệ thống App Ngân hàng </h1>
<h3>1.User:</h3>
<li><strong>Khách hàng</strong> : có thể xem số dư, chuyển khoản, thanh toán hoá đơn, sử dụng các tiện ích trong app</li>
<li><strong>Nhân Viên</strong>: Hỗ trợ khách hàng, xử lý tra soát, duyệt giao dịch</li>
<li><strong>Quản trị Hệ thống (admin):</strong> Giám sát hoạt động, bảo trí, cập nhập hệ thống</li>


<h3>2.Phần Cứng</h3>
<li><strong>Thiết Bị Người dùng: </strong> Điện thoại, máy tính bảng, laptop</li>
<li><strong>Server:</strong> Lưu trữ cơ sở dữ liệu, sử lý giao dịch, bảo mật</li>
<li><strong>thiết bị mạng</strong> Router, wifi ...</li>
<li><strong>Máy ATM:</strong> kết nối với hệ thống ngân hàng</li>


<h3>3.Phần mền</h3>

<li><strong>Phần mềm hỗ trợ: </strong> Hệ điều hành, android, ios, window ...</li>

<li><strong>Nền Tảng phát triển:</strong> Java, kotlin, React ...</li>
<li><strong>CSDL:</strong> My SQL</li>
<li><strong>Phần mền bảo mật:</strong>Smart OTP ...</li>


<h3>4.Hệ thống bên ngoài</h3>
<li><strong>Napas: </strong> Sử lý chuyển tiền 24/7</li>
<li><strong>Ví Điện tử: </strong>Kết nối tới ví như OMO zalaPay...</li>
<li><strong>Cơ Quan Nhà nước:</strong> Giám sát điều hành, cấp phép ...</li>

<h3>5. Quy trình hệ thống</h3>
<li><strong>Đăng Nhập Xác thực OTP</strong></li>
<li><strong>Giao dịch tài chính</strong></li>
<li><strong>Quản lý thẻ</strong></li>
<li><strong>Mở tài khoản tiến kiệm online</strong></li>
<li><strong>Báo cáo đối soát dịch vụ ..v.v.m.m</strong></li>

<h3>6. Luật lệ và quy định</h3>
<li>luật các tổ chức tín dụng Việt Nam </li>
<li>Quy định nhà nước</li>
<li>Luật an toàn thông tin</li>
<li>Chính sách nội bộ</li>
<li>...</li>


<h1>Ex4: Cấu trúc tài liệu SRS - Hệ thống Học trực tuyến</h1>

<table>
	<tr>
		<th>STT</th>
		<th>Tên Phần</th>
		<th>Giải thích</th>
	</tr>
	<tr>
		<td>1</td>
		<td>Giới thiệu</td>
		<td>Trình bày mục tiêu, phạm vi hệ thống, và người sử dụng hướng tới (sinh viên, Giáo viện ..)</td>
	</tr>
	<tr>
		<td>2</td>
		<td>Mô tả tổng quan hệ thống</td>
		<td>Cung cấp cái nhìn tổng thể: môi trường hoạt động, chức năng chính</td>
	</tr>
	<tr>
		<td>3</td>
		<td>Yêu cầu chứng năng</td>
		<td>Liệt kê chi tiết các chức năng mà hệ thống cần có (VD: đăng nhập, quản lý khoá học ..v.v.m.m)</td>
	</tr>
	<tr>
		<td>4</td>
		<td>Yêu Cầu phi chứng năng</td>
		<td>Nêu các yêu cầu về hiệu suất, bảo mật, giao diện, tính ổn định, khả năng mở rộng phát triển</td>
	</tr>
	<tr>
		<td>5</td>
		<td>Mô Hình và sơ đồ hệ thống</td>
		<td>Minh Hoạ hoạt động của hệ thống bằng sơ đồ Use case, sơ lớp ....</td>
	</tr>
	<tr>
		<td>6</td>
		<td>Giao diện người dùng</td>
		<td>Mô tả Giao diện: trang Đăng Nhập, trang Khoá Học Trang Bài Giải và bảng điểm</td>
	</tr>
	<tr>
		<td>7</td>
		<td>Yêu Cầu về phần cứng và mền</td>
		<td>Máy chủ, hệ điều hành, cơ sở dữ liệu, môi trường cài đặt .. </td>
	</tr>
	<tr>
		<td>8</td>
		<td>Giới hạn và ràng buộ</td>
		<td>Ngân sách, thời gian phát triển, chính sách, quy định Giáo dục</td>
	</tr>
</table>


<h1>Ex5: So sánh các kỹ thuật phỏng vấn, quan sát, khảo sát, phân tích tài liệu</h1>


<table>
	<tr>
		<th>tên loại</th>
		<th>Ưu Điểm</th>
		<th>Nhượng điểm</th>
		<th>Nào Khi lên dùng</th>
		<th>Tình Huống</th>
	</tr>
	<tr>
		<td>Phỏng Vấn</td>
		<td>Khai thác được thông tin chi tiết, giải quyết đc các vấn đề khúc mắc, phức tạp chưa rõ ràng</td>
		<td>Rât tốn time khì có nhiều stakeholder trong dự án, Maybe khó tiếp nhận thông tin trong vài trường hợp khi phỏng vấn</td>
		<td>Khi thắng mắc về 1 vấn đề điều hành trong dự án, mà người có liên quan nghiệp vụ có thể giải đáp ( Như quy trinh cho mượn sách, quy trình vay vốn ...) </td>
		<td>VD: Trong tình huống dự án chưa hiểu rõ quy trình gia hạn sách, qua bao lâu sẽ bị phạt, khi đó người phụ trách sẽ phải sắp xếp để gặp sinh viện người điều hành thư viện để làm rõ và ptr </td>
	</tr>
	<tr>
		<td>Quan Sát</td>
		<td>Thu Thập thông tin chính sác, thực tế, hiệu rõ không gian, bối cảnh củ dự án => hiểu rõ phần nào về quy trình làm vc</td>
		<td>Rất tốn Time khi và tiền trong  dự án phức tạp cần quan sát lâu dài, Kó áp dụng cho dự án có quy mô lớn, Khó tổng hợp và phân tích</td>
		<td>Khi quy mô dư án nhỏ, khả thi cho việc quan sát để lấy thông tin, quy trình dễ ràng ....</td>
		<td>VD: Trong dự án quản lý thư viện, nhóm phát triển có thể quan sát, các bược điều hành như mượn và trả sách, sử lý trường họp quá hạn... </td>
	</tr>
	<tr>
		<td>Khảo Sát</td>
		<td>Chi phí thấp, Lấy đc lượng lớn thông tin nhanh tróng từ đó giúp phân tính được như cầu sử dụng thói quen ....</td>
		<td>Thông tin chưa được chi tiết, Câu trả lời chủ quan... </td>
		<td>Khi cần thu thập tin trong thời gian ngắn và vẫn đáp ứng về số lượng</td>
		<td>VD: Rikkei muốn khảo sát sinh viên hàng tháng ....</td>
	</tr>
	<tr>
		<td>Phân tính tài liệu</td>
		<td>Giúp hiểu sâu về dự án, phát triển sâu về một lĩnh vực ...</td>
		<td>Tốn thời gian và nhân lực đòi hỏi nhân lực có trình độ cao</td>
		<td>Khi dự án phát triên cần thông tin chính xác tuyệt đối</td>
		<td>VD: Mô hình phần tích chuẩn đoán bệnh , khí dó nhóm phát triển cần phải nghiên cứu tài liệu chuyên sâu....</td>
	</tr>
</table>








