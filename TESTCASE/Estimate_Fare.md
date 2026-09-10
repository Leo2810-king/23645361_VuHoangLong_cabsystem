# Estimate Fare

**Test Scenario:** `Estimate Fare`  

**Total Test Cases:** `18`

## TC-EF-001 - Đăng nhập/Thao tác hợp lệ

**Scenario:** Estimate Fare  

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

## TC-EF-002 - Username không tồn tại

**Scenario:** Estimate Fare  

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

## TC-EF-003 - Sai mật khẩu

**Scenario:** Estimate Fare  

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

## TC-EF-004 - Bỏ trống trường bắt buộc

**Scenario:** Estimate Fare  

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

## TC-EF-005 - Bỏ trống toàn bộ

**Scenario:** Estimate Fare  

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

## TC-EF-006 - Dữ liệu sai định dạng

**Scenario:** Estimate Fare  

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

## TC-EF-007 - Vượt giới hạn ký tự

**Scenario:** Estimate Fare  

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

## TC-EF-008 - Giá trị tối thiểu

**Scenario:** Estimate Fare  

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

## TC-EF-009 - Giá trị tối đa

**Scenario:** Estimate Fare  

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

## TC-EF-010 - Ký tự đặc biệt

**Scenario:** Estimate Fare  

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

## TC-EF-011 - SQL Injection

**Scenario:** Estimate Fare  

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

## TC-EF-012 - XSS Script

**Scenario:** Estimate Fare  

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

## TC-EF-013 - Session hết hạn

**Scenario:** Estimate Fare  

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

## TC-EF-014 - Mất kết nối mạng

**Scenario:** Estimate Fare  

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

## TC-EF-015 - Thao tác đồng thời

**Scenario:** Estimate Fare  

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

## TC-EF-016 - Dữ liệu trùng lặp

**Scenario:** Estimate Fare  

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

## TC-EF-017 - Không có quyền

**Scenario:** Estimate Fare  

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

## TC-EF-018 - Business Rule

**Scenario:** Estimate Fare  

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
