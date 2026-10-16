# Đăng bài qua trình duyệt

Agent dùng giao diện đăng bài chính thức của từng nền tảng trong phiên trình duyệt đã đăng nhập: Facebook Page, LinkedIn Company Page, TikTok hoặc CMS của blog. Không cần nền tảng trung gian trả phí. Đây là thao tác có người giám sát; Agent không cam kết chạy nền hoặc tự đăng định kỳ khi người dùng không có mặt.

## Quy trình cho từng bài

1. Chọn đúng một dòng trong `content_calendar.csv`; xác nhận nội dung, kênh, tài khoản/trang đích, media, hành động (đăng ngay hay lên lịch) và thời gian. Không suy đoán trang cá nhân hay trang công ty.
2. Dùng phiên browser hiện có đã đăng nhập. Mở composer chính thức của đúng Page/Company Page; với blog dùng CMS. Không lấy hoặc sao chép cookie, không yêu cầu người dùng gửi mật khẩu.
3. Điền một bài, kiểm tra danh tính trang, nội dung, ảnh/video, link, định dạng xem trước và giờ đăng. Lưu nháp nếu người dùng yêu cầu.
4. Sau khi xem preview, xác định người dùng đã chấp thuận rõ đúng nội dung, trang đích và hành động chưa. Nếu đã có chấp thuận cụ thể và preview khớp, không hỏi lại. Nếu chưa có, hoặc nội dung/tài khoản/media/thời gian trong preview khác điều đã duyệt, dừng trước nút cuối và xin duyệt cho phiên bản/hành động đang hiển thị.
5. Chỉ sau khi đủ chấp thuận, chuyển trạng thái sang `approved` và thực hiện đúng hành động đã duyệt. Không tự đổi từ đăng ngay sang lên lịch hoặc ngược lại.
6. Cập nhật `drafted`, `scheduled` hoặc `published` dựa trên xác nhận nhìn thấy trong giao diện. Lưu permalink/xác nhận trong phần bàn giao. Nếu trạng thái không rõ hoặc lỗi, đánh dấu `blocked`, không thử lại mù quáng.

## Yêu cầu và giới hạn theo kênh

- **Facebook/LinkedIn:** chọn đúng Page hoặc Company Page mà người dùng chỉ định; không đăng lên profile cá nhân thay thế.
- **TikTok:** cần video đã dựng, không chỉ có kịch bản. Điền caption/hashtag, kiểm tra video, quyền riêng tư, disclosure và nhạc trong preview trước khi đăng.
- **Blog:** dùng CMS đã đăng nhập, điền các trường SEO có sẵn và kiểm tra URL/slug, ảnh đại diện, preview trước khi xuất bản.
- Lên lịch trong nền tảng nếu composer có chức năng này. Nếu không có, đề xuất người dùng đăng thủ công vào thời điểm đã chọn; không giả vờ rằng Agent sẽ tự thức dậy để đăng.

Không vượt qua MFA, CAPTCHA, bước bảo mật hoặc giới hạn tự động hóa của nền tảng; khi chúng xuất hiện, dừng và để chủ tài khoản xử lý. Không chấp nhận điều khoản pháp lý hoặc cấp quyền ứng dụng mở rộng thay người dùng. Giao diện và chức năng có thể thay đổi; kiểm tra đúng composer và preview tại thời điểm thao tác.
