# CAB Booking API

Đây là bộ đặc tả API OpenAPI cho hệ thống đặt xe CAB dựa trên BR01-BR11, FR01-FR70 và AC01-AC17.

## 1. File chính

- `openapi/openapi.yaml`: API Specification.
- `docs/traceability.md`: Mapping BR -> FR -> AC -> API.

## 2. Mở bằng Swagger Editor

Mở Swagger Editor:
https://editor.swagger.io/

Sau đó mở/paste nội dung `openapi/openapi.yaml`.

Swagger sẽ hiển thị các nhóm:
- Authentication
- Customers
- Rides
- Driver Matching
- Drivers
- Vehicles
- Payments
- Notifications
- Administration
- Audit
- Reports

## 3. Chạy Swagger UI local

Có thể dùng Docker với Swagger UI:

```bash
docker run -p 8081:8080 \
  -e SWAGGER_JSON=/foo/openapi.yaml \
  -v ${PWD}/openapi:/foo \
  swaggerapi/swagger-ui
```

Mở:
http://localhost:8081

## 4. Try it out

OpenAPI chỉ là hợp đồng API. Nút `Try it out` cần backend thật tại:

http://localhost:8080/api/v1

Nếu chưa có backend thì Swagger chỉ dùng để xem/kiểm tra specification.

## 5. GitHub

```bash
git init
git add .
git commit -m "Add CAB Booking OpenAPI specification"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/cab-booking-api.git
git push -u origin main
```

## 6. Lưu ý

Không đưa số thẻ, CVV hoặc thông tin thanh toán nhạy cảm vào API CAB. Với thanh toán điện tử, dùng payment token/reference do payment provider cấp.

Các trạng thái chuyến được chuẩn hóa:
SEARCHING_DRIVER -> DRIVER_ASSIGNED -> ARRIVED -> PICKED_UP -> IN_PROGRESS -> COMPLETED

Có thể CANCELLED hoặc NO_DRIVER_AVAILABLE theo tình huống nghiệp vụ.
