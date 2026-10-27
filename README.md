# Portfolio CV - Phùng Hải Nam

## Mô tả dự án

Portfolio cá nhân dạng trang web tĩnh, giới thiệu Phùng Hải Nam với định hướng Frontend Developer. Trang được xây dựng bằng HTML và CSS thuần, ưu tiên bố cục responsive, nội dung có cấu trúc ngữ nghĩa và không cần máy chủ ứng dụng hay bước biên dịch.

## Chức năng

- Hiển thị phần giới thiệu, vai trò nghề nghiệp và ảnh đại diện.
- Điều hướng đến các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Trình bày danh sách kỹ năng và các dự án mẫu.
- Cung cấp liên kết liên hệ qua email, GitHub và LinkedIn.
- Tương thích với màn hình điện thoại, máy tính bảng và máy tính để bàn.

Các dự án, kỹ năng và đường dẫn hiện có trong trang là nội dung minh họa. Hãy cập nhật theo thông tin thực tế trước khi sử dụng portfolio chính thức.

## Công nghệ

- HTML5: cấu trúc và nội dung trang.
- CSS3: giao diện responsive, Flexbox, CSS Grid, custom properties và media queries.
- Docker tùy chọn: phục vụ trang bằng Nginx trong container.

## Yêu cầu môi trường

- Một trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Để mở trực tiếp: không cần cài thêm công cụ.
- Để chạy máy chủ cục bộ: Python 3 (hoặc một máy chủ web tĩnh tương đương).
- Để chạy bằng Docker: Docker Engine hoặc Docker Desktop đang hoạt động.
- Không yêu cầu Node.js, npm, cơ sở dữ liệu, API key hay bước build.

## Cài đặt

Tải hoặc sao chép mã nguồn về máy, sau đó mở terminal tại thư mục dự án `CV-main`. Nếu dự án được lấy từ Git, dùng URL kho mã nguồn của bạn thay cho `<URL-kho-ma-nguon>`:

```bash
git clone <URL-kho-ma-nguon>
cd CV-main
```

Nếu đã tải file ZIP, giải nén rồi mở terminal tại thư mục vừa giải nén. Không cần cài đặt các gói phụ thuộc.

## Cấu hình và tùy chỉnh

Không có file cấu hình môi trường hoặc biến `.env`. Chỉnh sửa trực tiếp nội dung trong `index.html`, bao gồm tên, mô tả, kỹ năng, dự án, email và liên kết mạng xã hội. Cập nhật các thẻ `title`, `description` và `author` trong phần `<head>` nếu thay đổi chủ sở hữu portfolio.

CSS và các biến màu, phông chữ, khoảng cách nằm trong `assets/css/styles.css`. Ảnh đại diện hiện được tham chiếu tại `assets/img/truong con.jfif`; nếu thay ảnh, cập nhật cả đường dẫn `src` tương ứng trong HTML. Giữ nguyên đường dẫn tương đối hoặc sửa đường dẫn nếu bạn đổi vị trí tệp.

Các nút “Xem chi tiết” và một số liên kết hồ sơ hiện dùng `#` hoặc thông tin mẫu. Hãy thay bằng URL thật trước khi đưa trang lên Internet.

## Chạy thử

### Windows

Mở PowerShell tại thư mục dự án. Có thể mở trực tiếp trang bằng trình duyệt mặc định:

```powershell
Start-Process .\index.html
```

Hoặc chạy máy chủ tĩnh bằng Python Launcher:

```powershell
py -m http.server 8000
```

Truy cập <http://localhost:8000>. Dừng máy chủ bằng `Ctrl+C`. Nếu lệnh `py` không có, cài Python 3 và thử `python -m http.server 8000`.

### macOS

Mở Terminal, chuyển đến thư mục dự án và khởi động máy chủ:

```bash
cd /duong-dan/toi/CV-main
python3 -m http.server 8000
```

Truy cập <http://localhost:8000>. Dừng máy chủ bằng `Ctrl+C`.

### Linux

Mở Terminal, chuyển đến thư mục dự án và khởi động máy chủ:

```bash
cd /duong-dan/toi/CV-main
python3 -m http.server 8000
```

Truy cập <http://localhost:8000>. Dừng máy chủ bằng `Ctrl+C`. Nếu hệ thống chưa có Python 3, cài Python 3 bằng trình quản lý gói của bản phân phối Linux đang sử dụng.

### Docker (Windows, macOS và Linux)

Cài và khởi động Docker trước. Chạy lệnh tại thư mục gốc của dự án để mount mã nguồn chỉ đọc vào Nginx:

**PowerShell (Windows):**

```powershell
docker run --name cv-portfolio --rm -d -p 8080:80 --mount "type=bind,source=$($PWD.Path),target=/usr/share/nginx/html,readonly" nginx:alpine
```

**Terminal (macOS/Linux):**

```bash
docker run --name cv-portfolio --rm -d -p 8080:80 --mount "type=bind,source=$(pwd),target=/usr/share/nginx/html,readonly" nginx:alpine
```

Mở <http://localhost:8080> để xem trang. Dừng container bằng:

```bash
docker stop cv-portfolio
```

> Tùy chọn `--rm` sẽ tự xóa container sau khi dừng. Lệnh này không tạo image riêng và không thêm Dockerfile vào dự án.

## Thông tin liên hệ

Thông tin chủ sở hữu portfolio: **Phùng Hải Nam**. Các địa chỉ dưới đây đang là dữ liệu mẫu trong trang; thay bằng thông tin thật trong `index.html`:

- Email: `an.nguyen@example.com`
- GitHub: `github.com/nguyenvanan`
- LinkedIn: `linkedin.com/in/nguyenvanan`
