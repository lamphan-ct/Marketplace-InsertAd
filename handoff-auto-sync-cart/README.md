# Handoff · Auto-sync cart (Tự động đồng bộ giỏ hàng) — đọc trước

Tickets: carousell/ct-technical-sdd #1941 · #1943 · #1944 · Design owner: Lâm Phan · 2026-11-17

## ⛔ Còn thiếu / đang chặn
1. **Copy "24/7"** (thẻ khách + bottom sheet trang shop): chưa ship cho tới khi BE xác nhận tần suất sync. Dùng copy dự phòng trong spec (Open Items B1).
2. **Lý do "Tạo không thành công"**: FE hiển thị nguyên văn text BE trả về; BE cần chốt error code + câu tiếng Việt (B2).


## Gói có gì
- `designspec-auto-sync-cart.md` — spec chính (5 screen: section crosspost, tab Bài đăng, tab Tin chuyên trang, thẻ chủ shop, thẻ khách + bottom sheet).
- `assets/` — icon giỏ hàng 3D (256×256, xuất @1x/@2x/@3x) và 4 banner (nên do server trả về).
- `assets/illustrations/` — minh hoạ bottom sheet trang shop đã render (iOS @1x–3x, Android mdpi→xxxhdpi, Web, master @4x + `manifest.json`). Canvas 359×236dp, bleed trên 12 / dưới 28 / ngang 24; đặt trên nền #F7F7F7.
- Prototype bấm được: không đóng gói offline. Mở canvas https://claude.ai/artifact/NbNTzi4sCeF1JbznzB2A2w → page *Auto InsertAd Crosspost* → **▶ Prototype hoàn chỉnh** (có bộ chọn trường hợp) và **▶ Prototype trang shop**. Animation đọc giá trị trong spec, so mắt với prototype.

## Ngoài phạm vi
- Chế độ **Chọn nhiều** để đăng nhiều tin lên Chợ Tốt (nút nổi, thanh đáy, tooltip) — đã bỏ khỏi spec.
- Giỏ hàng / hạng tin / voucher / thanh toán (Revenue #1942), banner "3 tin miễn phí" ở tab Tin chuyên trang.
- Desktop/Web.
