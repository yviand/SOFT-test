# 🐞 BÁO CÁO LỖI (BUG REPORTS)

Tài liệu này ghi nhận các lỗi được phát hiện trong quá trình kiểm thử thủ công hệ thống E-Commerce.

---

## 📌 Danh sách Bug

| Bug ID | Summary | Steps to Reproduce | Expected Result | Actual Result | Severity | Priority | Environment |
|--------|---------|-------------------|-----------------|---------------|----------|----------|-------------|
| **BUG_AUTH_001** | Không hiển thị thông báo khi đăng nhập sai mật khẩu | 1. Mở trang Login<br>2. Nhập email hợp lệ<br>3. Nhập sai mật khẩu<br>4. Nhấn “Đăng nhập” | Hiển thị thông báo “Sai mật khẩu” | Không hiển thị thông báo lỗi, hệ thống không phản hồi | Major | High | Chrome / Windows 10 |
| **BUG_CART_002** | Hệ thống chấp nhận số lượng âm trong giỏ hàng | 1. Mở trang Cart<br>2. Nhập giá trị “-2” vào ô Quantity<br>3. Nhấn cập nhật | Hệ thống phải từ chối giá trị âm và hiển thị cảnh báo | Hệ thống chấp nhận giá trị âm và tổng tiền hiển thị âm | **Critical** | High | Edge / Windows 11 |
| **BUG_CART_003** | Tổng tiền giỏ hàng tính sai sau khi lọc sản phẩm | 1. Lọc sản phẩm theo giá<br>2. Thêm sản phẩm vào giỏ<br>3. Kiểm tra tổng tiền | Tổng tiền = Giá x Số lượng (bao gồm VAT) | Tổng tiền không bao gồm VAT | Major | Medium | Chrome / macOS |
| **BUG_CHK_004** | Giỏ hàng không được làm trống sau khi đặt hàng thành công | 1. Thêm sản phẩm vào giỏ<br>2. Thanh toán COD<br>3. Quay lại trang Cart | Giỏ hàng phải được làm trống | Giỏ hàng vẫn giữ nguyên sản phẩm đã mua | Major | High | Chrome / Windows 10 |
| **BUG_CHK_005** | Lỗi hệ thống (500) khi thanh toán bằng thẻ Visa hết hạn | 1. Vào Checkout<br>2. Chọn Visa<br>3. Nhập thẻ hết hạn<br>4. Nhấn thanh toán | Hiển thị thông báo “Thẻ không hợp lệ” | Hệ thống trả về lỗi 500 và màn hình trắng | **Critical** | High | Chrome / Windows 10 |
| **BUG_CART_006** | Không thể nhấn nút “Xóa” trong giỏ hàng trên mobile | 1. Chuyển sang chế độ mobile view<br>2. Mở giỏ hàng<br>3. Nhấn “Xóa” | Nút hoạt động bình thường | Nút bị che bởi layout, không thể click | Major | Medium | Chrome (Mobile View) |
| **BUG_AUTH_007** | Tiêu đề popup “Quên mật khẩu” hiển thị sai định dạng chữ | 1. Mở Login<br>2. Nhấn “Quên mật khẩu” | Tiêu đề in đậm theo thiết kế | Tiêu đề hiển thị sai font-weight | Minor | Low | Chrome |
| **BUG_CART_008** | Nội dung mô tả sản phẩm bị tràn khỏi khung | 1. Mở sản phẩm có mô tả dài<br>2. Quan sát phần mô tả | Nội dung nằm trong khung, có scroll nếu cần | Nội dung tràn ra ngoài layout | Minor | Low | Firefox |
| **BUG_CHK_009** | Lỗi chính tả trong placeholder ô nhập địa chỉ | 1. Mở Checkout<br>2. Quan sát placeholder | Hiển thị “Nhập địa chỉ của bạn” | Hiển thị sai chính tả | Minor | Low | All Browsers |
| **BUG_AUTH_010** | Thời gian phản hồi khi đăng ký tài khoản chậm | 1. Mở Signup<br>2. Nhập thông tin hợp lệ<br>3. Nhấn Submit | Phản hồi trong < 3 giây | Loading kéo dài bất thường | Minor | Low | Chrome |

---

## 📊 Phân bố mức độ nghiêm trọng (Severity Distribution)

- 🔴 Critical: 2  
- 🟠 Major: 4  
- 🟡 Minor: 4  

---

## 📌 Nhận xét

- Các lỗi **Critical** ảnh hưởng trực tiếp đến tính chính xác dữ liệu và quá trình thanh toán.
- Các lỗi **Major** gây gián đoạn trải nghiệm người dùng.
- Các lỗi **Minor** chủ yếu liên quan đến UI/hiển thị.
