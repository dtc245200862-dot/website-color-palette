# [Thực hành] Sử dụng màu sắc trong trang web (Monochromatic Color Scheme)

## 🎯 Mục tiêu
- Luyện tập kỹ năng phối màu đơn tông (Monochromatic) trên trang web.
- Hiểu cách chọn một màu chủ đạo (Primary Color) và triển khai các cấp độ màu (Tiers) nhạt dần để áp dụng hài hòa cho từng khu vực giao diện: Banner, Button, Badge, Content Cards, Footer,...
- Ứng dụng màu trung tính (đen, trắng) làm nổi bật nội dung văn bản.

---

## 🎨 Bảng màu đơn tông chuẩn theo màu xanh Logo (#00ADEE)

Màu chủ đạo được lấy từ tâm của Logo Store: `#00ADEE` (Màu bậc 1). Bảng các cấp độ màu nhạt dần:

| Cấp độ (Tier) | Mã HEX | Ứng dụng trong giao diện | Ghi chú |
| :---: | :---: | :--- | :--- |
| **Bậc 1 (Base)** | `#00ADEE` | Logo, Nhãn ON SALE, Huy hiệu PREVIEW, Nút bấm CTA "Add to Cart", Submit | Màu chủ đạo nổi bật nhất |
| **Bậc 2** | `#00B2EF` | Hiệu ứng Hover nút bấm, Hover liên kết, Nút chuyển trang | Sắc độ đậm phụ trợ |
| **Bậc 3** | `#00B9F1` | Đường viền tab, Active state | Trung gian |
| **Bậc 4** | `#00BFF2` | Nền khối `#banner` | Màu nền nổi bật cho phần đầu trang |
| **Bậc 5** | `#33CCF4` | Phụ trợ chuyển sắc | |
| **Bậc 6** | `#5CD6F6` | Phụ trợ viền khối | |
| **Bậc 7** | `#8DD7F7` | Nền các thẻ xem trước nhạc (`#main .preview li a`) | Thay thế cho màu nền hồng ban đầu |
| **Bậc 8** | `#A9E1F9` | Viền ngăn cách (divider), dấu quote | Hỗ trợ phân cách nhẹ nhàng |
| **Bậc 9** | `#C6E9FA` | Nền phần chân trang (`footer`) | Tạo độ sáng sủa, thanh lịch |
| **Bậc 10** | `#E3F4FC` | Nền khối thông tin (`#info` newsletter/refund) | Tone nền cực nhạt, dịu mắt |

---

## 🛠️ Chi tiết các bước thực hiện theo đề bài

### Bước 1: Xác định màu chính
- Sử dụng màu xanh logo `#00ADEE` làm màu bậc 1.
- Xây dựng hệ thống biến CSS `:root` từ `--color-tier-1` đến `--color-tier-10`.

### Bước 2: Thay đổi màu nền Banner
- Chuyển `background` của `#banner` từ màu đỏ `#c33` sang màu bậc 4 `#00BFF2`.
- Chữ giữ màu trắng `#fff` có bóng đổ nhẹ để đảm bảo độ tương phản rõ ràng.

### Bước 3: Thay đổi màu nền phần ON SALE / PREVIEW
- Chuyển dải băng `.trans .on-sale` từ nền đỏ sang màu bậc 1 `#00ADEE`.
- Chuyển nhãn `.title` và hình tròn icon `.circle` của phần PREVIEW sang màu bậc 1 `#00ADEE`.

### Bước 4: Đổi màu nền phần nội dung Previews
- Chuyển màu nền khối nghe thử nhạc `#main .preview li a` từ màu hồng phấn `#fac7d2` sang màu bậc 7 `#8DD7F7`.
- Giữ màu chữ đen `#000000` để đảm bảo độ tương phản cao, dễ đọc trên nền xanh nhạt.

### Bước 5: Đổi màu nền Footer & Info
- Đổi màu nền thẻ `footer` thành màu bậc 9 `#C6E9FA` với chữ màu đen `#222`.
- Khối `#info` áp dụng màu bậc 10 `#E3F4FC` giúp toàn bộ bố cục sáng sủa và đồng bộ tông màu.

### Bước 6: Quy chuẩn màu chữ toàn trang
- Màu chữ tổng thể trang web được duy trì màu đen (`#000000` / `#222222`), loại bỏ các xung đột màu đỏ/hồng cũ.

### Bước 7: Chạy và kiểm tra kết quả
- Mở file `index.html` trên trình duyệt để kiểm tra toàn bộ giao diện sau khi phối lại màu.

### Bước 8: Mở rộng thêm các bảng màu đơn tông khác
Đã xây dựng thêm 2 bảng màu đơn sắc hoàn chỉnh để đáp ứng yêu cầu Bước 8:
1. **Emerald Green Monochromatic (`style-green.css`)**: Màu chủ đạo `#059669` -> Bậc 4 `#48BB78` -> Bậc 7 `#A7F3D0` -> Bậc 9 `#D1FAE5`.
2. **Purple Violet Monochromatic (`style-purple.css`)**: Màu chủ đạo `#7C3AED` -> Bậc 4 `#9F7AEA` -> Bậc 7 `#DDD6FE` -> Bậc 9 `#EDE9FE`.
3. Tích hợp thanh công cụ **Theme Switcher** ngay trên đầu trang để chuyển đổi qua lại nhanh chóng giữa các bảng màu.

---

## 💻 Cấu trúc thư mục dự án

```
website-color-palette/
├── index.html          # Trang giao diện chính tích hợp Theme Switcher
├── style.css           # Bảng màu đơn tông Xanh Dương chuẩn đề bài (#00ADEE)
├── style-green.css     # Bảng màu đơn tông Xanh Ngọc (Mở rộng Bước 8)
├── style-purple.css    # Bảng màu đơn tông Tím Violet (Mở rộng Bước 8)
├── README.md           # Hướng dẫn và báo cáo chi tiết
├── fonts/              # Bộ font pacifico, ptsans
└── images/             # Tài nguyên hình ảnh, logo xanh #00ADEE
```

---

## 🚀 Hướng dẫn chạy thử
1. Clone hoặc tải project về máy:
   ```bash
   git clone https://github.com/dtc245200862-dot/website-color-palette.git
   ```
2. Mở file `index.html` trực tiếp bằng trình duyệt Chrome/Edge/Firefox.
3. Click vào các nút trên thanh menu để trải nghiệm các bảng màu đơn tông khác nhau!
