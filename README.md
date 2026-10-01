# Lộ trình học tiếng Anh

Các trang tự học tiếng Anh. Part 1 và Part 2 mỗi ngày 20 phút; *Mấy phút cho mình* là bản
thử nhẹ hơn, 3–12 phút tuỳ tâm trạng.

| Trang | Nội dung |
|---|---|
| [`index.html`](index.html) | **Part 1 — giao tiếp hằng ngày** (tháng 1–12): checklist 20 phút theo thứ, hẹn giờ từng bước, 24 điểm phát âm, 120 câu nền, lịch từng ngày, đo tiến bộ 2 tuần/lần |
| [`part-2.html`](part-2.html) | **Part 2 — tiếng Anh ngành dược** (tháng 13–24): cổng điều kiện đầu vào, 4 quý, 60 câu chuyên ngành, đo bằng bài tư vấn bệnh nhân |
| [`may-phut.html`](may-phut.html) | **Mấy phút cho mình — bản thử cho mẹ bỉm**: chọn tâm trạng, 5 câu "giờ đi ngủ", nghe tự chạy, game tai thính + ghép hình, một câu dùng ngay với bé; cách đọc bằng trọng âm + âm cuối, không phiên âm chữ Việt |

## Dùng thế nào

Mở trang, tick việc đã làm. Tiến độ lưu **trong trình duyệt của chính thiết bị đó**
(`localStorage`) — không có máy chủ, không gửi dữ liệu đi đâu.

Vì vậy: chọn **một** thiết bị để tick, và mỗi tháng bấm *Sao chép dữ liệu* trong tab
cuối rồi dán vào ghi chú để giữ bản dự phòng.

Giọng đọc dùng giọng có sẵn của trình duyệt: mở bằng Chrome hoặc Safari, không mở trong
khung xem của Zalo/Messenger.

## Sinh lại file

Các file HTML ở đây được sinh tự động từ bản nguồn bằng `make_standalone.py` — bản
nguồn không có `doctype`/`head` vì nó dùng cho một nền tảng khác tự bọc khung. Script
dựng lại khung đó và đổi liên kết giữa hai trang sang đường dẫn tương đối.

```
py -3 make_standalone.py english-tracker.html  site/index.html
py -3 make_standalone.py pharmacy-english.html site/part-2.html
```

`may-phut.html` được bọc khung theo cùng cách (thêm `doctype`, `charset`, `viewport`).
