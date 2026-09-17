# Lộ trình học tiếng Anh

Hai trang theo dõi việc tự học tiếng Anh, mỗi ngày 20 phút.

| Trang | Nội dung |
|---|---|
| [`index.html`](index.html) | **Part 1 — giao tiếp hằng ngày** (tháng 1–12): checklist 20 phút theo thứ, hẹn giờ từng bước, 24 điểm phát âm, 120 câu nền, lịch từng ngày, đo tiến bộ 2 tuần/lần |
| [`part-2.html`](part-2.html) | **Part 2 — tiếng Anh ngành dược** (tháng 13–24): cổng điều kiện đầu vào, 4 quý, 60 câu chuyên ngành, đo bằng bài tư vấn bệnh nhân |

## Dùng thế nào

Mở trang, tick việc đã làm. Tiến độ lưu **trong trình duyệt của chính thiết bị đó**
(`localStorage`) — không có máy chủ, không gửi dữ liệu đi đâu.

Vì vậy: chọn **một** thiết bị để tick, và mỗi tháng bấm *Sao chép dữ liệu* trong tab
cuối rồi dán vào ghi chú để giữ bản dự phòng.

## Sinh lại file

Hai file HTML ở đây được sinh tự động từ bản nguồn bằng `make_standalone.py` — bản
nguồn không có `doctype`/`head` vì nó dùng cho một nền tảng khác tự bọc khung. Script
dựng lại khung đó và đổi liên kết giữa hai trang sang đường dẫn tương đối.

```
py -3 make_standalone.py english-tracker.html  site/index.html
py -3 make_standalone.py pharmacy-english.html site/part-2.html
```
