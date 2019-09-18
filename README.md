# Layout

## Overview
Layouts có thể hiểu là cách dàn trang, cách phân bổ các tài liệu, nội dung, hình ảnh trên website sao cho hợp lý, đáp ứng được các mong muốn của người dùng truy cập web cũng như mang lại các trải nghiệm sử dụng web tốt nhất cho họ.
Ta thường định nghĩa tất cả mọi thứ trên website là box, vậy việc sắp xếp các box đó sao cho hợp lý chính là layout.
Việc lựa chọn thuộc tính xây dựng layout trong css có sự phát triển rất nhanh qua từng giai đoạn, và ngày càng tiện lợi hơn. Ta sẽ tìm hioeeur chút về hành trình của nó.

![Overview](https://github.com/khacthe/Layout/blob/master/531-298-.png)

## Display: inline-block
- Đây có thể nói là thuộc tính đầu tiên bắt đầu cho quá trình xây dựng layout, điểm ưu việt của thuộc tính này đó chính là hỗ trợ ở mọi trình duyệt.

Giả sử ta có layout html:
```
<body>
  <div class="sidebar">Sidebar</div>
  <div class="main">Main content</div>
</body>

```
ở đây ta chỉ cần thêm thuộc tính inline-block dòngvào sidebar và main là có được layout trên 1 dòng.
```
.sidebar,
.main {
   display: inline-block;
}

```

![Inline-block](https://github.com/khacthe/Layout/blob/master/display_inline.png)

[Link pull](https://github.com/khacthe/Layout/pull/2)
