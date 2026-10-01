# Lộ trình học tiếng Anh

Các trang tự học tiếng Anh. Part 1 và Part 2 mỗi ngày 20 phút; *Mấy phút cho mình* là bản
nhẹ hơn, 3–10 phút tuỳ tâm trạng.

| Trang | Nội dung |
|---|---|
| [`index.html`](index.html) | **Part 1 — giao tiếp hằng ngày** (tháng 1–12): checklist 20 phút theo thứ, hẹn giờ từng bước, 24 điểm phát âm, 120 câu nền, lịch từng ngày, đo tiến bộ 2 tuần/lần |
| [`part-2.html`](part-2.html) | **Part 2 — tiếng Anh ngành dược** (tháng 13–24): cổng điều kiện đầu vào, 4 quý, 60 câu chuyên ngành, đo bằng bài tư vấn bệnh nhân |
| [`may-phut.html`](may-phut.html) | **Mấy phút cho mình — cho mẹ bỉm**: lộ trình 20 bài theo mục lục sách *Gia đình song ngữ – Hoạt động tại nhà* (câu tự viết, không chép sách); đã có Bài 1–3 và 13. Chọn tâm trạng; nghe tự chạy, hội thoại mẹ–con hai giọng, tai thính, ghép hình, dùng ngay, thử thách 30 giây; Tập nói riêng có chấm từng từ; phiên âm IPA giọng Mỹ + cách đọc nối âm, không phiên âm chữ Việt |
| `audio/*.js` | Giọng đọc của từng bài (giọng AI thu sẵn), `may-phut.html` chỉ tải bài đang mở |

## Dùng thế nào

Mở trang, tick việc đã làm. Tiến độ lưu **trong trình duyệt của chính thiết bị đó**
(`localStorage`) — không có máy chủ, không gửi dữ liệu đi đâu.

Vì vậy: chọn **một** thiết bị để tick, và mỗi tháng bấm *Sao chép dữ liệu* trong tab
cuối rồi dán vào ghi chú để giữ bản dự phòng.

Part 1/Part 2 dùng giọng có sẵn của trình duyệt: mở bằng Chrome hoặc Safari, không mở trong
khung xem của Zalo/Messenger. *Mấy phút cho mình* có giọng thu sẵn nên mở ở đâu cũng nghe được;
riêng nút 🎤 Tập nói cần Chrome (Android) hoặc Safari (iPhone).

## Sinh lại file

Các file HTML ở đây được sinh tự động từ bản nguồn bằng `make_standalone.py` — bản
nguồn không có `doctype`/`head` vì nó dùng cho một nền tảng khác tự bọc khung. Script
dựng lại khung đó và đổi liên kết giữa hai trang sang đường dẫn tương đối.

```
py -3 make_standalone.py english-tracker.html  site/index.html
py -3 make_standalone.py pharmacy-english.html site/part-2.html
```

`may-phut.html` và `audio/*.js` sinh từ `lessons.json` bằng `gen_ipa.py` → `build.js extract` →
`tts.py` → `build.js inline` (bản có `doctype` là `may-phut.site.html`).
