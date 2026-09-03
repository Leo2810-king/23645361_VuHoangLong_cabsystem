# Traceability: BR - FR - AC - API

## BR01 - Quản lý tài khoản khách hàng
- FR01 -> POST /auth/register -> AC01
- FR02 -> POST /auth/login, POST /auth/logout -> AC01
- FR03 -> GET/PATCH /customers/me -> AC01
- FR04 -> POST /auth/login + security -> AC01, AC14

## BR02 - Đặt xe
- FR05-FR09 -> POST /rides/estimate -> AC02
- FR05-FR10 -> POST /rides -> AC02

## BR03 - Tìm và phân công tài xế
- FR11-FR16 -> POST /rides/{rideId}/matching -> AC03
- FR17 -> POST /rides/{rideId}/accept, POST /rides/{rideId}/reject -> AC03, AC04
- FR18-FR19 -> GET /rides/{rideId}/matching/status -> AC04, AC05

## BR04 - Theo dõi chuyến đi
- FR20-FR23 -> GET /rides/{rideId} -> AC06
- FR24-FR27 -> PATCH /rides/{rideId}/status -> AC07
- FR23 -> PATCH /rides/{rideId}/location -> AC06

## BR05 - Quản lý thanh toán và tính cước
- FR28 -> GET /rides/{rideId}/fare -> AC08
- FR29-FR33 -> POST /payments -> AC09
- FR33-FR34 -> GET /payments/{paymentId} -> AC09, AC10
- FR35 -> POST /payments/{paymentId}/retry -> AC10
- FR31-FR32 -> mô hình paymentToken/reference, không nhận số thẻ/CVV trong CAB

## BR06 - Thông báo
- FR36-FR42 -> GET /notifications -> AC11
- Đánh dấu đã đọc -> PATCH /notifications/{notificationId}/read

## BR07 - Quản lý tài xế và phương tiện
- FR43 -> POST /drivers -> AC12
- FR44 -> GET/PATCH /drivers/me -> AC12
- FR45 -> GET/PATCH /drivers/me/vehicle -> AC12
- FR46-FR47 -> PATCH /drivers/me/status -> AC12
- FR48 -> PATCH /drivers/me/location -> AC12

## BR08 - Quản lý vận hành
- FR49 -> GET /admin/customers -> AC13
- FR50 -> GET/PATCH /admin/drivers -> AC13
- FR51 -> GET/PATCH /admin/vehicles -> AC13
- FR52-FR54 -> GET /admin/rides + POST /admin/rides/{rideId}/support -> AC13
- FR55 -> GET /admin/payments -> AC13

## BR09 - Phân quyền và bảo mật
- FR56 -> JWT Bearer Authentication -> AC14
- FR57 -> Role: CUSTOMER, DRIVER, STAFF, ADMIN -> AC14
- FR58 -> 401/403 + RBAC -> AC14
- FR59 -> schema/API không chứa dữ liệu thẻ nhạy cảm; kiểm soát truy cập tài nguyên
- FR60 -> GET /admin/audit-logs -> AC15

## BR10 - Báo cáo
- FR61 -> GET /reports/rides -> AC16
- FR62 -> GET /reports/revenue -> AC16
- FR63 -> GET /reports/completion-rate -> AC16
- FR64 -> GET /reports/cancellation-rate -> AC16
- FR65 -> GET /reports/drivers -> AC16

## BR11 - Khả năng mở rộng
- FR66 -> ServiceType enum là điểm mở rộng cho loại dịch vụ
- FR67 -> PaymentMethod enum + payment provider abstraction
- FR68 -> Notification type/provider abstraction
- FR69 -> API chia theo resource/service độc lập
- FR70 -> versioning /api/v1 và OpenAPI contract giúp triển khai chức năng mới hạn chế ảnh hưởng hệ thống hiện tại

## Acceptance Criteria summary
- AC01: Authentication + customer profile
- AC02: Ride creation
- AC03: Driver matching
- AC04: Automatic rematching
- AC05: No-driver response
- AC06: Ride tracking
- AC07: Ride state transition
- AC08: Fare calculation
- AC09: Payment
- AC10: Payment retry
- AC11: Notifications
- AC12: Driver/vehicle management
- AC13: Operations
- AC14: Authentication/authorization
- AC15: Audit
- AC16: Reports
- AC17: Extensibility
