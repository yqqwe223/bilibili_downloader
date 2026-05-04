# 🎬 Công Cụ Phân Tích Video Từ Bilibili

> Công cụ trích xuất nội dung video từ Bilibili nhẹ, nhanh và đa năng (Phiên bản học tập & nghiên cứu)

[🌐 Dùng thử trực tuyến](https://twittervideodownloaderx.com/bilibili_downloader_vi) • [📝 Hướng dẫn sử dụng](#-hướng-dẫn-sử-dụng) • [❓ Câu hỏi thường gặp](#-câu-hỏi-thường-gặp)

---

## 📋 Giới thiệu dự án

Dự án này là công cụ phân tích video dựa trên nền web, hỗ trợ trích xuất an toàn siêu dữ liệu tài nguyên media từ các video công khai trên nền tảng Bilibili (哔哩哔哩), đồng thời cung cấp tùy chọn chuyển đổi và lưu trữ cục bộ dưới nhiều định dạng khác nhau. Không cần cài đặt phần mềm máy khách, không yêu cầu đăng ký tài khoản, sử dụng ngay lập tức qua trình duyệt.

> ⚠️ **Thông báo quan trọng**: Công cụ này chỉ dành cho mục đích học tập cá nhân, nghiên cứu kỹ thuật và sử dụng trong phạm vi hợp lý. Vui lòng tuân thủ [Quy ước cộng đồng Bilibili](https://www.bilibili.com/blackboard/protocol.html) cùng 《Luật Bản quyền Cộng hòa Nhân dân Trung Hoa》và các quy định pháp luật liên quan, tôn trọng thành quả lao động của người sáng tạo, không sử dụng nội dung đã tải xuống cho mục đích thương mại hoặc xâm phạm quyền lợi của người khác.

---

## ✨ Tính năng nổi bật

- 🔗 **Phân tích liên kết**: Hỗ trợ liên kết video/hoạt hình chuẩn của Bilibili, tự động nhận diện tập phim và tùy chọn độ phân giải
- 📥 **Xuất nhiều định dạng**:
  - Luồng video gốc (hỗ trợ độ phân giải công khai như 1080P/720P, v.v.)
  - Trích xuất âm thanh → Định dạng MP3 (tiện lợi cho việc nghe bài giảng/nhạc offline)
  - Đoạn video ngắn → Chuyển đổi thành ảnh động GIF (phù hợp làm biểu cảm/hướng dẫn giảng dạy)
- 🌍 **Giao diện đa ngôn ngữ**: Hỗ trợ tiếng Việt, tiếng Anh, tiếng Trung, tiếng Nhật và nhiều ngôn ngữ khác
- 📱 **Tương thích đa nền tảng**: Hoạt động tốt trên Chrome / Firefox / Safari / Edge, trải nghiệm mượt mà trên điện thoại và máy tính bảng
- 🔒 **Ưu tiên quyền riêng tư**: Không cần đăng nhập tài khoản B stand, không thu thập thông tin người dùng, quy trình phân tích hoàn toàn ẩn danh
- ⚡ **Xử lý tốc độ cao**: Hoàn thành phân tích trung bình trong vòng 5-10 giây, hỗ trợ yêu cầu song song và xử lý hàng loạt

---

## 🚀 Bắt đầu nhanh

### Sử dụng trực tuyến (khuyến nghị)
1. Truy cập [https://twittervideodownloaderx.com/bilibili_downloader_vi](https://twittervideodownloaderx.com/bilibili_downloader_vi)
2. Sao chép liên kết video mục tiêu (ví dụ: `https://www.bilibili.com/video/BV1xx411c7mD`)
3. Dán liên kết vào ô nhập liệu → Nhấp nút 「Phân tích」
4. Chọn độ phân giải và định dạng mong muốn → Lưu tệp theo hướng dẫn của trình duyệt

### Triển khai cục bộ (dành cho nhà phát triển)
```bash
# Clone repository
git clone https://github.com/your-repo/bili-video-parser.git

# Cài đặt dependencies
cd bili-video-parser && npm install

# Cấu hình biến môi trường (tùy chọn)
cp .env.example .env

# Khởi động server phát triển
npm run dev
```

> 💡 Lưu ý: Dự án sử dụng kiến trúc Node.js + Express. Vui lòng tham khảo tài liệu triển khai chi tiết tại `/docs/DEPLOY.md`

---

## 🛠 Công nghệ sử dụng

| Module | Công nghệ áp dụng |
|--------|------------------|
| Frontend | Vue 3 + TypeScript + Vite |
| Backend | Node.js + Express + Axios |
| Xử lý video | ffmpeg.wasm (chuyển đổi nhẹ trên frontend) |
| Proxy chuyển tiếp | Cloudflare Workers / Middleware tự xây dựng |
| Quốc tế hóa | vue-i18n + Gói ngôn ngữ JSON |

---

## 📚 Hướng dẫn sử dụng

### Quy trình thao tác cơ bản
```
1. Lấy liên kết video
   └─ Mở video mục tiêu trên Bilibili → Sao chép URL từ thanh địa chỉ trình duyệt

2. Gửi yêu cầu phân tích
   └─ Dán liên kết vào ô nhập của công cụ → Nhấp 「Bắt đầu phân tích」

3. Chọn cấu hình đầu ra
   ├─ 🎬 Tải video: Chọn độ phân giải (360P/720P/1080P, v.v. - các tùy chọn công khai)
   ├─ 🎵 Trích xuất âm thanh: Tạo tệp MP3 (phù hợp nghe bài giảng/nhạc offline)
   └─ 🎞 Tạo GIF: Cắt khoảng thời gian chỉ định để tạo ảnh động (khuyến nghị: ≤15 giây)

4. Lưu tệp
   └─ Tài nguyên mở trong tab mới → Nhấp chuột phải/menu → 「Lưu thành」
```

### Mẹo sử dụng trên điện thoại thông minh
- iOS Safari: Nút Chia sẻ → 「Lưu vào Tệp」
- Android Chrome: Nhấn giữ xem trước video → 「Tải video」
- Trường hợp video tự động phát: Nhấp `⋮` góc trên bên phải trình phát → Chọn 「Tải xuống」

---

## ❓ Câu hỏi thường gặp

**Hỏi: Tệp đã tải về được lưu ở đâu?**  
Đáp: Tệp sẽ được lưu vào thư mục tải xuống đã cài đặt trong trình duyệt. Bạn có thể kiểm tra hoặc thay đổi đường dẫn lưu trong phần cài đặt của trình duyệt.

**Hỏi: Có thể phân tích nội dung dành riêng cho thành viên hoặc cần đăng nhập không?**  
Đáp: Không. Công cụ này chỉ hỗ trợ các video được cài đặt ở chế độ công khai và tôn trọng cài đặt quyền truy cập của nội dung gốc.

**Hỏi: Chất lượng hình ảnh/âm thanh sau khi chuyển đổi có bị giảm không?**  
Đáp: Tải video sẽ giữ nguyên bitrate gốc của độ phân giải đã chọn. Định dạng MP3 sử dụng mã hóa tiêu chuẩn 128kbps. Định dạng GIF sẽ tối ưu hóa tốc độ khung hình theo thời lượng phát để cân bằng giữa kích thước tệp và độ mượt.

**Hỏi: Lịch sử tải xuống hoặc bộ nhớ đệm có được lưu trữ không?**  
Đáp: Không. Tất cả tài nguyên đều được truyền trực tiếp đến thiết bị người dùng qua proxy tạm thời, máy chủ không lưu trữ bất kỳ nội dung yêu cầu hoặc tệp media nào.

**Hỏi: Nếu phân tích thất bại thì phải làm sao?**  
Đáp: Vui lòng kiểm tra: ① Liên kết video công khai có hợp lệ không ② Môi trường mạng có ổn định không ③ Thử đổi trình duyệt khác và thử lại. Nếu vấn đề vẫn tiếp diễn, vui lòng báo cáo qua Issue bất cứ lúc nào.

---

## ⚖️ Tuân thủ quy định và Tuyên bố miễn trừ

- Công cụ này **không xâm nhập hoặc bypass bất kỳ biện pháp bảo vệ kỹ thuật nào** của nền tảng, chỉ thu thập siêu dữ liệu thông qua giao diện công khai
- Người dùng vui lòng tự xác nhận hành vi sử dụng của mình có phù hợp với quy định pháp luật địa phương và điều khoản sử dụng của nền tảng hay không
- Các trường hợp sử dụng được khuyến nghị: Lưu trữ học tập cá nhân, minh họa giáo dục, tài liệu tham khảo sản xuất nội dung... trong phạm vi sử dụng hợp lý (Fair Use)
- Nếu phát hiện nội dung có nghi ngờ xâm phạm quyền lợi, vui lòng liên hệ kênh chính thức của [Bilibili qua liên kết báo cáo bản quyền này](https://www.bilibili.com/blackboard/help.html#copyright)

---

## 🤝 Hướng dẫn đóng góp

Chúng tôi hoan nghênh việc gửi Pull Request và báo cáo Issue! Trước khi đóng góp, vui lòng đọc kỹ các tài liệu sau:
- [Quy chuẩn mã nguồn](/CONTRIBUTING.md)
- [Hướng dẫn dịch đa ngôn ngữ](/locales/README.md)
- [Yêu cầu bảo mật và tuân thủ](/SECURITY.md)

---

## 📄 Giấy phép

Dự án này được phát hành dưới [Giấy phép MIT](/LICENSE), có thể sử dụng miễn phí cho mục đích học tập và nghiên cứu. Trường hợp sử dụng thương mại, vui lòng rà soát kỹ các yêu cầu tuân thủ pháp luật.

---

> 🌟 Nếu công cụ này hữu ích với bạn, vui lòng ✨nhấn Star để ủng hộ! Sự ủng hộ của mọi người chính là động lực lớn nhất để chúng tôi duy trì và phát triển dự án~

*Cập nhật lần cuối: Tháng 5 năm 2026 | Phiên bản: v1.0.0*