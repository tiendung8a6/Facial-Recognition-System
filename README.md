# Hướng Dẫn Khởi Chạy Dự Án

## 1.Cài Đặt

### 1.1 Cài Đặt XAMPP và Import Cơ Sở Dữ Liệu

1. Truy cập trang [XAMPP](https://www.apachefriends.org/download.html) để tải và cài đặt.
2. Cài đặt và mở XAMPP, Start Apache và MySQL. Lưu ý: Nếu Apache không Start được, đổi cổng thành 8080 [hướng dẫn đổi cổng](https://stackoverflow.com/questions/11294812/how-to-change-xampp-apache-server-port).
3. Mở trình duyệt, truy cập PHPMyAdmin bằng [http://localhost/phpmyadmin](http://localhost/phpmyadmin) hoặc [http://localhost:8080/phpmyadmin](http://localhost:8080/phpmyadmin) nếu đã đổi cổng thành 8080.
4. Trong PHPMyAdmin, chọn Import và chọn file "face_recognizer.sql" để import Cơ sở dữ liệu.

### 1.2 Cài Đặt Python và Visual Studio Code

1. Cài đặt [Python](https://www.python.org/downloads/).
2. Cài đặt [Visual Studio Code](https://code.visualstudio.com/download/).

### 1.3 Cài Đặt Thư Viện Python Cần Thiết

1. Mở thư mục chương trình trong Visual Studio Code.
2. Mở Terminal và nhập các lệnh sau để cài đặt thư viện:

```bash
pip install Pillow==9.5.0
pip install numpy
pip install opencv-python
pip install tk
pip install tkcalendar
pip install mysql-connector-python
pip install opencv-contrib-python
```

Hoặc chạy lệnh duy nhất:

```bash
pip install Pillow==9.5.0 numpy opencv-python tk tkcalendar mysql-connector-python opencv-contrib-python
```

## 2. Chạy Ứng Dụng

1. Mở Visual Studio Code và mở thư mục chương trình.
2. Chạy file ["login.py"](https://github.com/tiendung8a6/Facial-Recognition-System/blob/main/login.py) để khởi động ứng dụng.
3. Đăng nhập bằng tài khoản Admin:
   - Tài khoản: admin
   - Mật khẩu: 123456

## 3. Hướng Dẫn Sử Dụng

### 3.1 Đăng Nhập và Quản Lý Tài Khoản

- **Đăng Nhập:**
  - Sử dụng tài khoản Admin hoặc tài khoản Giáo viên để truy cập vào hệ thống.
- **Quyền Hạn:**
  - Admin: Có quyền sử dụng toàn bộ chức năng của phần mềm.
  - Sinh viên: Thêm, sửa, xóa thông tin sinh viên, chụp ảnh bằng Webcam, và train model nhận dạng.
  - Giáo viên: Thêm, sửa, xóa thông tin giáo viên.

### 3.2 Quản Lý Thông Tin Học Viên và Giáo Viên

- **Sinh viên:**
  - Thêm, sửa, xóa thông tin sinh viên.
  - Chụp ảnh sinh viên bằng Webcam.
  - Lựa chọn "Training Data" để huấn luyện mô hình nhận dạng sinh viên sau khi chụp ảnh.
- **Giáo viên:**
  - Thêm, sửa, xóa thông tin giáo viên.

### 3.3 Quản Lý Môn Học và Buổi Học

- **Môn học:**
  - Quản lý thông tin môn học.
  - Đăng ký môn học cho sinh viên.
  - Thêm môn học cho giáo viên.
- **Buổi học:**
  - Thêm, sửa, xóa thông tin buổi học cho từng môn học.

### 3.4 Xem Ảnh và Nhận Dạng

- **Xem ảnh:**
  - Hiển thị tất cả các ảnh sinh viên đã chụp.
- **Nhận dạng:**
  - Admin: Điểm danh tất cả buổi học của tất cả giáo viên.
  - Chọn Môn học/ID Bài học trong ngày và mở Camera để điểm danh.
  - Hệ thống thông báo sinh viên đã điểm danh thành công và lưu vào database.
  - Kiểm tra thời gian vào/ra lớp và so sánh với thời gian bắt đầu/kết thúc để lưu trạng thái điểm danh.

### 3.5 Quản Lý Điểm Danh và Thống Kê

- **Điểm danh:**
  - Xem thông tin tất cả các bản điểm danh được lưu trữ trên database.
- **Thống kê:**
  - Thống kê sinh viên đi muộn, trốn về sớm, hoặc không điểm danh.

### 3.6 Sử Dụng Cho Giáo Viên

- **Nhận Dạng:**
  - Cho phép giáo viên điểm danh tất cả buổi học trong ngày mà họ được sắp xếp dạy.
