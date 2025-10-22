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

<h1>Ex6: hệ thống “Giao hàng nhanh” (FastDelivery)</h1>

<table>
	<tr>
		<th>Stakeholder</th>
		<th>Vai Trò</th>
		<th>Mối Quan Tâm</th>
		<th>Mức độ Ưu tiên</th>
	</tr>
	<tr>
		<td>Customer</td>
		<td>Người sử dụng dịch vụ và nhận hàng</td>
		<td>Tốc độ giao hàng, dịch vụ mang lại, theo dõi đơn hàng</td>
		<td>Critical ( ảnh Hưởng trực tiếp tới sự thành công của hệ thống )</td>
	</tr>
	<tr>
		<td>Tài xế giao hàng</td>
		<td>Thực Hiện nhiệm vụ vận chuyển hàng, giao cho khách hàng</td>
		<td>Ứng dụng của hệ thống, quy trình giao hàng, định vị chính xác chỗ cần giao, hỗ trợ kĩ thuật</td>
		<td>Major</td>
	</tr>
	<tr>
		<td>Công ty quản lý</td>
		<td>chủ sở hữu và điều hành hệ thống</td>
		<td>Lợi nhuận và doanh thu, tính ổn định, phân tính dữ liệu thống kê, uy tín thương hiệu và định hướng ptriển lâu dài</td>
		<td>Critical</td>
	</tr>
	<tr>
		<td>Đối tác bán hàng</td>
		<td>Gửi hàng thông qua hệ thống</td>
		<td>Ứng dụng hệ thống, thời gian lấy hàng, giao hàng,  phí vận chuyển ...</td>
		<td>Major</td>
	</tr>
	<tr>
		<td>Nhóm kĩ thuật IT</td>
		<td>Là người thiết kế, vận hành hệ thống, duy trì vầ bảo trì</td>
		<td>Ổn định hệ thống và hiệu xuất cao, bảo mật dữ liệu, mở rộng vào cập nhập</td>
		<td>Major</td>
	</tr>
	<tr>
		<td>Cơ quan quản lý nhà nước</td>
		<td>Là người giám sát hoạt động hệ thống</td>
		<td>Tính minh bạch, thuế, tuân thủ phá luận nhà nước</td>
		<td>Minor</td>
	</tr>
</table>


<h1>Ex7: Mô tả ngắn một quy trình mua hàng online </h1>
<ol>
  <li>Khách hàng đăng nhập vào hệ thống</li>
  <li>Tìm kiến sản phẩm theo nhu cần</li>
  <li>Tiến hành đặt hàng ( chọn hình thức thanh toán: COD, Ví ĐT, thẻ ....</li>
  <li>Hệ thống gửi thông tin cho người bán cbi hàng</li>
  <li>Người bàn hàng xác nhận và đóng đơn</li>
  <li>Đơn vị vận chuyển đến lấy hàng về kho tổng gần đó ( hoặc Giao luôn tuỳ theo hình thức )</li>
  <li>Giao đến khách hàng</li>
  <li>Khách hàng phản hồi và đánh giá dịch vụ</li>
</ol>

<h3>4 Yêu cầu chứng năng hệ thống</h3>
<ul>
	<li>Đăng Nhập vào hệ thống</li>
	<li>tìm kiếm, lựa chọn sp</li>
	<li>Đặt hàng</li>
	<li>Nhắn tin với người bán</li>
</ul>
<h3>4 Yêu cầu phi chứng năng hệ thống</h3>
<ul>
	<li>Tính bảo mật dữ liêu người dùng</li>
	<li>Chịu tải số lượng lớn User cùng lúc trong thời điểm</li>
	<li>Bảo trì khi có sự cố</li>
	<li>Phát triển và update phần mền </li>
</ul>

<h1>Ex8: Đề cương tài liệu SRS cho hệ thống đặt món ăn tại quán.</h1>
<h3>1. Giới thiệu</h3>
	<ul>
		<li>1.1 Mục Đính</li>
			<p>- Xây Dựng Hệ thống đặt món ăn: Cho phép khách hàng có thêm xem thực đơn, đặt món, thanh toán và theo dỗi trạng thái đơn hàng</p>
		<li>1.2 Phạm Vi</li>
			<p>- Hiện thị thực đơn, đặt món, thanh toán, quản lý đơn hàng, báo cáo doanh thu</p>
		<li>1.3 Tài liệu Kham Khảo</li>
			<p>- Liệt kê các tài liệu, tiêu chuẩn, hoặc hệ thống tương đương tự dùng hoặc kham khảo</p>
	</ul>
<h3>2. Mô Tả hệ thống</h3>	
	<ul>
		<li>2.1 Góc nhìn hệ thống</li>
			<p>- Tổng quan về hệ thống và môi trường hoạt động:</p>
			<p>- Hệ thống là 1 phần của mô hinhg POS hoặc hoạt động độc lập, mô tả qua sơ đồ khối ( quản lý thực đơn - đơn hàng - thanh toán - báo cáo )</p>
		<li>2.2 Chức năng hệ thống</li>
			<p>- Khách Hàng: xem Menu, chọn món, đặt món</p>
			<p>- Nhân viên: xác nhận đơn, cập nhập trạng thái đơn</p>
			<p>- Quản lý: thông kê doanh thu, quản lý món ăn, tài khoản nhân viên ( nếu có )</p>
		<li>2.3 Đặc điểm của người dùng</li>
			<p>- Phân Loại người dùng: khách hàng, nhân viên, quản lý quán, ...</p>	
			<p>- Mỗi nhóm có nhu cầu sử dụng riêng và mức độ truy cập khác nhau</p>
		<li>2.4 Giới hạn</li>
			VD:
			<p>- Ứng dụng hệ thống chỉ hoạt động trong mang nội bộ của quán</p>
			<p>- Cần thiết bị để sử dụng hệ thống ( máy tính, tablet ...)</p>
			<p>- Hệ thông hỗ trợ đa ngôn ngữ (VN / EN) </p>
		<li>2.5 Giải định và phụ thuộc</li>
			<p>- Giả định khách hàng kết nội mạng nội bộ của quán</p>
			<p>- Phụ thuộc vào hệ thống thanh toán ..</p>
	</ul>
<h3>3. Yêu cầu chưng năng</h3>	
	<ul>
		<li>3.1 Quản lý người dùng</li>
			<p>- Đăng Nhập / Đăng Xuất ( cho nhân viên và quản lý )</p>
			<p>- Phân quyền truy cập ( admin, staff, cashier )</p>
		<li>3.2 Quản lý thực đơn</li>
			<p>- Thêm sửa xoá món ăn, giá tiền, hình ảnh</p>
			<p>- Phân loại món ( chính, phụ, tráng miệng, đồ uống.. )</p>
		<li>3.3 Đặt món</li>
			<p>- Chọn menu từ quán</p>
			<p>- Ghi nhận số lượng, Ghi chú món ăn ( ít cay .. )</p>
			<p>- Cập nhập tráng thái đơn hàng</p>
		<li>3.4 Thanh Toán</li>
			<p>- Tính tổng hoá đơn, giảm giá, thuế</p>
			<p>- Chọn Phương thức thành toán</p>
		<li>3.5 Báo cáo vào thông kê</li>
			<p>- Thống kê doang thu theo ngày tháng ..</p>
			<p>- Báo cáo món bán chạy</p>
			<p>- Phân tính thống kê đánh giá món</p>
	</ul>
<h3>4. Yêu cầu Phi chưng năng</h3>	
	<table>
		<tr>
			<th>Loại Yêu Cầu</th>
			<th>Mô tả</th>
		</tr>
		<tr>
			<td>Hiệu Năng</td>
			<td>Hệ thống phản hồi trong thơi gian ngắn <= 2s cho thao tác chọn món</td>
		</tr>
		<tr>
			<td>Bảo mật</td>
			<td>Mã hoá dữ liệu thanh toán, phân quyền chặt chẽ</td>
		</tr>
		<tr>
			<td>Khá năng mở rộng</td>
			<td>Có nhiều thiết bị truy cập đồng thời, tối ưu hiệu xuất</td>
		</tr>
		<tr>
			<td>Giao Diện</td>
			<td>Thân thiệt, dễ sử dụng cho nhiên viên phục vụ</td>
		</tr>
		<tr>
			<td>Độ tin cậy</td>
			<td>Hệ thống hoạt động 24/7 không mất dữ liệu ( backUp thường xuyên )</td>
		</tr>
	</table>
				
<h3>5. Thiết kế giao diện</h3>	
	<ul>
		<li>Phác thảo sơ bộ giao diện: trang menu, đặt món, thanh toán</li>
		<li>Mô tả hành vi người dùng</li>
	</ul>
<h3>6. Mục lục</h3>	
	<ul>
		<li>Sơ đồ ca sử dụng</li>
		<li>Sơ đồ lớp</li>
		<li>Sơ đồ trình tự</li>
		<li>Các biểu mẫu, dữ liệu mẫu</li>
	</ul>
	
	


<h1>Ex9:  BÁO CÁO PHÂN TÍCH HỆ THỐNG – HỆ THỐNG QUẢN LÝ TUYỂN DỤNG (RMS)</h1>
<h3>1. Các yếu tố môi trường</h3>
	<ul>
		<li>1.1 Môi trường người dùng</li>
			<p><strong>Nhà tuyển Dụng:</strong> tạo tin tuyển dụng, quản lý ứng viên, phỏng vấn, lựa trọn</p>
			<p><strong>Ứng Viên:</strong> tạo hồ sơ, nộp đơn ứng tuyển, theo dõi tiến trình, nhận thông báo phản hồi</p>
			<p><strong>Quản trị viên:</strong> quản lý tài khoản, dữ liệu, phân quyền</p>
			<p><strong>Nhà quản lý cấp cao:</strong> xem báo cáo, thông kê dữ liệu, tính hiệu quả của hệ thống</p>
		<li>1.2 Môi trường phân cứng</li>
			<p><strong>Máy chủ:</strong> máy chủ riêng server hoặc các dịch vụ khác ...</p>	
			<p><strong>thiết bị sử dụng:</strong> Điện thoại, máy tính, laptop ...</p>	
		<li>1.3 Môi trường phân mền</li>
			<p><strong>Hệ điều hành :</strong> windows / MacOs/ ios / ...</p>
			<p><strong>Trình duyệt :</strong> Chrome, safari ...</p>
			<p><strong>Công nghệ :</strong> web application + Database ( SQL / PostgreSQL )</p>		
		<li>1.4 Môi trường làm việc</li>
			<ul>
				<li>Tích hợp email API, ZaLo OA để gửi thông báo</li>
				<li>Tuân thủ các quy định bảo mật thông tin các nhân</li>
			</ul>
	</ul>
<h3>2. Phân tính stakeholder</h3>
	<table>
		<tr>
			<th>Nhóm Stakeholder</th>
			<th>Vai trò / Quyền hạn</th>
			<th> Mối quan tâm</th>
			<th>Mức độ ưu tiên</th>
		</tr>
		<tr>
			<td>Ứng Viên</td>
			<td>Tạo hồ sơ, ứng tuyển</td>
			<td>Giao diện dễ sử dụng, bảo mật thông tin ca nhân, </td>
			<td>Critical</td>
		</tr>
		<tr>
			<td>Nhà tuyển Dụng HR</td>
			<td>Quản lý thông tin, chọn lọc hồ sơ, gửi phàn hồi</td>
			<td>Quản lý hiệu quả, tìm ứng viên nhanh tróng</td>
			<td>Critical</td>
		</tr>
		<tr>
			<td>Quàn lý nhận sự</td>
			<td>Theo dõi quy tình tuyển dụng, nộp báo cáo</td>
			<td>Dữ liệu chính xác, dễ tổng hợp thông tin</td>
			<td>Major</td>
		</tr>
		<tr>
			<td>Ban Giám đốc</td>
			<td>Xem tổng quát, tiến trình hiệu quả của hệ thống</td>
			<td>Thông kê dữ liệu, KPI</td>
			<td>Major</td>
		</tr>
		<tr>
			<td>Nhóm Kĩ thuật IT</td>
			<td>Bảo trì, cập nhật, phát triển hệ thống</td>
			<td>Hệ thống ổn định, dữ liệu được bảo mật, dễ mở rộng</td>
			<td>Major</td>
		</tr>
		<tr>
			<td>Cơ Quan quản lý nhà nước</td>
			<td>Giám sát hoạt động, kiểm tra việc tuân thủ luật pháp</td>
			<td>Bảo vệ dữ liệu cá nhân, tính minh bạch hê thống</td>
			<td>Minor</td>
		</tr>
	</table>
	
<h3>3. Các Nguồn yêu cầu</h3>
	<table>
		<tr>
			<th>Nguồn</th>
			<th>Mô tả thông tin thu thập</th>
		</tr>
		<tr>
			<td>Phỏng vấn</td>
			<td>Trao đổi với nhân viên HR để hiểu quy tình tuyển dụng của hệ thống</td>	
		</tr>
		<tr>
			<td>Quan Sát</td>
			<td>Quan sát các sử lý hồ sơ thủ công và các vần đề khó khăn khi sử lý</td>	
		</tr>
		<tr>
			<td>Phân tích tài liệu</td>
			<td>Nghiên cứu quy trình tuyển dụng, (form CV, email, ...) Mẫu</td>	
		</tr>
		<tr>
			<td>Khảo sát</td>
			<td>Thu thập thông tin từ nhiều nguồn, nhận sự, ứng viên</td>	
		</tr>
		<tr>
			<td>Hệ thông cũ</td>
			<td>Đánh giá từ hệ thông cũ và đưa ra hướng phát triện hệ thống mới hiện đại hơn</td>	
		</tr>
	</table>
	
<h3>4. Một số yêu Cầu chức năng & Phi Chức năng</h3>
	<h4>4.1 Yêu cầu chứng năng</h4>
	<ol>
		<li>Quản lý tài khoản User</li>
		<li>Đăng tin tuyển dụng</li>
		<li>Quản lý hồ sơ ứng viên</li>
		<li>Quy trình tuyển dụng, đặt lịch phong vấn, ghi chú ...</li>
		<li>Báo cáo và thông kê dữ liệu</li>
	</ol>
	<h4>4.2 Yêu cầu phi chứng năng</h4>
		<table>
			<tr>
				<th>chức năng</th>
				<th>Mô tả</th>
			</tr>
			<tr>
				<td>Hiệu năng</td>
				<td>Thời gian phản hồi khi thao tác</td>
			</tr>
			<tr>
				<td>Bảo mật</td>
				<td>Bảo mật dữ liêu cá nhân, ứng viên , nhân sự và hệ thống, xác thực bằng OTP ...</td>
			</tr>
			<tr>
				<td>Khả năng mở rộng</td>
				<td>Cho phép thêm chi nhánh mới ...</td>
			</tr>
			<tr>
				<td>Tính khả dụng</td>
				<td>Hoạt động hệ thống 24/7</td>
			</tr>
		</table>

	
<h3>5. Cấu trúc tài liệu SRC</h3>
	<table>
		<tr>
			<th>Mục</th>
			<th>Nội dung</th>
		</tr>
		<tr>
			<td>Giới thiệu</td>
			<td>Mô tả mục đính, đinh nghĩa, tài liệu kam khảo</td>
		</tr>
		<tr>
			<td>Mô tả tổng quát</td>
			<td>Bối cảnh, người dug, môi trường hệ thống</td>
		</tr>
		<tr>
			<td>Yêu cầu chứng năng</td>
			<td>Mô tả chi tiết tứng chức năng</td>
		</tr>
		<tr>
			<td>Yêu cầu phi chức năng</td>
			<td>Hiệu năng, bảo mật, giao diện, khả năng mở rộng</td>
		</tr>
		<tr>
			<td>thiết kế giao diện</td>
			<td>Giao diên thân thiện dễ sử dụng, đầy đủ các trang như: đăng kí / nhập, hồ sơ, báo cáo ...</td>
		</tr>
		<tr>
			<td>Phụ Lục</td>
			<td>Sơ đồ UML, dữ liệu, biểu mẫu quynh trình tuyển dung</td>
		</tr>
	</table>
	

<h1>Ex10: BÁO CÁO TƯ VẤN BAN ĐẦU </h1>
Dự án: Xây dựng hệ thống Quản lý học viên và khóa học trực tuyến (LMS) <br>
Đơn vị: Trung tâm đào tạo ngoại ngữ ABC <br>
Người thực hiện: Chuyên viên phân tích hệ thống


<h3>1. Phân tích môi trường hệ thống </h3>
	<h4>1.1 Môi trường hoạt động</h4>
		<p>Môi trường bạn đầu: TT ABC có hơn 1000 học viên và có 30 giảng viên. Các quy trình quản lý học viên, điêm danh, và chấm điểm đang thực hiện thủ công, gây mất rất nhiều thời gian 
			Thiếu chính xác, khó kiểm soát
		</p>
		<p>Ban lãnh đạo mong muốn, có một hệ thông có thể tự động hoá như sau: </p>
		<ul>
			<li>Quản lý học viên, giảng viên, và khoá học</li>
			<li>Tự động hoá việc điểm danh, và chấm điểm</li>
			<li>Giúp học viên học online, và xem tiến độ học tập, quá trình ..</li>
		</ul>
	<h4>1.2 Môi trường kĩ thuật</h4>
		<ul>
			<li><strong>Phần cứng :</strong> hệ thốn chạy trên máy chủ</li>
			<li><strong>Phần mền :</strong> hỗ trợ truy cập đa nền tảng</li>
			<li><strong>Mạng :</strong> kết nối mảng để sử dụng hệ thống</li>
		</ul>
	<h4>Môi trường pháp lý và tổ chức</h4>
		<ul>
			<li>Tuân thủ nghị định và luật pháp nhà nước</li>
			<li>Phì hợp với quy định giao dục</li>
		</ul>
<h3>2. Xác định stakeholder</h3>
	<table>
		<tr>
			<th>Nhóm Stakeholder</th>
			<th>Vai trò</th>
			<th>Mối quan Tâm</th>
			<th>Mức độ ưu tiên</th>
		</tr>
		<tr>
			<td>Học Viên</td>
			<td>Là người sử dụng chính hệ thống</td>
			<td>Giao diện thân thiện dễ sử dụng, đày đủ chức năng cần có</td>
			<td>Critical</td>
		</tr>
		<tr>
			<td>Giảng viên</td>
			<td>chịu trách nghiệm giảng bài online/ offine , điểm, bài tập</td>
			<td>Hệ thống chấm điếm, upload các bài giảng online, thời gian biểu lớp học</td>
			<td>Major</td>
		</tr>
		<tr>
			<td>Trợ Giảng</td>
			<td>Điểm danh, kiêm tra tiến độ của HV, báo cáo kết quả HV</td>
			<td>Hệ thông điểm danh, báo cáo đánh giá HV</td>
			<td>Major</td>
		</tr>
		<tr>
			<td>Ban Giám đốc</td>
			<td>Phê duyệt, Giám sát hệ thống</td>
			<td>Hiệu quả vận hành, báo cáo, doanh thu</td>
			<td>Major</td>
		</tr>
		<tr>
			<td>Nhóm kĩ thuật</td>
			<td>Bảo trì, phát triển hê thống</td>
			<td>Tính ổn định, bảo mật, </td>
			<td>Major</td>
		</tr>
		<tr>
			<td>Quan trị viên</td>
			<td>Quản lý dữ liệu</td>
			<td>dễ thao tác, toàn bộ quyên hạn</td>
			<td>Major</td>
		</tr>
		<tr>
			<td>Nhà nước, Bộ giao dục</td>
			<td>Kiểm tra tính giao dục và bảo mật của hệ thống</td>
			<td>Thuế, quynh trình giảng dạy phù hợp đối tượng HS SV</td>
			<td>Minor</td>
		</tr>
	</table>

<h3>3. Xác định nguồn yêu cầu & kĩ thuật thu thập</h3>
	<table>
		<tr>
			<th>Nguồn Y/c</th>
			<th>Phương Pháp thu thập</th>
			<th>Nội dung chính</th>
		</tr>
		<tr>
			<td>Ban Giám Đốc</td>
			<td>Phỏng vấn sâu</td>
			<td>Nhu cầu tổng thể, mục tiêu phát tiển</td>
		</tr>
		<tr>
			<td>Giảng viên</td>
			<td>Khảo sát & quan sát</td>
			<td>Cách chấm điểm, quản lý bài học</td>
		</tr>
		<tr>
			<td>Học viên</td>
			<td>Khảo sát trực tuyến</td>
			<td>Trải nghiệm hcoj tập và khó khăn trong vc học tập và sử dụng Hê thống</td>
		</tr>
		<tr>
			<td>Hệ thống cũ</td>
			<td>Tài liệu</td>
			<td>Phân tính tài liệu đánh giá, ptr</td>
		</tr>
		<tr>
			<td>Nhóm IT</td>
			<td>Phỏng vẫn kĩ thuật</td>
			<td>Yêu cầu hạ tầng ntn, kết nối, Phân phôi quyền</td>
		</tr>
	</table>
<h3>4. Phân Loại yêu cầu chứng năng và phi chứng năng</h3>
	<h4>4.1 Y/c Chứng năng</h4>
		<ol>
			<li>Đăng nhập / xuất , kí hệ thống</li>
			<li>Chỉnh sửa hồ sơ</li>
			<li>Quản lý khoá học</li>
			<li>Học trực tuyến</li>
			<li>Điểm danh & chấm điểm</li>
			<li>Báo cáo - thông kê</li>
		</ol>
	<h4>4.2 Y./c Phi chứng năng</h4>
	<table>
			<tr>
				<th>chức năng</th>
				<th>Mô tả</th>
			</tr>
			<tr>
				<td>Hiệu năng</td>
				<td>Thời gian phản hồi khi thao tác</td>
			</tr>
			<tr>
				<td>Bảo mật</td>
				<td>Bảo mật dữ liêu cá nhân,  học viên , Giảng viên và hệ thống, xác thực bằng OTP ...</td>
			</tr>
			<tr>
				<td>Khả năng mở rộng</td>
				<td>Cho phép thêm chi nhánh mới ...</td>
			</tr>
			<tr>
				<td>Tính khả dụng</td>
				<td>Hoạt động hệ thống 24/7</td>
			</tr>
		</table>
<h3>5. Gới ý cấu trúc SRS</h3>
<table>
		<tr>
			<th>Mục</th>
			<th>Nội dung</th>
		</tr>
		<tr>
			<td>Giới thiệu</td>
			<td>Mô tả mục đính, đinh nghĩa, tài liệu kam khảo</td>
		</tr>
		<tr>
			<td>Mô tả tổng quát</td>
			<td>Bối cảnh, người dug, môi trường hệ thống</td>
		</tr>
		<tr>
			<td>Yêu cầu chứng năng</td>
			<td>Mô tả chi tiết tứng chức năng</td>
		</tr>
		<tr>
			<td>Yêu cầu phi chức năng</td>
			<td>Hiệu năng, bảo mật, giao diện, khả năng mở rộng</td>
		</tr>
		<tr>
			<td>thiết kế giao diện</td>
			<td>Giao diên thân thiện dễ sử dụng, đầy đủ các trang như: đăng kí / nhập, hồ sơ, báo cáo ...</td>
		</tr>
		<tr>
			<td>Phụ Lục</td>
			<td>Sơ đồ UML, dữ liệu, biểu mẫu quynh trình tuyển dung</td>
		</tr>
	</table>





<h1>HẾT!</h1>








