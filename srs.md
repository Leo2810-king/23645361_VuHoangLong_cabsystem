       Dự án xây dựng hệ thống CAB System – Nền tảng đặt xe

B1:bussiness content
| Nội dung               | Mô tả                                                                                       |
| ---------------------- | ------------------------------------------------------------------------------------------- |
| **Business**           | Công ty ABC cung cấp dịch vụ đặt xe trực tuyến                                              |
| **Vấn đề hiện tại**    | Phân công tài xế thủ công, khó theo dõi chuyến, thanh toán chưa tập trung, khó mở rộng      |
| **Mục tiêu**           | Xây dựng nền tảng CAB có khả năng phục vụ nhiều khách hàng/tài xế và dễ mở rộng             |
| **Khách hàng**         | Đăng ký, đặt xe, theo dõi chuyến, thanh toán, xem lịch sử, đánh giá tài xế                  |
| **Tài xế**             | Quản lý hồ sơ/phương tiện, nhận/từ chối chuyến, cập nhật trạng thái, chia sẻ vị trí         |
| **Nhân viên vận hành** | Quản lý khách hàng, tài xế, phương tiện, chuyến đi, giao dịch và báo cáo                    |
| **Business goal**      | Tự động hóa điều phối, nâng cao trải nghiệm khách hàng, tăng khả năng mở rộng và độ ổn định |
| **Yêu cầu quan trọng** | Matching tài xế, thanh toán, thông báo, quản trị, bảo mật, logging, báo cáo                 |
| **Yêu cầu tương lai**  | Thêm dịch vụ, phương thức thanh toán, nhà cung cấp thông báo và thay đổi công nghệ dễ dàng  |




B2: B2. Xác định các Stack Folder và vai trò
| STT | Stack / Folder                     | Vai trò trong hệ thống CAB                                   | Mức độ quan trọng |
| --- | ---------------------------------- | ------------------------------------------------------------ | ----------------- |
| 1   | **Frontend / Client**              | Giao diện cho khách hàng, tài xế và nhân viên vận hành       | Cao               |
| 2   | **API / Backend**                  | Xử lý nghiệp vụ và kết nối các thành phần của hệ thống       | Rất cao           |
| 3   | **Authentication & Authorization** | Đăng nhập, xác thực và phân quyền người dùng                 | Rất cao           |
| 4   | **Ride Management**                | Tạo, quản lý và cập nhật trạng thái chuyến đi                | Rất cao           |
| 5   | **Driver Matching / Dispatch**     | Tìm kiếm và phân công tài xế phù hợp                         | Rất cao           |
| 6   | **Location / GPS**                 | Theo dõi vị trí tài xế và hỗ trợ tìm tài xế gần khách        | Cao               |
| 7   | **Pricing / Fare**                 | Tính cước chuyến đi                                          | Cao               |
| 8   | **Payment**                        | Xử lý thanh toán tiền mặt và điện tử                         | Rất cao           |
| 9   | **Notification**                   | Gửi thông báo cho khách hàng và tài xế                       | Cao               |
| 10  | **Database**                       | Lưu trữ tài khoản, chuyến đi, tài xế, phương tiện, giao dịch | Rất cao           |
| 11  | **Message Queue / Event Bus**      | Xử lý bất đồng bộ giữa các thành phần                        | Cao               |
| 12  | **Admin / Operation**              | Quản lý khách hàng, tài xế, chuyến đi và vận hành            | Cao               |
| 13  | **Reporting / Analytics**          | Thống kê chuyến, doanh thu và hiệu quả hoạt động             | Trung bình        |
| 14  | **Logging / Audit**                | Lưu vết thao tác và hỗ trợ kiểm tra sự cố                    | Cao               |
| 15  | **External Services**              | Tích hợp cổng thanh toán, bản đồ, SMS/Push Notification      | Cao              

<img width="1169" height="879" alt="image" src="https://github.com/user-attachments/assets/3832707e-7015-4ea0-b98c-a2faee755577" />


B3. Mục tiêu nghiệp vụ (Business Goals)
| Mã       | Business Goal             | Mục tiêu                                                                                        |
| -------- | ------------------------- | ----------------------------------------------------------------------------------------------- |
| **BG01** | **Tự động tìm tài xế**    | Tự động xác định và phân công tài xế phù hợp, ưu tiên tài xế gần khách hàng.                    |
| **BG02** | **Quản lý đặt xe**        | Cho phép khách hàng tạo và quản lý yêu cầu đặt xe nhanh chóng, chính xác.                       |
| **BG03** | **Theo dõi chuyến đi**    | Cho phép khách hàng theo dõi trạng thái chuyến đi và vị trí tài xế theo thời gian thực.         |
| **BG04** | **Quản lý tài xế**        | Quản lý thông tin, phương tiện và trạng thái hoạt động của tài xế.                              |
| **BG05** | **Tính cước tự động**     | Tự động xác định số tiền khách hàng phải trả dựa trên thông tin chuyến đi và loại dịch vụ.      |
| **BG06** | **Quản lý thanh toán**    | Hỗ trợ thanh toán tiền mặt và thanh toán điện tử thông qua nhà cung cấp bên ngoài.              |
| **BG07** | **Gửi thông báo**         | Gửi thông báo kịp thời cho khách hàng và tài xế về các sự kiện của chuyến đi.                   |
| **BG08** | **Quản lý vận hành**      | Hỗ trợ nhân viên theo dõi, quản lý và xử lý các vấn đề phát sinh trong quá trình vận hành.      |
| **BG09** | **Bảo mật và phân quyền** | Bảo vệ dữ liệu và kiểm soát quyền truy cập của từng nhóm người dùng.                            |
| **BG10** | **Báo cáo và thống kê**   | Cung cấp báo cáo về số chuyến, doanh thu, tỷ lệ hoàn thành, hủy chuyến và hiệu quả tài xế.      |
| **BG11** | **Khả năng mở rộng**      | Cho phép hệ thống phục vụ số lượng lớn khách hàng, tài xế và mở rộng chức năng trong tương lai. |
| **BG12** | **Đảm bảo tính ổn định**  | Đảm bảo lỗi ở một thành phần như thanh toán hoặc thông báo không làm ngừng toàn bộ hệ thống.    |

 
 B4: xác định phạm vi yêu cầu phải làm
 | STT | Module                           | Phạm vi phải làm | Chức năng chính                                                              | Không làm / ngoài phạm vi                               |
| --- | -------------------------------- | ---------------- | ---------------------------------------------------------------------------- | ------------------------------------------------------- |
| 1   | **QLKH – Quản lý khách hàng**    | **Phải làm**     | Đăng ký, đăng nhập, cập nhật thông tin, xem lịch sử chuyến, đánh giá tài xế  | Không quản lý thông tin ngoài dịch vụ CAB               |
| 2   | **QLTài xế – Quản lý tài xế**    | **Phải làm**     | Tạo tài khoản, cập nhật hồ sơ, quản lý trạng thái, thông tin phương tiện     | Không quản lý lương, hợp đồng lao động                  |
| 3   | **QLĐặt xe – Quản lý đặt xe**    | **Phải làm**     | Nhập điểm đón/điểm đến, chọn loại xe, tạo và hủy yêu cầu                     | Không hỗ trợ đặt các dịch vụ không liên quan đến CAB    |
| 4   | **Điều phối tài xế**             | **Phải làm**     | Tìm tài xế phù hợp, ưu tiên tài xế gần, xử lý từ chối/không phản hồi         | Không phân công thủ công là chức năng chính             |
| 5   | **QLChuyến đi – Quản lý chuyến** | **Phải làm**     | Theo dõi trạng thái, cập nhật trạng thái chuyến, lưu lịch sử chuyến          | Không quản lý hành trình ngoài hệ thống CAB             |
| 6   | **QLVị trí – GPS**               | **Phải làm**     | Theo dõi vị trí tài xế, hỗ trợ tìm tài xế và dự kiến thời gian đến           | Không xây dựng hệ thống bản đồ riêng                    |
| 7   | **QLCước – Tính cước**           | **Phải làm**     | Tính số tiền phải trả dựa trên loại dịch vụ và thông tin chuyến              | Chưa triển khai các chính sách giá chưa được thống nhất |
| 8   | **QLThanh toán**                 | **Phải làm**     | Thanh toán tiền mặt/điện tử, xử lý giao dịch thất bại, lưu lịch sử giao dịch | **Không lưu thông tin nhạy cảm của thẻ/tài khoản**      |
| 9   | **QLThông báo**                  | **Phải làm**     | Thông báo đặt xe, tài xế nhận chuyến, tài xế đến, hoàn thành, thanh toán     | Không tự xây dựng nhà mạng/SMS riêng                    |
| 10  | **QLVận hành/Admin**             | **Phải làm**     | Quản lý KH, tài xế, phương tiện, chuyến đi, xử lý sự cố, phân quyền          | Không cho nhân viên thường thực hiện thao tác nhạy cảm  |
| 11  | **Báo cáo – Thống kê**           | **Phải làm**     | Số chuyến, doanh thu, tỷ lệ hoàn thành/hủy, hiệu quả tài xế                  | Không xây dựng hệ thống BI phức tạp ở giai đoạn đầu     |
| 12  | **Bảo mật & Audit**              | **Phải làm**     | Xác thực, phân quyền, bảo vệ dữ liệu, lưu vết thao tác                       | Không lưu dữ liệu nhạy cảm không cần thiết              |
| 13  | **Mở rộng hệ thống**             | **Phải làm**     | Thiết kế để thêm dịch vụ, phương thức thanh toán, nhà cung cấp thông báo     | Không cần triển khai tất cả dịch vụ mới ngay từ đầu     |

SAU KHI ĐÁP ỨNG CÁC NH CẦU CỦA KHÁCH HÀNG 

B5. Business Requirements
| Mã BR    |  Business Requirement          | Diễn giải                                                                                              |
| -------- | --------------------------     | ------------------------------------------------------------------------------------------------------ |
| **BR01** | Đặt chuyến                     | Hệ thống cho phép khách hàng nhập điểm đón, điểm đến, chọn loại xe và gửi yêu cầu đặt xe.              |
| **BR02** | Quản lý khách hàng             | Hệ thống cho phép khách hàng đăng ký, đăng nhập và cập nhật thông tin cá nhân.                         |
| **BR03** | Tìm và phân công tài xế        | Hệ thống tự động tìm tài xế phù hợp dựa trên vị trí, trạng thái sẵn sàng và các tiêu chí vận hành.     |
| **BR04** | Nhận chuyến                    | Tài xế có thể nhận hoặc từ chối yêu cầu chuyến đi.                                                     |
| **BR05** | Theo dõi chuyến đi             | Khách hàng có thể theo dõi tài xế, thời gian dự kiến đến và trạng thái chuyến đi.                      |
| **BR06** | Cập nhật trạng thái chuyến     | Tài xế có thể cập nhật các trạng thái: đã đến, đã đón khách, đang di chuyển và hoàn thành.             |
| **BR07** | Quản lý tài xế                 | Hệ thống cho phép quản lý hồ sơ, phương tiện và trạng thái hoạt động của tài xế.                       |
| **BR08** | Tính cước                      | Hệ thống xác định số tiền khách hàng phải trả dựa trên loại dịch vụ và thông tin chuyến đi.            |
| **BR09** | Thanh toán                     | Hệ thống hỗ trợ thanh toán bằng tiền mặt và phương thức điện tử thông qua nhà cung cấp bên ngoài.      |
| **BR10** | Xử lý thanh toán thất bại      | Hệ thống thông báo khi thanh toán điện tử thất bại và cho phép xử lý lại theo chính sách doanh nghiệp. |
| **BR11** | Thông báo                      | Hệ thống gửi thông báo cho khách hàng và tài xế về các sự kiện quan trọng của chuyến đi.               |
| **BR12** | Quản lý lịch sử                | Hệ thống lưu và cho phép tra cứu lịch sử chuyến đi, thanh toán và giao dịch.                           |
| **BR13** | Đánh giá tài xế                | Khách hàng có thể đánh giá tài xế sau khi chuyến đi hoàn thành.                                        |
| **BR14** | Quản lý vận hành               | Nhân viên vận hành có thể quản lý khách hàng, tài xế, phương tiện và chuyến đi.                        |
| **BR15** | Phân quyền                     | Hệ thống kiểm soát quyền truy cập đối với các chức năng quản trị và thao tác nhạy cảm.                 |
| **BR16** | Báo cáo                        | Hệ thống cung cấp báo cáo về số chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả tài xế.     |
| **BR17** | Bảo mật dữ liệu                | Hệ thống bảo vệ thông tin cá nhân, phương tiện, vị trí và dữ liệu giao dịch của người dùng.            |
| **BR18** | Lưu vết hoạt động              | Hệ thống ghi nhận các thao tác quan trọng để phục vụ kiểm tra và xử lý sự cố.                          |
| **BR19** | Khả năng mở rộng               | Hệ thống có khả năng mở rộng để phục vụ số lượng lớn khách hàng, tài xế và các chức năng mới.          |
| **BR20** | Tính sẵn sàng                  | Lỗi tại một thành phần như thanh toán hoặc thông báo không được làm ngừng toàn bộ hệ thống.            |

B6. Business Process
| Mã       | Business Process            | Actor                                 | Các bước thực hiện                                                                                                                                                                                                                                                                                                                  |
| -------- | --------------------------- | ------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BP01** | **Đặt chuyến**              | Khách hàng, Hệ thống                  | 1. Khách hàng đăng nhập → 2. Nhập điểm đón, điểm đến → 3. Chọn loại xe → 4. Gửi yêu cầu → 5. Hệ thống tiếp nhận → 6. Tìm tài xế phù hợp → 7. Nếu có tài xế, gửi yêu cầu → 8. Nếu **không có tài xế**, thông báo khách hàng và kết thúc yêu cầu.                                                                                                                 |
| **BP02** | **Tìm và phân công tài xế** | Hệ thống, Tài xế                      | 1. Hệ thống tìm tài xế phù hợp → 2. Gửi thông báo cho tài xế → 3. Tài xế **nhận chuyến** → tiếp tục thực hiện chuyến. → 4. Nếu tài xế **từ chối** → tìm tài xế khác. → 5. Nếu tài xế **không phản hồi trong thời gian quy định** → chuyển sang tài xế khác. → 6. Nếu tất cả tài xế đều từ chối/không phản hồi → thông báo khách hàng **không tìm được tài xế**. |
| **BP03** | **Thực hiện chuyến đi**     | Tài xế, Khách hàng                    | 1. Tài xế nhận chuyến → 2. Di chuyển đến điểm đón → 3. Cập nhật "Đã đến" → 4. Đón khách → 5. Cập nhật "Đang di chuyển" → 6. Đến điểm đến → 7. Hoàn thành chuyến. **Nếu tài xế hủy chuyến:** hệ thống ghi nhận lý do và xử lý theo chính sách hủy, có thể tìm tài xế khác nếu chuyến chưa bắt đầu.                                                               |
| **BP04** | **Theo dõi chuyến đi**      | Khách hàng, Hệ thống                  | 1. Khách hàng xem thông tin chuyến → 2. Theo dõi vị trí tài xế → 3. Xem ETA → 4. Theo dõi trạng thái. **Nếu mất kết nối:** hệ thống giữ trạng thái gần nhất và cập nhật lại khi kết nối được khôi phục.                                                                                                                                                         |
| **BP05** | **Tính cước**               | Hệ thống                              | 1. Chuyến đi hoàn thành → 2. Lấy thông tin loại xe/dịch vụ và chuyến đi → 3. Tính cước → 4. Xác định số tiền phải trả → 5. Hiển thị cho khách hàng. **Nếu dữ liệu tính cước lỗi:** ghi nhận lỗi và chuyển xử lý theo quy định vận hành.                                                                                                                         |
| **BP06** | **Thanh toán**              | Khách hàng, Hệ thống, Payment Gateway | 1. Khách hàng chọn phương thức thanh toán → 2. Hệ thống gửi yêu cầu thanh toán → 3. Nhà cung cấp xử lý → 4. Nhận kết quả. **Nếu tài khoản không đủ tiền:** giao dịch thất bại → thông báo khách hàng → cho phép thanh toán lại hoặc chọn phương thức khác. **Nếu Payment Gateway không phản hồi:** ghi nhận trạng thái giao dịch và xử lý lại theo chính sách.  |
| **BP07** | **Đánh giá tài xế**         | Khách hàng                            | 1. Chuyến hoàn thành → 2. Khách hàng chọn đánh giá → 3. Nhập số sao/nhận xét → 4. Gửi đánh giá → 5. Hệ thống lưu đánh giá. **Nếu gửi đánh giá thất bại:** thông báo lỗi và cho phép gửi lại.                                                                                                                                                                    |
| **BP08** | **Quản lý tài xế**          | Tài xế, Nhân viên                     | 1. Tạo/đăng ký tài khoản → 2. Cập nhật hồ sơ → 3. Cập nhật phương tiện → 4. Chuyển sang trạng thái sẵn sàng → 5. Nhận chuyến. **Nếu tài xế không đủ điều kiện hoạt động:** không cho chuyển sang trạng thái sẵn sàng.                                                                                                                                           |
| **BP09** | **Quản lý vận hành**        | Nhân viên vận hành                    | 1. Đăng nhập → 2. Xem chuyến đang diễn ra → 3. Kiểm tra trạng thái tài xế → 4. Xử lý chuyến bị lỗi → 5. Tra cứu giao dịch. **Nếu nhân viên không có quyền:** từ chối thao tác và ghi log.                                                                                                                                                                       |
| **BP10** | **Báo cáo**                 | Nhân viên, Quản lý                    | 1. Chọn loại báo cáo → 2. Hệ thống tổng hợp dữ liệu → 3. Tính chỉ số → 4. Hiển thị báo cáo. **Nếu dữ liệu thiếu/lỗi:** thông báo và ghi nhận lỗi thay vì tạo báo cáo sai.                                                                                                                                                                                       |
| **BP11** | **Gửi thông báo**           | Hệ thống, Khách hàng, Tài xế          | 1. Phát sinh sự kiện → 2. Tạo thông báo → 3. Gửi đến người dùng. **Nếu gửi thất bại:** thử lại hoặc chuyển sang kênh khác theo chính sách; lỗi thông báo không làm dừng chức năng đặt xe.                                                                                                                                                                       |
| **BP12** | **Hủy chuyến**              | Khách hàng, Tài xế                    | 1. Người dùng yêu cầu hủy → 2. Hệ thống kiểm tra trạng thái chuyến → 3. Kiểm tra điều kiện/phí hủy → 4. Xác nhận hủy → 5. Cập nhật trạng thái → 6. Thông báo cho bên liên quan. **Nếu không đủ điều kiện hủy:** thông báo lý do và không thực hiện hủy.                                                                                                         |

B7. Phân rã Business Requirement → Functional Requirement
| BR                                        | Functional Requirement (FR)                                                                  |
| ----------------------------------------- | -------------------------------------------------------------------------------------------- |
| **BR01: Quản lý tài khoản khách hàng**    | **FR01:** Cho phép khách hàng đăng ký tài khoản                                              |
|                                           | **FR02:** Cho phép khách hàng đăng nhập/đăng xuất                                            |
|                                           | **FR03:** Cho phép khách hàng cập nhật thông tin cá nhân                                     |
|                                           | **FR04:** Cho phép khách hàng xác thực tài khoản trước khi sử dụng chức năng đặt xe          |
| **BR02: Đặt xe**                          | **FR05:** Cho phép khách hàng nhập điểm đón                                                  |
|                                           | **FR06:** Cho phép khách hàng nhập điểm đến                                                  |
|                                           | **FR07:** Cho phép khách hàng lựa chọn loại xe/dịch vụ                                       |
|                                           | **FR08:** Hệ thống xác định vị trí hiện tại của khách hàng                                   |
|                                           | **FR09:** Hệ thống tính toán thông tin chuyến đi dự kiến                                     |
|                                           | **FR10:** Cho phép khách hàng gửi yêu cầu đặt xe                                             |
| **BR03: Tìm và phân công tài xế**         | **FR11:** Hệ thống xác định vị trí khách hàng                                                |
|                                           | **FR12:** Hệ thống tìm các tài xế đang online và sẵn sàng nhận chuyến trong khu vực phù hợp  |
|                                           | **FR13:** Hệ thống lọc tài xế theo loại xe phù hợp với yêu cầu                               |
|                                           | **FR14:** Hệ thống ưu tiên tài xế ở gần khách hàng                                           |
|                                           | **FR15:** Hệ thống có thể ưu tiên tài xế dựa trên tiêu chí vận hành/đánh giá                 |
|                                           | **FR16:** Hệ thống gửi yêu cầu chuyến đến tài xế được lựa chọn                               |
|                                           | **FR17:** Tài xế có thể chấp nhận hoặc từ chối chuyến                                        |
|                                           | **FR18:** Nếu tài xế không phản hồi hoặc từ chối, hệ thống tiếp tục tìm tài xế khác          |
|                                           | **FR19:** Hệ thống thông báo cho khách hàng khi không tìm được tài xế                        |
| **BR04: Theo dõi chuyến đi**              | **FR20:** Cho phép khách hàng xem trạng thái tìm tài xế                                      |
|                                           | **FR21:** Hiển thị thông tin tài xế đã nhận chuyến                                           |
|                                           | **FR22:** Hiển thị thời gian dự kiến tài xế đến                                              |
|                                           | **FR23:** Theo dõi vị trí tài xế trên bản đồ                                                 |
|                                           | **FR24:** Tài xế cập nhật trạng thái đã đến điểm đón                                         |
|                                           | **FR25:** Tài xế cập nhật trạng thái đã đón khách                                            |
|                                           | **FR26:** Tài xế cập nhật trạng thái đang di chuyển                                          |
|                                           | **FR27:** Tài xế cập nhật trạng thái hoàn thành chuyến                                       |
| **BR05: Quản lý thanh toán và tính cước** | **FR28:** Hệ thống tính cước dựa trên loại dịch vụ và thông tin chuyến đi                    |
|                                           | **FR29:** Cho phép khách hàng thanh toán bằng tiền mặt                                       |
|                                           | **FR30:** Cho phép khách hàng thanh toán điện tử                                             |
|                                           | **FR31:** Hệ thống kết nối với nhà cung cấp thanh toán bên ngoài                             |
|                                           | **FR32:** Không lưu thông tin nhạy cảm của thẻ/tài khoản thanh toán trong CAB                |
|                                           | **FR33:** Hệ thống ghi nhận kết quả giao dịch thanh toán                                     |
|                                           | **FR34:** Thông báo cho khách hàng khi thanh toán thất bại                                   |
|                                           | **FR35:** Cho phép xử lý lại giao dịch thanh toán theo chính sách                            |
| **BR06: Thông báo**                       | **FR36:** Thông báo khi yêu cầu đặt xe được tiếp nhận                                        |
|                                           | **FR37:** Thông báo khi tài xế nhận chuyến                                                   |
|                                           | **FR38:** Thông báo khi tài xế đến điểm đón                                                  |
|                                           | **FR39:** Thông báo khi chuyến đi hoàn thành                                                 |
|                                           | **FR40:** Thông báo kết quả thanh toán                                                       |
|                                           | **FR41:** Gửi thông báo chuyến mới cho tài xế                                                |
|                                           | **FR42:** Gửi thông báo khi có thay đổi liên quan đến chuyến đi                              |
| **BR07: Quản lý tài xế và phương tiện**   | **FR43:** Cho phép tài xế đăng ký tài khoản hoặc nhân viên tạo tài khoản                     |
|                                           | **FR44:** Cho phép tài xế cập nhật hồ sơ                                                     |
|                                           | **FR45:** Cho phép tài xế cập nhật thông tin phương tiện                                     |
|                                           | **FR46:** Cho phép tài xế chuyển trạng thái online/offline                                   |
|                                           | **FR47:** Cho phép tài xế chuyển sang trạng thái sẵn sàng nhận chuyến                        |
|                                           | **FR48:** Hệ thống lưu thông tin vị trí của tài xế                                           |
| **BR08: Quản lý vận hành**                | **FR49:** Nhân viên xem danh sách khách hàng                                                 |
|                                           | **FR50:** Nhân viên quản lý thông tin tài xế                                                 |
|                                           | **FR51:** Nhân viên quản lý thông tin phương tiện                                            |
|                                           | **FR52:** Nhân viên xem các chuyến đang diễn ra                                              |
|                                           | **FR53:** Nhân viên kiểm tra trạng thái tài xế                                               |
|                                           | **FR54:** Nhân viên hỗ trợ xử lý chuyến bị lỗi                                               |
|                                           | **FR55:** Nhân viên tra cứu lịch sử giao dịch                                                |
| **BR09: Phân quyền và bảo mật**           | **FR56:** Hệ thống xác thực người dùng trước khi sử dụng chức năng yêu cầu tài khoản         |
|                                           | **FR57:** Hệ thống phân quyền khách hàng, tài xế và nhân viên                                |
|                                           | **FR58:** Hệ thống kiểm soát quyền thực hiện các thao tác quản trị                           |
|                                           | **FR59:** Bảo vệ thông tin cá nhân, phương tiện, vị trí và giao dịch                         |
|                                           | **FR60:** Hệ thống ghi log các thao tác quan trọng                                           |
| **BR10: Báo cáo**                         | **FR61:** Báo cáo số lượng chuyến đi                                                         |
|                                           | **FR62:** Báo cáo doanh thu                                                                  |
|                                           | **FR63:** Báo cáo tỷ lệ chuyến hoàn thành                                                    |
|                                           | **FR64:** Báo cáo tỷ lệ chuyến bị hủy                                                        |
|                                           | **FR65:** Báo cáo hiệu quả hoạt động của tài xế                                              |
| **BR11: Khả năng mở rộng**                | **FR66:** Cho phép thêm loại dịch vụ mới                                                     |
|                                           | **FR67:** Cho phép thêm phương thức thanh toán mới                                           |
|                                           | **FR68:** Cho phép tích hợp thêm nhà cung cấp thông báo                                      |
|                                           | **FR69:** Cho phép mở rộng từng thành phần độc lập khi tải tăng                              |
|                                           | **FR70:** Cho phép triển khai chức năng mới mà hạn chế ảnh hưởng đến hệ thống đang hoạt động |


B8: B8. Business Rules
| Mã       | Business Rule                                                                     |
| -------- | --------------------------------------------------------------------------------- |
| **BR01** | Chỉ tài xế có trạng thái **Sẵn sàng (Available)** mới được nhận chuyến.           |
| **BR02** | Tài xế phải bấm **Accept** trong thời gian quy định để nhận chuyến.               |
| **BR03** | Tài xế có quyền **Accept hoặc Reject** chuyến được gửi đến.                       |
| **BR04** | Tài xế phải có loại xe phù hợp với yêu cầu của khách hàng.                        |
| **BR05** | Một chuyến đi chỉ được gán cho **một tài xế**.                                    |
| **BR06** | Khi tài xế Reject, hệ thống phải tiếp tục tìm tài xế khác.                        |
| **BR07** | Khi không tìm được tài xế phù hợp, hệ thống phải thông báo cho khách hàng.        |
| **BR08** | Chỉ chuyến đã hoàn thành mới được thực hiện thanh toán cuối cùng.                 |
| **BR09** | Chỉ tài khoản có quyền phù hợp mới được thực hiện các chức năng quản trị.         |
| **BR10** | Chỉ tài khoản đã xác thực mới được phép đặt xe.                                   |
| **BR11** | Tài xế phải có phương tiện hợp lệ mới được chuyển sang trạng thái Sẵn sàng.       |
| **BR12** | Hệ thống phải lưu lại các thao tác quan trọng để phục vụ kiểm tra và xử lý sự cố. |

B8. Exceptions
| Mã       | Exception                                        | Cách xử lý                                                                                                |
| -------- | ------------------------------------------------ | --------------------------------------------------------------------------------------------------------- |
| **EX01** | Tài xế **không bấm Accept trước thời hạn**       | Hệ thống tự động **Timeout**, hủy yêu cầu đối với tài xế đó và tìm tài xế tiếp theo.                      |
| **EX02** | Tài xế **Reject** chuyến                         | Hệ thống ghi nhận từ chối và tiếp tục tìm tài xế khác.                                                    |
| **EX03** | Không có tài xế phù hợp                          | Thông báo cho khách hàng rằng không tìm được tài xế và cho phép thử lại.                                  |
| **EX04** | Tài xế chuyển sang Offline/Busy trước khi Accept | Hủy yêu cầu gửi cho tài xế và tìm tài xế khác.                                                            |
| **EX05** | Hai tài xế cùng Accept một chuyến                | Hệ thống chỉ xác nhận tài xế nhận thành công đầu tiên; tài xế còn lại nhận thông báo chuyến đã được nhận. |
| **EX06** | Payment Gateway không phản hồi                   | Ghi nhận giao dịch ở trạng thái Pending và xử lý lại theo chính sách.                                     |
| **EX07** | Thanh toán điện tử thất bại                      | Thông báo khách hàng và cho phép thực hiện thanh toán lại.                                                |
| **EX08** | Mất kết nối trong quá trình chuyến đi            | Lưu trạng thái cuối cùng và đồng bộ lại khi kết nối được khôi phục.                                       |
| **EX09** | Người dùng không đủ quyền thực hiện thao tác     | Từ chối thao tác và ghi nhận vào Audit Log.                                                               |
| **EX10** | Thông tin điểm đón/điểm đến không hợp lệ         | Thông báo lỗi và yêu cầu khách hàng nhập lại thông tin.                                                   |

B9. Domain Model – Các thực thể chính của hệ thống CAB
| STT | Thực thể             | Một số thuộc tính chính                                              | Mô tả                                 |
| --- | -------------------- | -------------------------------------------------------------------- | ------------------------------------- |
| 1   | **Customer**         | CustomerID, Name, Phone, Email, Password                             | Thông tin khách hàng                  |
| 2   | **Driver**           | DriverID, Name, Phone, Status, Rating                                | Thông tin tài xế                      |
| 3   | **Vehicle**          | VehicleID, DriverID, Type, LicensePlate, Status                      | Phương tiện của tài xế                |
| 4   | **Ride**             | RideID, CustomerID, DriverID, Pickup, Destination, Status, CreatedAt | Thông tin chuyến đi                   |
| 5   | **RideType**         | RideTypeID, Name, Description, BaseFare                              | Loại dịch vụ/loại xe                  |
| 6   | **DriverLocation**   | LocationID, DriverID, Latitude, Longitude, Timestamp                 | Vị trí hiện tại/lịch sử vị trí tài xế |
| 7   | **Payment**          | PaymentID, RideID, Amount, Method, Status, PaymentTime               | Thông tin thanh toán                  |
| 8   | **PaymentMethod**    | MethodID, Name                                                       | Phương thức thanh toán                |
| 9   | **Rating**           | RatingID, RideID, CustomerID, DriverID, Score, Comment               | Đánh giá tài xế                       |
| 10  | **Notification**     | NotificationID, UserID, Type, Content, Status, CreatedAt             | Thông báo cho người dùng              |
| 11  | **Staff**            | StaffID, Name, Email, Password, RoleID                               | Nhân viên vận hành                    |
| 12  | **Role**             | RoleID, RoleName                                                     | Quyền của nhân viên                   |
| 13  | **TripStatus**       | StatusID, StatusName                                                 | Các trạng thái của chuyến             |
| 14  | **DriverAssignment** | AssignmentID, RideID, DriverID, Status, SentAt, RespondedAt          | Lưu quá trình gửi chuyến cho tài xế   |
| 15  | **Fare**             | FareID, RideID, Distance, Duration, Amount                           | Chi tiết tính cước                    |

B10 – Non-Functional Requirements (NFR)
| Mã        | Nhóm NFR             | Non-Functional Requirement                                                                                                  |
| --------- | -------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| **NFR01** | **Performance**      | Hệ thống phải phản hồi nhanh khi khách hàng đặt xe và tìm tài xế.                                                           |
| **NFR02** | **Performance**      | Hệ thống phải có khả năng xử lý đồng thời số lượng lớn khách hàng và tài xế.                                                |
| **NFR03** | **Scalability**      | Hệ thống phải có khả năng mở rộng khi số lượng người dùng và chuyến đi tăng.                                                |
| **NFR04** | **Availability**     | Hệ thống phải hoạt động ổn định, hạn chế thời gian ngừng hoạt động.                                                         |
| **NFR05** | **Reliability**      | Lỗi ở Payment hoặc Notification không được làm toàn bộ hệ thống đặt xe ngừng hoạt động.                                     |
| **NFR06** | **Security**         | Người dùng phải được xác thực trước khi sử dụng các chức năng yêu cầu tài khoản.                                            |
| **NFR07** | **Authorization**    | Hệ thống phải kiểm soát quyền truy cập của khách hàng, tài xế và nhân viên.                                                 |
| **NFR08** | **Data Security**    | Thông tin cá nhân, thông tin phương tiện, vị trí và giao dịch phải được bảo vệ.                                             |
| **NFR09** | **Auditability**     | Hệ thống phải lưu vết các thao tác quan trọng để phục vụ kiểm tra và xử lý sự cố.                                           |
| **NFR10** | **Maintainability**  | Các thành phần phải được thiết kế dễ bảo trì và cập nhật.                                                                   |
| **NFR11** | **Modularity**       | Các thành phần như Payment, Notification, Matching có thể phát triển hoặc thay đổi độc lập.                                 |
| **NFR12** | **Extensibility**    | Có thể thêm loại dịch vụ, phương thức thanh toán và nhà cung cấp thông báo mới mà không phải xây dựng lại toàn bộ hệ thống. |
| **NFR13** | **Fault Tolerance**  | Khi một thành phần gặp lỗi, các chức năng không liên quan vẫn phải tiếp tục hoạt động.                                      |
| **NFR14** | **Data Integrity**   | Dữ liệu chuyến đi, thanh toán và trạng thái tài xế phải được đảm bảo chính xác và nhất quán.                                |
| **NFR15** | **Interoperability** | Hệ thống phải có khả năng tích hợp với Payment Gateway, bản đồ/GPS và các dịch vụ thông báo bên ngoài.                      |
| **NFR16** | **Deployability**    | Cho phép triển khai từng phần chức năng mới mà hạn chế ảnh hưởng đến các chức năng đang hoạt động.                          |

B11 – Xác định Use Case
| Actor                    | Use Case                    |
| ------------------------ | --------------------------- |
| **Customer**             | Đăng ký tài khoản           |
|                          | Đăng nhập                   |
|                          | Cập nhật thông tin cá nhân  |
|                          | Đặt xe                      |
|                          | Chọn loại xe                |
|                          | Theo dõi chuyến đi          |
|                          | Hủy chuyến                  |
|                          | Xem lịch sử chuyến          |
|                          | Xem cước                    |
|                          | Thanh toán                  |
|                          | Đánh giá tài xế             |
| **Driver**               | Đăng nhập                   |
|                          | Cập nhật hồ sơ              |
|                          | Cập nhật phương tiện        |
|                          | Bật/Tắt trạng thái sẵn sàng |
|                          | Nhận yêu cầu chuyến         |
|                          | Accept chuyến               |
|                          | Reject chuyến               |
|                          | Cập nhật trạng thái chuyến  |
|                          | Cập nhật vị trí             |
| **Staff**                | Đăng nhập                   |
|                          | Quản lý khách hàng          |
|                          | Quản lý tài xế              |
|                          | Quản lý phương tiện         |
|                          | Quản lý chuyến đi           |
|                          | Xử lý chuyến lỗi            |
|                          | Tra cứu giao dịch           |
|                          | Xem báo cáo                 |
|                          | Quản lý phân quyền          |
| **Payment Gateway**      | Xử lý thanh toán            |
|                          | Trả kết quả thanh toán      |
| **Notification Service** | Gửi thông báo               |
| **Map/GPS Service**      | Cung cấp vị trí             |
|                          | Tính khoảng cách/ETA        |

SƠ ĐỒ USECASE



B12 – Đặc tả Use Case
| Thành phần           | Nội dung                                                                                                                                                                                                                     |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Use Case ID**      | UC01                                                                                                                                                                                                                         |
| **Tên**              | Đặt xe                                                                                                                                                                                                                       |
| **Actor**            | Customer                                                                                                                                                                                                                     |
| **Mục tiêu**         | Khách hàng tạo yêu cầu đặt xe                                                                                                                                                                                                |
| **Pre-condition**    | Customer đã đăng nhập                                                                                                                                                                                                        |
| **Input**            | Điểm đón, điểm đến, loại xe                                                                                                                                                                                                  |
| **Main Flow**        | 1. Customer nhập điểm đón và điểm đến → 2. Chọn loại xe → 3. Hệ thống kiểm tra thông tin → 4. Hệ thống tạo yêu cầu → 5. Hệ thống tìm tài xế → 6. Gửi yêu cầu cho tài xế → 7. Tài xế Accept → 8. Xác nhận chuyến cho Customer |
| **Alternative Flow** | Tài xế Reject → tìm tài xế khác                                                                                                                                                                                              |
| **Exception**        | Tài xế không Accept trong thời hạn → Timeout → tìm tài xế tiếp theo                                                                                                                                                          |
| **Exception**        | Không tìm được tài xế → thông báo Customer                                                                                                                                                                                   |
| **Post-condition**   | Chuyến được tạo và gán cho tài xế hoặc chuyển sang trạng thái không tìm được tài xế                                                                                                                                          |
| Thành phần           | Nội dung                                                                                                                                                    |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Use Case ID**      | UC02                                                                                                                                                        |
| **Tên**              | Tìm và phân công tài xế                                                                                                                                     |
| **Actor**            | System, Driver                                                                                                                                              |
| **Mục tiêu**         | Tìm tài xế phù hợp cho chuyến                                                                                                                               |
| **Pre-condition**    | Đã có yêu cầu đặt xe                                                                                                                                        |
| **Main Flow**        | 1. Xác định vị trí khách → 2. Tìm tài xế Available → 3. Lọc theo loại xe → 4. Tính khoảng cách → 5. Ưu tiên tài xế phù hợp → 6. Gửi yêu cầu → 7. Chờ Accept |
| **Alternative Flow** | Driver Reject → chọn Driver tiếp theo                                                                                                                       |
| **Exception**        | Timeout → chọn Driver tiếp theo                                                                                                                             |
| **Exception**        | Không có Driver → thông báo Customer                                                                                                                        |
| **Post-condition**   | Một Driver được gán vào Ride                                                                                                                                |
| Thành phần         | Nội dung                                                                                                                                                                               |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Use Case ID**    | UC03                                                                                                                                                                                   |
| **Tên**            | Thanh toán                                                                                                                                                                             |
| **Actor**          | Customer, Payment Gateway                                                                                                                                                              |
| **Pre-condition**  | Chuyến đã hoàn thành                                                                                                                                                                   |
| **Main Flow**      | 1. Hệ thống tính cước → 2. Customer chọn phương thức → 3. Gửi yêu cầu thanh toán → 4. Payment Gateway xử lý → 5. Nhận kết quả → 6. Cập nhật trạng thái Payment → 7. Thông báo Customer |
| **Exception**      | Thanh toán thất bại → thông báo Customer → cho phép thanh toán lại                                                                                                                     |
| **Post-condition** | Payment = Success hoặc Failed/Pending                                                                                                                                                  |
| Thành phần         | Nội dung                                                               |
| ------------------ | ---------------------------------------------------------------------- |
| **Use Case ID**    | UC04                                                                   |
| **Tên**            | Cập nhật trạng thái chuyến                                             |
| **Actor**          | Driver                                                                 |
| **Pre-condition**  | Driver đã nhận chuyến                                                  |
| **Main Flow**      | Đã nhận → Đã đến điểm đón → Đã đón khách → Đang di chuyển → Hoàn thành |
| **Exception**      | Cập nhật sai thứ tự → hệ thống từ chối                                 |
| **Post-condition** | Trạng thái Ride được cập nhật                                          |
| Thành phần         | Nội dung                                                                    |
| ------------------ | --------------------------------------------------------------------------- |
| **Use Case ID**    | UC05                                                                        |
| **Tên**            | Đánh giá tài xế                                                             |
| **Actor**          | Customer                                                                    |
| **Pre-condition**  | Chuyến đã hoàn thành                                                        |
| **Main Flow**      | Customer chọn số sao → nhập nhận xét → gửi đánh giá → hệ thống lưu đánh giá |
| **Exception**      | Chuyến chưa hoàn thành → không cho đánh giá                                 |
| **Post-condition** | Rating được lưu và cập nhật điểm tài xế                                     |

B13 – Acceptance Criteria
| Mã AC    | Business Requirement                    | Acceptance Criteria – Tiêu chí chấp nhận                                                                                                                |
| -------- | --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **AC01** | **BR01 – Quản lý tài khoản khách hàng** | Khách hàng có thể đăng ký, đăng nhập và cập nhật thông tin cá nhân thành công. Hệ thống phải từ chối thông tin đăng nhập không hợp lệ.                  |
| **AC02** | **BR02 – Đặt xe**                       | Khách hàng nhập đầy đủ điểm đón, điểm đến và loại xe thì có thể gửi yêu cầu đặt xe thành công.                                                          |
| **AC03** | **BR03 – Tìm tài xế**                   | Hệ thống phải tìm được tài xế đang **Available**, có loại xe phù hợp và ưu tiên tài xế phù hợp/gần khách hàng.                                          |
| **AC04** | **BR03 – Tìm tài xế**                   | Nếu tài xế không Accept trong thời hạn quy định hoặc Reject, hệ thống phải tự động chuyển sang tìm tài xế khác mà khách hàng không cần tạo lại yêu cầu. |
| **AC05** | **BR03 – Tìm tài xế**                   | Nếu không còn tài xế phù hợp, hệ thống phải thông báo rõ ràng cho khách hàng.                                                                           |
| **AC06** | **BR04 – Theo dõi chuyến đi**           | Khách hàng phải xem được tài xế, vị trí tài xế, ETA và trạng thái hiện tại của chuyến đi.                                                               |
| **AC07** | **BR04 – Theo dõi chuyến đi**           | Tài xế có thể cập nhật tuần tự các trạng thái: **Đã đến → Đã đón khách → Đang di chuyển → Hoàn thành**.                                                 |
| **AC08** | **BR05 – Tính cước**                    | Sau khi chuyến hoàn thành, hệ thống phải tính và hiển thị số tiền khách hàng cần thanh toán.                                                            |
| **AC09** | **BR05 – Thanh toán**                   | Khách hàng có thể thanh toán bằng tiền mặt hoặc phương thức điện tử. Hệ thống phải ghi nhận chính xác kết quả giao dịch.                                |
| **AC10** | **BR05 – Thanh toán**                   | Khi thanh toán điện tử thất bại, hệ thống phải thông báo cho khách hàng và cho phép thanh toán lại theo chính sách.                                     |
| **AC11** | **BR06 – Thông báo**                    | Khách hàng nhận được thông báo khi đặt xe, có tài xế nhận, tài xế đến, chuyến hoàn thành và thanh toán có kết quả.                                      |
| **AC12** | **BR07 – Quản lý tài xế**               | Tài xế có thể cập nhật hồ sơ, phương tiện và trạng thái Available/Offline.                                                                              |
| **AC13** | **BR08 – Quản lý vận hành**             | Nhân viên có quyền phù hợp có thể xem và quản lý khách hàng, tài xế, phương tiện, chuyến đi và giao dịch.                                               |
| **AC14** | **BR09 – Bảo mật**                      | Người dùng phải đăng nhập trước khi sử dụng chức năng yêu cầu tài khoản; nhân viên không có quyền không được thực hiện thao tác quản trị bị hạn chế.    |
| **AC15** | **BR09 – Audit**                        | Các thao tác quản trị quan trọng phải được ghi log và có thể tra cứu khi xảy ra sự cố.                                                                  |
| **AC16** | **BR10 – Báo cáo**                      | Nhân viên có quyền có thể xem báo cáo số chuyến, doanh thu, tỷ lệ hoàn thành, tỷ lệ hủy và hiệu quả tài xế.                                             |
| **AC17** | **BR11 – Khả năng mở rộng**             | Có thể thêm loại dịch vụ, phương thức thanh toán hoặc nhà cung cấp thông báo mới mà không phải xây dựng lại toàn bộ hệ thống.                           |

B14 - RTM – Ma trận truy xuất yêu cầu CAB
| Business Process             | BR                                      | FR                                     | UC                         | AC                                                                         |
| ---------------------------- | --------------------------------------- | -------------------------------------- | -------------------------- | -------------------------------------------------------------------------- |
| **BP01 – Quản lý tài khoản** | **BR01 – Quản lý tài khoản khách hàng** | FR01 – Đăng ký tài khoản               | UC01 – Đăng ký             | AC01 – Khách hàng đăng ký thành công và thông tin được lưu                 |
|                              |                                         | FR02 – Đăng nhập                       | UC02 – Đăng nhập           | AC02 – Người dùng đăng nhập thành công với thông tin hợp lệ                |
|                              |                                         | FR03 – Cập nhật thông tin              | UC03 – Cập nhật hồ sơ      | AC03 – Khách hàng cập nhật và lưu thông tin thành công                     |
| **BP02 – Đặt xe**            | **BR02 – Đặt xe**                       | FR04 – Nhập điểm đón                   | UC04 – Đặt xe              | AC04 – Điểm đón hợp lệ được ghi nhận                                       |
|                              |                                         | FR05 – Nhập điểm đến                   | UC04 – Đặt xe              | AC05 – Điểm đến hợp lệ được ghi nhận                                       |
|                              |                                         | FR06 – Chọn loại xe                    | UC04 – Đặt xe              | AC06 – Khách hàng chọn được loại xe                                        |
|                              |                                         | FR07 – Gửi yêu cầu đặt xe              | UC04 – Đặt xe              | AC07 – Yêu cầu đặt xe được tạo thành công                                  |
| **BP03 – Tìm tài xế**        | **BR03 – Tìm và phân công tài xế**      | FR08 – Xác định vị trí khách           | UC05 – Tìm tài xế          | AC08 – Hệ thống xác định được vị trí khách                                 |
|                              |                                         | FR09 – Tìm tài xế Available            | UC05 – Tìm tài xế          | AC09 – Chỉ tài xế Available được đưa vào danh sách                         |
|                              |                                         | FR10 – Lọc theo loại xe                | UC05 – Tìm tài xế          | AC10 – Chỉ tài xế có loại xe phù hợp được lựa chọn                         |
|                              |                                         | FR11 – Ưu tiên tài xế gần/phù hợp      | UC05 – Tìm tài xế          | AC11 – Tài xế phù hợp được ưu tiên                                         |
|                              |                                         | FR12 – Gửi yêu cầu cho tài xế          | UC05 – Tìm tài xế          | AC12 – Tài xế nhận được yêu cầu                                            |
|                              |                                         | FR13 – Accept/Reject                   | UC06 – Nhận chuyến         | AC13 – Tài xế có thể Accept hoặc Reject                                    |
|                              |                                         | FR14 – Xử lý Timeout                   | UC06 – Nhận chuyến         | AC14 – Quá thời hạn không Accept thì hệ thống tìm tài xế khác              |
|                              |                                         | FR15 – Thông báo không tìm được tài xế | UC05 – Tìm tài xế          | AC15 – Khách hàng nhận được thông báo khi không có tài xế                  |
| **BP04 – Theo dõi chuyến**   | **BR04 – Theo dõi chuyến đi**           | FR16 – Xem trạng thái chuyến           | UC07 – Theo dõi chuyến     | AC16 – Khách hàng xem được trạng thái hiện tại                             |
|                              |                                         | FR17 – Xem vị trí tài xế               | UC07 – Theo dõi chuyến     | AC17 – Khách hàng xem được vị trí tài xế                                   |
|                              |                                         | FR18 – Tính ETA                        | UC07 – Theo dõi chuyến     | AC18 – Hệ thống hiển thị thời gian dự kiến                                 |
|                              |                                         | FR19 – Cập nhật trạng thái chuyến      | UC08 – Cập nhật chuyến     | AC19 – Driver cập nhật được các trạng thái hợp lệ                          |
| **BP05 – Thanh toán**        | **BR05 – Tính cước và thanh toán**      | FR20 – Tính cước                       | UC09 – Thanh toán          | AC20 – Hệ thống tính đúng số tiền                                          |
|                              |                                         | FR21 – Thanh toán tiền mặt             | UC09 – Thanh toán          | AC21 – Giao dịch tiền mặt được ghi nhận                                    |
|                              |                                         | FR22 – Thanh toán điện tử              | UC09 – Thanh toán          | AC22 – Giao dịch điện tử được xử lý                                        |
|                              |                                         | FR23 – Xử lý thanh toán thất bại       | UC09 – Thanh toán          | AC23 – Thanh toán thất bại được thông báo và có thể xử lý lại              |
| **BP06 – Thông báo**         | **BR06 – Quản lý thông báo**            | FR24 – Thông báo đặt xe                | UC10 – Gửi thông báo       | AC24 – Khách nhận được thông báo đặt xe                                    |
|                              |                                         | FR25 – Thông báo tài xế nhận chuyến    | UC10 – Gửi thông báo       | AC25 – Khách nhận được thông báo tài xế                                    |
|                              |                                         | FR26 – Thông báo trạng thái chuyến     | UC10 – Gửi thông báo       | AC26 – Thông báo được gửi khi trạng thái thay đổi                          |
| **BP07 – Quản lý vận hành**  | **BR07 – Quản lý vận hành**             | FR27 – Quản lý khách hàng              | UC11 – Quản lý khách hàng  | AC27 – Staff có quyền xem/chỉnh sửa khách hàng                             |
|                              |                                         | FR28 – Quản lý tài xế                  | UC12 – Quản lý tài xế      | AC28 – Staff có quyền quản lý tài xế                                       |
|                              |                                         | FR29 – Quản lý phương tiện             | UC13 – Quản lý phương tiện | AC29 – Staff quản lý được phương tiện                                      |
|                              |                                         | FR30 – Quản lý chuyến                  | UC14 – Quản lý chuyến      | AC30 – Staff xem và xử lý được chuyến                                      |
| **BP08 – Báo cáo**           | **BR08 – Báo cáo**                      | FR31 – Báo cáo số chuyến               | UC15 – Xem báo cáo         | AC31 – Hiển thị chính xác số chuyến                                        |
|                              |                                         | FR32 – Báo cáo doanh thu               | UC15 – Xem báo cáo         | AC32 – Hiển thị chính xác doanh thu                                        |
|                              |                                         | FR33 – Báo cáo tỷ lệ hoàn thành/hủy    | UC15 – Xem báo cáo         | AC33 – Hiển thị đúng tỷ lệ                                                 |
| **BP09 – Bảo mật**           | **BR09 – Bảo mật và phân quyền**        | FR34 – Xác thực người dùng             | UC16 – Xác thực            | AC34 – Người chưa xác thực không truy cập được chức năng yêu cầu đăng nhập |
|                              |                                         | FR35 – Phân quyền                      | UC17 – Phân quyền          | AC35 – Người dùng chỉ thực hiện được chức năng được cấp quyền              |
|                              |                                         | FR36 – Ghi Audit Log                   | UC18 – Ghi nhật ký         | AC36 – Thao tác quan trọng được ghi log                                    |
