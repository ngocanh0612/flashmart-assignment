# Phân tích kỹ thuật sử dụng LEFT JOIN và hàm COUNT()
Khi sử dụng `LEFT JOIN`, các bản ghi bên bảng trái không có giao dịch (như Charlie) vẫn được bảo toàn. Nếu dùng `COUNT(*)`, hệ thống sẽ đếm nhầm dòng giá trị NULL thành 1 đơn hàng. Do đó, phải dùng `COUNT(o.order_id)` để tự động bỏ qua giá trị NULL và trả về kết quả chính xác bằng 0.
