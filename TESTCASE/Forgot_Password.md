# Forgot Password

**Test Scenario:** `Forgot Password`  

**Total Test Cases:** `18`

## TC-FP-001 - Đăng nhập/Thao tác hợp lệ

**Scenario:** Forgot Password  

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

## TC-FP-002 - Username không tồn tại

**Scenario:** Forgot Password  

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

## TC-FP-003 - Sai mật khẩu

**Scenario:** Forgot Password  

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

## TC-FP-004 - Bỏ trống trường bắt buộc

**Scenario:** Forgot Password  

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

## TC-FP-005 - Bỏ trống toàn bộ

**Scenario:** Forgot Password  

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

## TC-FP-006 - Dữ liệu sai định dạng

**Scenario:** Forgot Password  

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

## TC-FP-007 - Vượt giới hạn ký tự

**Scenario:** Forgot Password  

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

## TC-FP-008 - Giá trị tối thiểu

**Scenario:** Forgot Password  

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

## TC-FP-009 - Giá trị tối đa

**Scenario:** Forgot Password  

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

## TC-FP-010 - Ký tự đặc biệt

**Scenario:** Forgot Password  

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

## TC-FP-011 - SQL Injection

**Scenario:** Forgot Password  

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

## TC-FP-012 - XSS Script

**Scenario:** Forgot Password  

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

## TC-FP-013 - Session hết hạn

**Scenario:** Forgot Password  

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

## TC-FP-014 - Mất kết nối mạng

**Scenario:** Forgot Password  

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

## TC-FP-015 - Thao tác đồng thời

**Scenario:** Forgot Password  

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

## TC-FP-016 - Dữ liệu trùng lặp

**Scenario:** Forgot Password  

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

## TC-FP-017 - Không có quyền

**Scenario:** Forgot Password  

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

## TC-FP-018 - Business Rule

**Scenario:** Forgot Password  

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
