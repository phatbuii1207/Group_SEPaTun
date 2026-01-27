# Thiết kế hệ thống quản lý cửa hàng thú cưng (Pet Store Management)

## 1. Class Pet (Lớp cha – lớp cơ sở)

### Tác dụng
- Đại diện cho một thú cưng chung trong cửa hàng.
- Là lớp nền (base class) cho các loại thú cưng cụ thể như `Dog`, `Cat`.

### Các thành phần chính

#### Thuộc tính
- `ID`: mã thú cưng  
- `name`: tên thú cưng  
- `age`: tuổi  
- `price`: giá bán  
- `type`: loại thú cưng (Dog, Cat…)

#### Phương thức
- **Nhập thông tin**: nhập dữ liệu chung cho mọi thú cưng.
- **Hiển thị thông tin**: in thông tin cơ bản của thú cưng.
- **Getter**: cho phép các lớp khác truy cập `id`, `name`, `price`.

### 👉 Ý nghĩa OOP
- Dùng để kế thừa, giúp tránh lặp code.
- Tạo tính đa hình khi quản lý danh sách thú cưng chung.

---

## 2. Class Dog (Lớp con của Pet)

### Tác dụng
- Đại diện cho chó – một loại thú cưng cụ thể.

### Các thành phần chính

#### Thuộc tính riêng
- `breed`: giống chó.
- `isTrained`: tình trạng đã được huấn luyện hay chưa.

#### Phương thức
- **Nhập thông tin**: kế thừa từ `Pet`, bổ sung thông tin riêng của `Dog`.
- **Hiển thị thông tin**: hiển thị thêm thông tin đặc trưng của chó.

### 👉 Ý nghĩa
- Thể hiện kế thừa và mở rộng.
- Giữ đúng đặc điểm riêng của `Dog` nhưng vẫn dùng chung cấu trúc `Pet`.

---

## 3. Class Cat (Lớp con của Pet)

### Tác dụng
- Đại diện cho mèo trong cửa hàng.

### Các thành phần chính

#### Thuộc tính riêng
- `furColor`: màu lông.
- `isIndoor`: mèo nuôi trong nhà hay ngoài trời.

#### Phương thức
- **Nhập thông tin**: nhập thông tin riêng cho mèo.
- **Hiển thị thông tin**: hiển thị thông tin đặc trưng của mèo.

### 👉 Ý nghĩa
- Tương tự `Dog` nhưng cho loại thú cưng khác.
- Thể hiện rõ đa hình khi hiển thị hoặc lưu trữ chung với `Dog`.

---

## 4. Class Customer (Khách hàng)

### Tác dụng
- Lưu trữ thông tin khách hàng mua thú cưng.

### Các thành phần chính

#### Thuộc tính
- `customerId`: mã khách hàng.
- `customerName`: tên khách hàng.
- `phoneNumber`: số điện thoại.

#### Phương thức
- **Nhập thông tin khách hàng**.
- **Hiển thị thông tin khách hàng**.
- **Lấy tên khách hàng** khi cần.

### 👉 Ý nghĩa
- Tách riêng đối tượng khách hàng khỏi các đối tượng khác.
- Tuân thủ nguyên tắc **Single Responsibility**.

---

## 5. Class Order (Đơn hàng)

### Tác dụng
- Quản lý một lần mua hàng của khách.

### Các thành phần chính

#### Thuộc tính
- `orderId`: mã đơn hàng.
- `customer`: khách hàng thực hiện đơn hàng.
- `petList`: danh sách thú cưng được mua.
- `totalPrice`: tổng tiền.

#### Phương thức
- **Thêm thú cưng vào đơn hàng**.
- **Tính tổng tiền**.
- **Hiển thị thông tin đơn hàng**.

### 👉 Ý nghĩa
- Kết nối `Customer` ↔ `Pet`.
- Thể hiện quan hệ **has-a** (Order có Customer, có nhiều Pet).

---

## 6. Class PetStoreManagement (Lớp quản lý)

### Tác dụng
- Là trung tâm điều khiển toàn bộ hệ thống cửa hàng thú cưng.

### Các thành phần chính

#### Thuộc tính
- Danh sách thú cưng trong cửa hàng.
- Danh sách đơn hàng đã tạo.

#### Chức năng
- Thêm thú cưng (`Dog` hoặc `Cat`).
- Xóa thú cưng.
- Tìm thú cưng theo tên.
- Hiển thị toàn bộ thú cưng.
- Tạo đơn hàng và quản lý quá trình mua.

### 👉 Ý nghĩa
- Đóng vai trò **Controller** trong mô hình chương trình đơn giản.
- Quản lý luồng nghiệp vụ chính của hệ thống.

---

## 7. Class Main (Điểm bắt đầu chương trình)

### Tác dụng
- Chạy chương trình.
- Hiển thị menu và nhận lựa chọn từ người dùng.

### Vai trò
- Gọi các chức năng tương ứng trong `PetStoreManagement`.
- Điều hướng luồng hoạt động của hệ thống.

### 👉 Ý nghĩa
- Không chứa logic nghiệp vụ.
- Chỉ làm nhiệm vụ khởi động và điều hướng chương trình.
