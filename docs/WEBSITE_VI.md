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

## Cập nhật giao diện tương tác (03/11/2026)

- Bổ sung **Lắp ráp** tại #lap-rap với 6 bước từ chọn bo Waveshare 1.75C, công cụ ESP-IDF, sao lưu Flash, nạp firmware, ghép đôi điện thoại đến kiểm tra định vị. Mục này tóm tắt [hướng dẫn Waveshare DIY](WAVESHARE_DIY_GUIDE.md), không thay thế chỉ dẫn an toàn và các thông số kiểm chứng trong tài liệu gốc.
- Khi chọn **↱ Dẫn đường**, màn hình tròn minh họa tuyến đường có chuyển động CSS và khoảng cách được cập nhật định kỳ bằng JavaScript. Có nút bắt đầu/dừng; chuyển chế độ sẽ dừng mô phỏng. Tôn trọng thiết lập giảm chuyển động của hệ điều hành.
- Mục **Âm nhạc** hiển thị bài **Chẳng cần diễm son** và nút mở khung Zing MP3 tại liên kết nhúng chính thức dự kiến: https://zingmp3.vn/embed/song/65A3tmuG8W7c ; khung chỉ được tạo khi người dùng bấm mở, không tự phát. Có liên kết nghe trực tiếp: https://zingmp3.vn/bai-hat/Chang-Can-Diem-Son/65A3tmuG8W7c.html. Khả năng tải và phát phụ thuộc Zing MP3, chính sách nhúng và trình duyệt; không đưa bản ghi âm vào repository.
- Footer hiển thị đúng nội dung: **Long Ngo phát triển, Dựa trên dự án Glimpse. © 2026 MotoMap**. Nghĩa vụ giấy phép, ghi nhận công lao và hạn chế sử dụng vẫn được duy trì trong LICENSE.md, NOTICE, LICENSES và phần FAQ.

## Giới hạn kỹ thuật và an toàn

- Phần cứng tham khảo hiện tại là Waveshare ESP32-S3-Touch-AMOLED-1.75C, màn hình 1,75 inch/466×466.
- Điện thoại đảm nhiệm định vị, tìm kiếm, tính lộ trình; màn hình tròn hiển thị dữ liệu truyền qua Bluetooth.
- Lưu bản đồ nền không đồng nghĩa với điều hướng hoàn toàn không có Internet.
- Quy tắc hạn chế xe máy, dữ liệu tốc độ giới hạn và tính năng CarPlay chưa được bảo đảm.
- **Không chạm điện thoại hay điều chỉnh lộ trình khi xe đang di chuyển.** Tuân thủ luật và biển báo.

## Tác giả và quyền sử dụng

Ý tưởng Glimpse và các thành phần kế thừa của moto-gps-waveshare ghi nhận Maler X; phiên bản MotoMap là giao diện tiếng Việt/phần mở rộng trên repository này. Giữ nguyên [LICENSE.md](../LICENSE.md), [NOTICE](../NOTICE) và [LICENSES](../LICENSES). Không được hiểu website mới đồng nghĩa với cấp quyền thương mại hóa các thành phần của dự án gốc.

Dữ liệu nền dự án gốc tham chiếu OpenStreetMap, Protomaps và dịch vụ bản đồ của bên thứ ba. Sơ đồ trên website này được vẽ thủ công để minh họa, không gọi các dịch vụ đó.
