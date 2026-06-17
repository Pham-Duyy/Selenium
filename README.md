# Automated Testing with Selenium (Chrome/Edge DevTools Recorder)

Dự án thực hành xây dựng kịch bản kiểm thử tự động (Automation Testing) sử dụng công cụ **Trình ghi (DevTools Recorder)** tích hợp sẵn trên trình duyệt. Bài tập tập trung vào việc thiết kế và thực thi kiểm thử tuyến tính (Linear Testing) cho một luồng quy trình nghiệp vụ thương mại điện tử cơ bản.

## 📌 Tổng Quan Dự Án
* **Mục tiêu:** Thực hành tìm hiểu công cụ kiểm thử tự động và xây dựng tối thiểu 03 kịch bản kiểm thử mẫu (Test Cases) cho các chức năng phổ biến của một hệ thống website.
* **Môi trường thử nghiệm (Target Website):** [SauceDemo](https://www.saucedemo.com/) (Nền tảng thương mại điện tử chuẩn dành cho thực hành kiểm thử).
* **Công cụ sử dụng:** Microsoft Edge / Google Chrome DevTools Recorder (Hỗ trợ xuất định dạng tương thích với Selenium / Puppeteer).

---

## 📋 Danh Sách Kịch Bản Kiểm Thử (Test Cases)

Hệ thống ghi nhận và thực thi liên tục chuỗi 03 quy trình kiểm thử tự động dưới đây:

| STT | Tên Kịch Bản (Test Case) | Mô Tả Các Bước (Steps) | Kết Quả Mong Đợi (Expected Result) | Trạng Thái |
| :---: | :--- | :--- | :--- | :---: |
| **TC 01** | **Đăng Nhập Thành Công** | 1. Truy cập hệ thống.<br>2. Nhập định danh `standard_user`.<br>3. Nhập mật khẩu `secret_sauce`.<br>4. Click button `Login`. | Chuyển hướng thành công vào trang chủ bán hàng (`/inventory.html`). | **PASS** |
| **TC 02** | **Thêm Vào Giỏ Hàng** | 1. Tại danh sách sản phẩm, chọn mặt hàng đầu tiên (Sauce Labs Backpack).<br>2. Click button `Add to cart`. | Icon giỏ hàng hiển thị badge số lượng cập nhật tăng lên `1`. | **PASS** |
| **TC 03** | **Đăng Xuất Hệ Thống** | 1. Kích hoạt menu điều hướng (Burger Menu).<br>2. Click chọn liên kết `Logout`. | Hệ thống hủy phiên làm việc, điều hướng an toàn trở lại trang Đăng nhập ban đầu. | **PASS** |

---

## 📸 Kết Quả Thực Thi & Minh Chứng (Replay Evidence)

Kịch bản kiểm thử sau khi được ghi hình đã được chạy lại tự động (**Replay**) hoàn chỉnh. Toàn bộ các bước kiểm tra (Assertions) đều đạt trạng thái hợp lệ (**Màu xanh lá cây / Pass**), không xảy ra lỗi gián đoạn hay lệch phần tử định vị (Locators).

### 1. Khởi tạo quy trình và Đăng nhập (TC 01)
Hệ thống tự động điều hướng đến URL mục tiêu, tìm kiếm các thẻ đầu vào thông qua thuộc tính định vị ID (`#user-name`, `#password`) để điền thông tin và thực hiện sự kiện kích hoạt click chuyển trang.

### 2. Tương tác Thêm sản phẩm & Đăng xuất (TC 02 & TC 03)
Trình ghi tự động bắt các Selector tương ứng của button bán hàng và các liên kết điều hướng ẩn trong Sidebar Menu để hoàn tất vòng đời kiểm thử.

---

## 🛠️ Hướng Dẫn Chạy Kịch Bản (Dành cho Người chấm bài)

Nếu muốn tái định cấu hình hoặc chạy lại trực tiếp kịch bản này trên máy tính của thầy/cô:

1. Tải file kịch bản đuôi `.json` đính kèm trong thư mục mã nguồn này về máy.
2. Mở trình duyệt Chrome hoặc Microsoft Edge, nhấn **F12** (hoặc chuột phải chọn **Inspect** / **Kiểm tra**).
3. Di chuyển đến tab **Recorder** (Trình ghi). Nếu bị ẩn, bấm vào dấu cộng `+` bên cạnh các tab để hiển thị.
4. Bấm vào biểu tượng **Nhập bản ghi (Import recording)** và chọn file `.json` vừa tải.
5. Nhấn nút **Phát lại (Replay)** để quan sát toàn bộ quá trình trình duyệt tự động hóa thao tác.

---
*Báo cáo kết quả thực hành môn Kiểm thử phần mềm tự động - Sinh viên thực hiện.*
