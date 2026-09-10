# Book Cab

**Test Scenario:** `Book Cab`  

**Total Test Cases:** `18`

## TC-BC-001 - Đăng nhập/Thao tác hợp lệ

**Scenario:** Book Cab  

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

## TC-BC-002 - Username không tồn tại

**Scenario:** Book Cab  

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

## TC-BC-003 - Sai mật khẩu

**Scenario:** Book Cab  

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

## TC-BC-004 - Bỏ trống trường bắt buộc

**Scenario:** Book Cab  

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

## TC-BC-005 - Bỏ trống toàn bộ

**Scenario:** Book Cab  

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

## TC-BC-006 - Dữ liệu sai định dạng

**Scenario:** Book Cab  

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

## TC-BC-007 - Vượt giới hạn ký tự

**Scenario:** Book Cab  

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

## TC-BC-008 - Giá trị tối thiểu

**Scenario:** Book Cab  

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

## TC-BC-009 - Giá trị tối đa

**Scenario:** Book Cab  

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

## TC-BC-010 - Ký tự đặc biệt

**Scenario:** Book Cab  

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

## TC-BC-011 - SQL Injection

**Scenario:** Book Cab  

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

## TC-BC-012 - XSS Script

**Scenario:** Book Cab  

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

## TC-BC-013 - Session hết hạn

**Scenario:** Book Cab  

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

## TC-BC-014 - Mất kết nối mạng

**Scenario:** Book Cab  

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

## TC-BC-015 - Thao tác đồng thời

**Scenario:** Book Cab  

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

## TC-BC-016 - Dữ liệu trùng lặp

**Scenario:** Book Cab  

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

## TC-BC-017 - Không có quyền

**Scenario:** Book Cab  

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

## TC-BC-018 - Business Rule

**Scenario:** Book Cab  

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
