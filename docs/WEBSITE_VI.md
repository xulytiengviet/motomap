# MotoMap · Website tiếng Việt

Trang giới thiệu công khai cho repository [xulytiengviet/motomap](https://github.com/xulytiengviet/motomap), lấy cảm hứng từ cách trình bày của [Glimpse](https://maler.top/) (Maler X).

## Truy cập

- Website dự kiến: https://xulytiengviet.github.io/motomap/
- Mã nguồn website: [index.html](../index.html)
- Firmware/app gốc vẫn nằm trong thư mục platforms, shared, backend và hardware, không bị thay đổi bởi website.
- Website sử dụng HTML/CSS/JS thuần; không cần npm, Node.js, CDN hoặc khóa API.

## Bật GitHub Pages (làm một lần)

1. Mở **Settings → Pages** của repository.
2. Trong **Build and deployment → Source**, chọn **GitHub Actions**.
3. Mở **Actions → Deploy MotoMap Vietnamese website → Run workflow** nếu cần triển khai thủ công.
4. Sau khi workflow thành công, truy cập URL website ở trên. Có thể cần đợi GitHub cập nhật cấu hình/đường dẫn.

Tệp [.github/workflows/pages.yml](../.github/workflows/pages.yml) tự động kiểm tra cú pháp JavaScript, đóng gói duy nhất trang HTML, icon và ảnh giới thiệu, rồi triển khai mỗi khi index.html hoặc tài nguyên liên quan thay đổi trên nhánh main.

Nếu tổ chức/tài khoản chặn GitHub Actions hoặc Pages chưa được bật, thiết lập quyền trong repository trước. Không cần sửa thông tin DNS hay xây dựng backend cho riêng website.

## Nội dung và thao tác

- Màn hình tròn: Dẫn đường, Tốc độ, Hướng đi, Âm nhạc. Thao tác bằng nút hoặc phím mũi tên.
- Quy trình 3 bước: Ghép đôi, chọn lộ trình, bắt đầu dẫn đường.
- Điện thoại mẫu: Chọn 1 trong 3 tuyến, nhấn **Bắt đầu mô phỏng** để cập nhật màn hình.
- Các mục: Bản đồ & offline, tính năng, phần cứng, tài liệu DIY, hỏi đáp tìm theo từ khóa.

**Toàn bộ chỉ dẫn, số liệu tốc độ/tuyến đường và đồ họa đường phố trên website là dữ liệu giả lập.** Trang web không có khả năng định vị thực, lập lộ trình, tải bản đồ offline, kết nối BLE hoặc điều khiển ứng dụng nhạc. Các chức năng đó thuộc ứng dụng/firmware riêng và có thể vẫn đang được phát triển, kiểm thử, cấu hình.

## Giới hạn kỹ thuật và an toàn

- Phần cứng tham khảo hiện tại là Waveshare ESP32-S3-Touch-AMOLED-1.75C, màn hình 1,75 inch/466×466.
- Điện thoại đảm nhiệm định vị, tìm kiếm, tính lộ trình; màn hình tròn hiển thị dữ liệu truyền qua Bluetooth.
- Lưu bản đồ nền không đồng nghĩa với điều hướng hoàn toàn không có Internet.
- Quy tắc hạn chế xe máy, dữ liệu tốc độ giới hạn và tính năng CarPlay chưa được bảo đảm.
- **Không chạm điện thoại hay điều chỉnh lộ trình khi xe đang di chuyển.** Tuân thủ luật và biển báo.

## Tác giả và quyền sử dụng

Ý tưởng Glimpse và các thành phần kế thừa của moto-gps-waveshare ghi nhận Maler X; phiên bản MotoMap là giao diện tiếng Việt/phần mở rộng trên repository này. Giữ nguyên [LICENSE.md](../LICENSE.md), [NOTICE](../NOTICE) và [LICENSES](../LICENSES). Không được hiểu website mới đồng nghĩa với cấp quyền thương mại hóa các thành phần của dự án gốc.

Dữ liệu nền dự án gốc tham chiếu OpenStreetMap, Protomaps và dịch vụ bản đồ của bên thứ ba. Sơ đồ trên website này được vẽ thủ công để minh họa, không gọi các dịch vụ đó.
