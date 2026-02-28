# 🔗 REQUIREMENT TRACEABILITY MATRIX (RTM)

Tài liệu này thể hiện mối liên hệ giữa yêu cầu hệ thống (Requirement) và các ca kiểm thử (Test Case).

📌 **Requirement Coverage: 100%**  
(Mỗi Requirement được liên kết với tối thiểu 2 Test Case)

---

## 📋 RTM Table

| Requirement ID | Mô tả yêu cầu | Test Case ID liên quan | Coverage Status |
|----------------|--------------|------------------------|------------------|
| **R1** | Người dùng đăng ký bằng email hợp lệ | TC_AUTH_001, TC_AUTH_002 | Covered |
| **R2** | Không cho đăng ký khi email sai định dạng | TC_AUTH_003, TC_AUTH_004, TC_AUTH_005 | Covered |
| **R3** | Mật khẩu tối thiểu 8 ký tự | TC_AUTH_006, TC_AUTH_007, TC_AUTH_008 | Covered |
| **R4** | Đăng nhập thành công với thông tin hợp lệ | TC_AUTH_009, TC_AUTH_010, TC_AUTH_015 | Covered |
| **R5** | Đăng nhập thất bại khi sai mật khẩu | TC_AUTH_011, TC_AUTH_012 | Covered |
| **R6** | Quên mật khẩu gửi email đặt lại | TC_AUTH_013, TC_AUTH_014 | Covered |
| **R7** | Tìm kiếm hiển thị đúng kết quả | TC_CART_016, TC_CART_017, TC_CART_018, TC_CART_019, TC_CART_020 | Covered |
| **R8** | Lọc sản phẩm theo giá hoạt động đúng | TC_CART_021, TC_CART_022, TC_CART_023, TC_CART_024, TC_CART_025 | Covered |
| **R9** | Xem chi tiết sản phẩm | TC_CART_026, TC_CART_027 | Covered |
| **R10** | Thêm sản phẩm vào giỏ thành công | TC_CART_028, TC_CART_029, TC_CART_030 | Covered |
| **R11** | Cập nhật số lượng trong giỏ hàng | TC_CART_031, TC_CART_032, TC_CART_033, TC_CART_034 | Covered |
| **R12** | Xóa sản phẩm khỏi giỏ hàng | TC_CART_035, TC_CART_036 | Covered |
| **R13** | Thanh toán bắt buộc nhập địa chỉ giao hàng | TC_CHK_037, TC_CHK_038 | Covered |
| **R14** | Chọn phương thức thanh toán (COD / Visa) | TC_CHK_039, TC_CHK_040, TC_CHK_041 | Covered |
| **R15** | Đặt hàng thành công | TC_CHK_042, TC_CHK_043 | Covered |
| **R16** | Lưu và hiển thị lịch sử đơn hàng | TC_CHK_044, TC_CHK_045 | Covered |