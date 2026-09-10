# Driver Accept Booking

**Test Scenario:** `Driver Accept Booking`  

**Total Test Cases:** `18`

## TC-DAB-001 - Đăng nhập/Thao tác hợp lệ

**Scenario:** Driver Accept Booking  

**Priority:** `High`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
Valid data
```

### Expected Result

Thực hiện thành công

---

## TC-DAB-002 - Username không tồn tại

**Scenario:** Driver Accept Booking  

**Priority:** `High`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
Unknown user
```

### Expected Result

Thông báo không hợp lệ

---

## TC-DAB-003 - Sai mật khẩu

**Scenario:** Driver Accept Booking  

**Priority:** `High`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
Wrong password
```

### Expected Result

Đăng nhập thất bại

---

## TC-DAB-004 - Bỏ trống trường bắt buộc

**Scenario:** Driver Accept Booking  

**Priority:** `High`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
Empty field
```

### Expected Result

Hiển thị Required

---

## TC-DAB-005 - Bỏ trống toàn bộ

**Scenario:** Driver Accept Booking  

**Priority:** `High`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
All empty
```

### Expected Result

Hiển thị validation

---

## TC-DAB-006 - Dữ liệu sai định dạng

**Scenario:** Driver Accept Booking  

**Priority:** `Medium`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
Invalid format
```

### Expected Result

Từ chối dữ liệu

---

## TC-DAB-007 - Vượt giới hạn ký tự

**Scenario:** Driver Accept Booking  

**Priority:** `Medium`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
256 chars
```

### Expected Result

Hiển thị lỗi độ dài

---

## TC-DAB-008 - Giá trị tối thiểu

**Scenario:** Driver Accept Booking  

**Priority:** `Medium`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
Min value
```

### Expected Result

Xử lý đúng giá trị biên

---

## TC-DAB-009 - Giá trị tối đa

**Scenario:** Driver Accept Booking  

**Priority:** `Medium`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
Max value
```

### Expected Result

Xử lý đúng giá trị biên

---

## TC-DAB-010 - Ký tự đặc biệt

**Scenario:** Driver Accept Booking  

**Priority:** `Medium`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
@#$%^
```

### Expected Result

Không làm lỗi hệ thống

---

## TC-DAB-011 - SQL Injection

**Scenario:** Driver Accept Booking  

**Priority:** `High`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
' OR 1=1 --
```

### Expected Result

Không bị SQL Injection

---

## TC-DAB-012 - XSS Script

**Scenario:** Driver Accept Booking  

**Priority:** `High`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
<script>alert(1)</script>
```

### Expected Result

Escape dữ liệu

---

## TC-DAB-013 - Session hết hạn

**Scenario:** Driver Accept Booking  

**Priority:** `Medium`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
Expired session
```

### Expected Result

Yêu cầu đăng nhập lại

---

## TC-DAB-014 - Mất kết nối mạng

**Scenario:** Driver Accept Booking  

**Priority:** `Medium`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
Network off
```

### Expected Result

Thông báo lỗi mạng

---

## TC-DAB-015 - Thao tác đồng thời

**Scenario:** Driver Accept Booking  

**Priority:** `High`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
Concurrent
```

### Expected Result

Chỉ một giao dịch thành công

---

## TC-DAB-016 - Dữ liệu trùng lặp

**Scenario:** Driver Accept Booking  

**Priority:** `High`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
Duplicate
```

### Expected Result

Không tạo dữ liệu trùng

---

## TC-DAB-017 - Không có quyền

**Scenario:** Driver Accept Booking  

**Priority:** `High`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
Guest role
```

### Expected Result

Từ chối truy cập

---

## TC-DAB-018 - Business Rule

**Scenario:** Driver Accept Booking  

**Priority:** `High`

### Preconditions

Hệ thống đang hoạt động và người dùng ở đúng màn hình chức năng

### Test Steps

1. Mở chức năng

2. Nhập dữ liệu theo Test Data

3. Nhấn nút xác nhận

4. Kiểm tra kết quả

### Test Data

```text
Boundary data
```

### Expected Result

Đúng quy tắc nghiệp vụ

---
