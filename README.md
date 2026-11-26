# order-management-power-apps
Ứng dụng canvas quản lý đơn hàng online, xây dựng bằng Power Apps và SharePoint Lists.

Các màn hình danh sách đơn, tạo đơn và chi tiết đơn đã hoạt động;
flow gửi email xác nhận (Power Automate) đang được xây dựng.

## Công nghệ
Power Apps (Canvas app, bố cục Tablet) · SharePoint Lists · Power Automate (đang thực hiện)

## Thiết kế dữ liệu (SharePoint Lists)

| List | Các cột chính |
|---|---|
| Products | Title (tên sản phẩm), SKU (duy nhất), Price, Stock, ReorderLevel, Category (Choice), Active (Yes/No) |
| Customers | Title (họ tên), Phone, Email, Address |
| Orders | Title (mã đơn), Customer (Lookup), Product (Lookup), Quantity, UnitPrice, Total (cột tính), Status (Choice), OrderDate, Note |

Orders liên kết với Customers và Products bằng cột Lookup.
Kiểm tra dữ liệu Quantity > 0, SKU duy nhất,
index cho Status và OrderDate, bật Versioning.

## Tính năng
- Danh sách đơn hàng, tìm kiếm và lọc theo trạng thái
- Tạo đơn: chọn khách hàng và sản phẩm, nhập số lượng, đơn giá và tổng tiền tự động điền
- Chi tiết đơn: xem đầy đủ thông tin, cập nhật trạng thái (Đang giao / Hoàn tất / Hủy)
