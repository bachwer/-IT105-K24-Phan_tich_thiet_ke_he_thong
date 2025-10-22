

## **EX1: Phân loại Hệ thống Thông tin**

  -----------------------------------------------------------------------
  **Chức năng**           **Loại hệ thống tương   **Mô tả**
                          ứng**                   
  ----------------------- ----------------------- -----------------------
  Giao dịch bán hàng      **TPS -- Transaction    Thu thập, xử lý, lưu
                          Processing System**     trữ và truy xuất dữ
                                                  liệu giao dịch hàng
                                                  ngày. Ví dụ: POS, đặt
                                                  hàng online, hóa đơn
                                                  điện tử.

  Phân tích xu hướng kinh **DSS -- Decision       Hỗ trợ nhà quản lý cấp
  doanh                   Support System**        trung ra quyết định bán
                                                  cấu trúc, phân tích
                                                  "what-if".

  Bảng tổng quan hiệu     **EIS -- Executive      Cung cấp thông tin
  suất hàng tháng cho CEO Information System**    chiến lược, trực quan
                                                  bằng dashboard và biểu
                                                  đồ.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## **EX2: Lựa chọn mô hình phát triển phần mềm**

  -----------------------------------------------------------------------
  **Dự án**         **Đặc điểm**      **Mô hình**       **Lý do lựa
                                                        chọn**
  ----------------- ----------------- ----------------- -----------------
  A. Quản lý điểm   Yêu cầu ổn định,  **Waterfall**     Quy trình tuần
  trường cấp 2      chuẩn hóa                           tự, dễ kiểm soát
                                                        tiến độ.

  B. App đặt lịch   Thị trường thay   **Agile**         Linh hoạt, phản
  khám bệnh         đổi nhanh                           hồi sớm từ người
                                                        dùng.

  C. Ngân hàng điện Phức tạp, bảo mật **Spiral**        Phân tích rủi ro
  tử                cao                                 mỗi vòng lặp, có
                                                        nguyên mẫu kiểm
                                                        chứng.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## **EX3: Các yếu tố môi trường hệ thống**

###  **Con Người**

-   Khách hàng, Đối tác nhà hàng, Tài xế, Quản trị viên hệ thống. \###
    **Dữ Liệu**
-   Người dùng, nhà hàng, đơn hàng, vị trí GPS. \### 🔁 **Quy Trình**

1.  Chọn món → 2. Đặt hàng → 3. Nhà hàng xử lý → 4. Giao hàng → 5. Đánh
    giá. \###  **Phần Mềm**

-   App khách hàng, App tài xế, App nhà hàng, Backend. \### ⚙️ **Phần
    Cứng**
-   Smartphone, Tablet, POS, Server, thiết bị mạng.

------------------------------------------------------------------------

## **EX4: Các giai đoạn trong dự án Điểm danh sinh viên**

  -----------------------------------------------------------------------
  **Giai đoạn**                       **Việc cần làm**
  ----------------------------------- -----------------------------------
  **Planning**                        Xác định mục tiêu, phạm vi, nhân
                                      sự, chi phí, thời gian.

  **Analysis**                        Thu thập, mô hình hóa yêu cầu, viết
                                      SRS.

  **Design**                          Thiết kế kiến trúc, CSDL, UI/UX.

  **Implementation**                  Lập trình backend, frontend, tích
                                      hợp API.

  **Testing**                         Unit, Integration, System, UAT.

  **Deployment & Maintenance**        Triển khai, đào tạo, bảo trì.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## **EX5: Dự án Hệ thống Điểm danh QR**

###  **Giai đoạn 1: Planning**

-   Mục tiêu: Tự động hóa điểm danh bằng QR code.
-   Phạm vi: Giảng viên, sinh viên, phòng đào tạo.
-   Kế hoạch: 1 PM, 2 Backend, 1 Mobile, 1 Web, 1 Tester. \### 🔍 **Giai
    đoạn 2: Requirement Analysis**
-   Thu thập yêu cầu, mô hình hóa Use Case, Activity. \### 🏗️ **Giai
    đoạn 3: System Design**
-   Kiến trúc Client--Server, sơ đồ Class & Sequence, thiết kế UI/UX.

------------------------------------------------------------------------

## **EX6: Chọn sơ đồ UML phù hợp**

  -----------------------------------------------------------------------
  **Tình huống**          **Sơ đồ UML tương ứng** **Mục đích**
  ----------------------- ----------------------- -----------------------
  Mô tả chức năng người   Use Case Diagram        Xác định hành vi hệ
  dùng                                            thống.

  Mô tả lớp và quan hệ    Class Diagram           Mô tả cấu trúc tĩnh.

  Mô tả luồng xử lý       Activity Diagram        Mô tả quy trình.

  Mô tả triển khai hệ     Deployment Diagram      Mô tả phần cứng và phần
  thống                                           mềm.

  Mô tả tương tác theo    Sequence Diagram        Mô tả luồng thông điệp.
  thời gian                                       
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## **EX7: Dự án "Đăng ký tiêm chủng online"**

  -----------------------------------------------------------------------
  **Giai đoạn**                       **Mô tả hoạt động chính**
  ----------------------------------- -----------------------------------
  Planning                            Xác định mục tiêu, phạm vi, kế
                                      hoạch nguồn lực.

  Analysis                            Thu thập yêu cầu chức năng & phi
                                      chức năng, vẽ Use Case.

  Design                              Thiết kế kiến trúc, CSDL, UI/UX, vẽ
                                      Class & Sequence Diagram.

  Implementation                      Xây dựng Backend, Frontend, tích
                                      hợp API.

  Testing                             Kiểm thử chức năng, bảo mật, hiệu
                                      năng, UAT.

  Deployment & Maintenance            Triển khai, đào tạo, bảo trì, hỗ
                                      trợ người dùng.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## **EX8: Hệ thống học trực tuyến**

###  **Tác nhân & chức năng**

  **Actor**    **Chức năng chính**
  ------------ ---------------------------------------------------
  Học viên     Đăng ký, xem khóa học, học, làm bài, xem điểm.
  Giảng viên   Quản lý khóa học, chấm điểm, phản hồi.
  Admin        Quản lý tài khoản, khóa học, báo cáo, phân quyền.

###  **Phân loại hệ thống thông tin**

-   **TPS:** Giao dịch học viên -- khóa học.
-   **MIS:** Báo cáo thống kê học tập.
-   **DSS:** Phân tích dữ liệu phục vụ quyết định chiến lược.

###  **Mô hình phát triển đề xuất**

-   **Agile (Scrum):** Linh hoạt, phản hồi sớm, cải tiến liên tục.

###  **Ba sơ đồ UML chính**

1.  **Use Case Diagram** -- mô tả chức năng & tác nhân.
2.  **Class Diagram** -- cấu trúc dữ liệu.
3.  **Sequence Diagram** -- luồng tương tác theo thời gian.
