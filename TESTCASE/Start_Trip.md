# Start Trip

**Test Scenario:** `Start Trip`  

**Total Test Cases:** `18`

## TC-ST-001 - Đăng nhập/Thao tác hợp lệ

**Scenario:** Start Trip  

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

## TC-ST-002 - Username không tồn tại

**Scenario:** Start Trip  

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

## TC-ST-003 - Sai mật khẩu

**Scenario:** Start Trip  

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

## TC-ST-004 - Bỏ trống trường bắt buộc

**Scenario:** Start Trip  

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

## TC-ST-005 - Bỏ trống toàn bộ

**Scenario:** Start Trip  

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

## TC-ST-006 - Dữ liệu sai định dạng

**Scenario:** Start Trip  

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

## TC-ST-007 - Vượt giới hạn ký tự

**Scenario:** Start Trip  

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

## TC-ST-008 - Giá trị tối thiểu

**Scenario:** Start Trip  

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

## TC-ST-009 - Giá trị tối đa

**Scenario:** Start Trip  

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

## TC-ST-010 - Ký tự đặc biệt

**Scenario:** Start Trip  

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

## TC-ST-011 - SQL Injection

**Scenario:** Start Trip  

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

## TC-ST-012 - XSS Script

**Scenario:** Start Trip  

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

## TC-ST-013 - Session hết hạn

**Scenario:** Start Trip  

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

## TC-ST-014 - Mất kết nối mạng

**Scenario:** Start Trip  

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

## TC-ST-015 - Thao tác đồng thời

**Scenario:** Start Trip  

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

## TC-ST-016 - Dữ liệu trùng lặp

**Scenario:** Start Trip  

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

## TC-ST-017 - Không có quyền

**Scenario:** Start Trip  

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

## TC-ST-018 - Business Rule

**Scenario:** Start Trip  

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
