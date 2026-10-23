# Báo Cáo Thực Hành: Kiểm Thử Tự Động Với Selenium


## 1. Thông Tin Chung
- **Họ và tên:** Nguyễn Duy Quang
- **Mã sinh viên:** 23010448
- **Môn học:** Kiểm thử phần mềm
- **Website kiểm thử:** [https://www.saucedemo.com/](https://www.saucedemo.com/)
- **Công cụ sử dụng:** Selenium (Automation Testing)

---

## 2. Bảng Đặc Tả 05 Test Cases Kiểm Thử Tự Động

| Mã TC | Tên Test Case | Dữ Liệu Đầu Vào (Test Data) | Các Bước Thực Hiện | Kết Quả Kỳ Vọng (Expected Result) | Kết Quả Thực Tế |
| :--- | :--- | :--- | :--- | :--- | :---: |
| **TC01** | Đăng nhập thất bại | User: `standard_user`<br>Pass: `wrong_pass` | 1. Mở trang đăng nhập<br>2. Nhập User và Pass sai<br>3. Bấm nút `Login` | Hệ thống chặn đăng nhập và hiển thị thông báo lỗi màu đỏ `Epic sadface...` | **PASS** |
| **TC02** | Đăng nhập thành công | User: `standard_user`<br>Pass: `secret_sauce` | 1. Mở trang đăng nhập<br>2. Nhập User và Pass hợp lệ<br>3. Bấm nút `Login` | Đăng nhập thành công, chuyển hướng sang trang danh sách sản phẩm (`/inventory.html`) | **PASS** |
| **TC03** | Thêm sản phẩm vào giỏ hàng | Sản phẩm: `Sauce Labs Backpack` | 1. Đăng nhập hệ thống<br>2. Tìm sản phẩm *Sauce Labs Backpack*<br>3. Bấm nút `Add to cart` | Nút bấm đổi thành `Remove`, biểu tượng giỏ hàng góc phải hiển thị số `1` | **PASS** |
| **TC04** | Kiểm tra giỏ hàng | Giỏ hàng đang có `1` sản phẩm | 1. Bấm vào biểu tượng giỏ hàng ở góc trên bên phải<br>2. Kiểm tra thông tin sản phẩm | Trang `Your Cart` hiển thị đúng tên sản phẩm `Sauce Labs Backpack` | **PASS** |
| **TC05** | Đăng xuất hệ thống | Tài khoản đang đăng nhập | 1. Bấm vào nút Menu (3 gạch ngang) ở góc trên bên trái<br>2. Chọn mục `Logout` | Đăng xuất thành công, hệ thống điều hướng quay về màn hình đăng nhập ban đầu | **PASS** |

---

## 3. Hình Ảnh Minh Hoạ Kết Quả Thực Hiện

### 🔹 Test Case 1: Kiểm thử đăng nhập thất bại (Nhập sai mật khẩu)
- **Mô tả:** Kiểm tra khả năng bắt lỗi của hệ thống khi người dùng nhập sai thông tin xác thực.
- **Hình ảnh minh hoạ:**

<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/d62c3b3e-56a1-4bcc-8c84-23742d12509b" />


---

### 🔹 Test Case 2: Kiểm thử đăng nhập thành công
- **Mô tả:** Xác nhận người dùng có thể truy cập vào trang sản phẩm khi cung cấp đúng tài khoản `standard_user`.
- **Hình ảnh minh hoạ:**

<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/a86d98ec-998d-4631-a42d-32f343302ce0" />


---

### 🔹 Test Case 3: Kiểm thử chức năng thêm sản phẩm vào giỏ hàng
- **Mô tả:** Tự động chọn sản phẩm *Sauce Labs Backpack* và kiểm tra số lượng hiển thị trên icon giỏ hàng.
- **Hình ảnh minh hoạ:**

<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/dfacaf45-3315-4314-b39a-5402c1bebfdd" />

---

### 🔹 Test Case 4: Kiểm thử trang chi tiết giỏ hàng
- **Mô tả:** Truy cập vào giỏ hàng và đối chiếu thông tin sản phẩm đã thêm ở bước trước.
- **Hình ảnh minh hoạ:**

<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/88860b92-941b-4b65-93bd-cbfd145ce2f1" />


---

### 🔹 Test Case 5: Kiểm thử chức năng đăng xuất (Logout)
- **Mô tả:** Mở thanh menu điều hướng và thực hiện đăng xuất khỏi phiên làm việc hiện tại.
- **Hình ảnh minh hoạ:**

<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/13c2ae0e-ce75-4173-97d5-c0c4c4c6d80a" />

---

### 🔹 Tổng kết: Kết quả chạy tự động toàn bộ 05 Test Cases (Test Suite Execution)
- **Mô tả:** Toàn bộ 05 kịch bản kiểm thử được thực thi tự động thông qua Selenium và đều vượt qua bài kiểm tra (**5/5 PASSED**).
- **Hình ảnh minh hoạ:**

<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/bb2e93f0-6bfa-4bbe-a583-c95f025a729e" />



---

## 4. Kết Luận
Qua quá trình tìm hiểu và thực hành với công cụ **Selenium**, em đã nắm được:
1. Cách cài đặt và cấu hình công cụ kiểm thử tự động trên trình duyệt.
2. Cách xác định các phần tử giao diện web (Web Elements) thông qua `ID`, `Class`, `CSS Selector` và `XPath`.
3. Xây dựng và thực thi thành công 05 kịch bản kiểm thử tự động bao phủ các luồng nghiệp vụ chính của một website thương mại điện tử (Đăng nhập, Thêm giỏ hàng, Kiểm tra giỏ hàng, Đăng xuất).
