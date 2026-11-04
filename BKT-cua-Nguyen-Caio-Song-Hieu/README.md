# Portfolio CV - Nguyễn Cao Song Hiếu

Website portfolio cá nhân giới thiệu thông tin, kỹ năng, các dự án tiêu biểu và
cách liên hệ với Nguyễn Cao Song Hiếu. Giao diện được xây dựng theo hướng
responsive, ưu tiên thiết bị di động và có thể chạy trực tiếp bằng trình duyệt
hoặc phục vụ bằng một web server tĩnh.

## Mục lục

- [Mô tả dự án](#mô-tả-dự-án)
- [Chức năng](#chức-năng)
- [Công nghệ sử dụng](#công-nghệ-sử-dụng)
- [Cấu trúc thư mục](#cấu-trúc-thư-mục)
- [Yêu cầu môi trường](#yêu-cầu-môi-trường)
- [Cài đặt](#cài-đặt)
- [Cấu hình và tùy chỉnh](#cấu-hình-và-tùy-chỉnh)
- [Chạy thử](#chạy-thử)
  - [Windows](#windows)
  - [macOS](#macos)
  - [Linux](#linux)
  - [Docker](#docker)
- [Kiểm tra](#kiểm-tra)
- [Thông tin liên hệ](#thông-tin-liên-hệ)

## Mô tả dự án

Đây là trang CV/portfolio một trang (single-page), trình bày bằng tiếng Việt.
Khách truy cập có thể dùng thanh điều hướng để chuyển đến phần giới thiệu, kỹ
năng, dự án và liên hệ. Bố cục tự điều chỉnh theo kích thước màn hình.

Đây là website tĩnh: dự án không có máy chủ ứng dụng, cơ sở dữ liệu, API backend,
quy trình build hay package cần cài đặt. Các thẻ dự án hiện là nội dung giới
thiệu và liên kết tham khảo; chúng không đại diện cho các ứng dụng chạy bên
trong portfolio.

## Chức năng

- Giới thiệu cá nhân, vai trò và ảnh đại diện.
- Hiển thị các kỹ năng dưới dạng thẻ.
- Trình bày dự án bằng các thẻ có ảnh minh họa, mô tả, nhãn công nghệ và liên
  kết bên ngoài.
- Điều hướng đến các phần bằng liên kết neo trên cùng trang.
- Hiển thị thông tin email, GitHub và LinkedIn.
- Thiết kế responsive: một cột trên màn hình nhỏ, lưới hai cột từ 768 px và ba
  cột từ 1280 px.
- Hỗ trợ điều hướng bằng bàn phím, nhãn ngôn ngữ tiếng Việt và mô tả ảnh.

## Công nghệ sử dụng

- **HTML5:** cấu trúc ngữ nghĩa, nội dung và điều hướng của trang.
- **CSS3:** giao diện, Flexbox, CSS Grid, custom properties, hiệu ứng và
  responsive media queries.
- **Git và GitHub:** quản lý mã nguồn.
- **JavaScript:** không được dùng để vận hành trang hiện tại; JavaScript chỉ
  xuất hiện trong danh sách kỹ năng được giới thiệu trên portfolio.
- **Docker (tùy chọn):** dùng Nginx để phục vụ website tĩnh trong container.

## Cấu trúc thư mục

```text
.
├── index.html                 # Nội dung trang portfolio
├── README.md                  # Tài liệu dự án
└── assets/
    ├── css/
    │   └── styles.css         # Giao diện và responsive
    └── img/
        └── 1000016186.jpg     # Ảnh đại diện
```

## Yêu cầu môi trường

### Để xem trang

- Trình duyệt hiện đại có hỗ trợ HTML5 và CSS Grid, ví dụ Chrome, Edge,
  Firefox hoặc Safari.
- Không cần cài Node.js, npm, cơ sở dữ liệu hoặc backend.
- Kết nối Internet chỉ cần thiết để tải ảnh minh họa và mở các liên kết bên
  ngoài trong phần dự án.

### Để chạy web server cục bộ

- Python 3 (tùy chọn), hoặc một web server tĩnh tương đương.

### Để chạy bằng Docker

- Docker Engine/Desktop đang chạy.
- Kết nối Internet trong lần đầu chạy để tải image `nginx:alpine`.

## Cài đặt

Không có bước cài thư viện. Lấy mã nguồn bằng Git:

```bash
git clone https://github.com/hieu91877-ai/My-CV-CUABOMAY.git
cd My-CV-CUABOMAY
```

Nếu đã có mã nguồn trên máy, mở terminal tại thư mục chứa `index.html`.

## Cấu hình và tùy chỉnh

Website không có file `.env` hoặc cấu hình môi trường riêng. Chỉnh nội dung trực
tiếp trong `index.html`:

- **Tên, phần giới thiệu, kỹ năng và dự án:** sửa các nội dung tương ứng trong
  các section `about`, `skills` và `projects`.
- **Liên hệ:** thay email mẫu `hieu.nguyen@example.com`, URL GitHub và LinkedIn
  mẫu trong section `contact` bằng thông tin thật. Các liên kết `href="#"` cần
  được thay bằng URL hợp lệ.
- **Chân trang:** cập nhật tên đang hiển thị ở phần copyright nếu cần.
- **Ảnh đại diện:** thay `assets/img/1000016186.jpg` hoặc sửa thuộc tính `src`
  của ảnh trong `index.html`. Giữ đường dẫn tương đối hợp lệ để ảnh tải được.
- **Giao diện:** sửa các biến màu, font, khoảng cách và kích thước trong khối
  `:root` ở đầu `assets/css/styles.css`; các breakpoint responsive hiện tại là
  768 px và 1280 px.
- **Ảnh bên ngoài:** các ảnh minh họa dự án đang tải từ URL bên ngoài, vì vậy
  cần có Internet để hiển thị. Có thể tải ảnh về `assets/img/` rồi cập nhật
  đường dẫn trong HTML nếu muốn tự lưu trữ.

Lưu ý: nội dung liên hệ hiện tại có địa chỉ ví dụ và liên kết giữ chỗ. Hãy cập
nhật trước khi công bố trang.

## Chạy thử

Có thể mở trực tiếp `index.html` trong trình duyệt. Để mô phỏng việc phục vụ
website qua HTTP (khuyến nghị), chạy server từ thư mục dự án rồi truy cập
`http://localhost:8000`.

### Windows

Mở PowerShell tại thư mục dự án và chạy:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có, thử:

```powershell
python -m http.server 8000
```

Mở `http://localhost:8000` trong trình duyệt. Dừng server bằng `Ctrl+C`.

### macOS

Mở Terminal, chuyển đến thư mục dự án (thay đường dẫn ví dụ bằng vị trí thực tế)
rồi chạy:

```bash
cd "/duong-dan/toi/My-CV-CUABOMAY"
python3 -m http.server 8000
```

Mở `http://localhost:8000` trong trình duyệt. Dừng server bằng `Ctrl+C`.

### Linux

Mở terminal, chuyển đến thư mục dự án rồi chạy:

```bash
cd "/duong-dan/toi/My-CV-CUABOMAY"
python3 -m http.server 8000
```

Mở `http://localhost:8000` trong trình duyệt. Dừng server bằng `Ctrl+C`.

Nếu máy chưa cài Python 3, hãy cài Python bằng trình quản lý gói của bản phân
phối đang sử dụng hoặc mở trực tiếp `index.html` bằng trình duyệt.

### Docker

Không cần tạo Dockerfile: image Nginx chính thức sẽ phục vụ các file trong thư
mục dự án. Mở terminal tại thư mục chứa `index.html`, rồi chạy lệnh phù hợp.

**Windows PowerShell:**

```powershell
docker run --rm --name cv-portfolio -p 8080:80 --mount "type=bind,source=$((Get-Location).Path),target=/usr/share/nginx/html,readonly" nginx:alpine
```

**macOS / Linux:**

```bash
docker run --rm --name cv-portfolio -p 8080:80 \
  --mount "type=bind,source=$PWD,target=/usr/share/nginx/html,readonly" \
  nginx:alpine
```

Mở `http://localhost:8080`. Dừng container bằng `Ctrl+C`; tùy chọn `--rm` sẽ
xóa container sau khi dừng. Cổng `8080` trên máy được ánh xạ đến cổng `80` trong
container. Nếu cổng `8080` đang được sử dụng, thay số `8080` ở vế trái của
`-p`, ví dụ `-p 8081:80`, rồi truy cập cổng mới.

## Kiểm tra

Sau khi mở trang, kiểm tra các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ; thử
các liên kết điều hướng, xác nhận ảnh đại diện và CSS được tải, rồi thu nhỏ cửa
sổ hoặc dùng chế độ giả lập thiết bị để kiểm tra bố cục responsive.

Dự án hiện không có bộ kiểm thử tự động hoặc bước build.

## Thông tin liên hệ

Thông tin liên hệ được hiển thị trong section **Liên hệ** của `index.html`.
Email và URL hồ sơ trong phiên bản hiện tại là giá trị mẫu/giữ chỗ; vui lòng
thay bằng thông tin chính xác trước khi sử dụng hoặc chia sẻ website.