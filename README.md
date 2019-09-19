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

## Float: left/right

Đây là thuộc tính ta hay gặp nhất nếu ở thời điểm 2-3 năm về trước khi mọi framework css để sử dụng nó để chia layout.
Điều quan trong nhất khi sử dụng float: left là làm sao để tránh trường hợp height của phần tử cần đồng đều, khi xây dựng layout thuộc tính này thường đi kèm với thuộc tính clear: both.

Với ví dụ trước đó ta chỉ cần sử dụng float thay cho display: inline-block.
```

.sidebar {
  float: left;
}

or 

.main {
  float: right;
}

```

[Link pull](https://github.com/khacthe/Layout/pull/3)


## Display: flex

Có thể nói đây là thời của nó vì hầu như tất cả các framework css hiện tại đều đang sử dụng để dựng layout, các thuộc tính đi kèm giúp cho việc định vị các item trở nên dễ dàng hơn bao giờ hết. Phần tài liệu chi tiết bạn có thể tham khảo tại [Tai lieu](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

- Hạn chế của cách này là thiết kế cho lưới một chiều (chỉ có một dòng duy nhất) va không support các các trình duyệt cũ kĩ, đặc biệt là các sản phẩm do kẻ lắm chuyện microsoft làm ra.

- Struct
```
  .parent_element {
  	display: flex;

  	// ---something--- //
  }
```

## Display: grid

- Nếu như inline-block/float là quá khứ, flex là hiện tại thì grid là tương lai. Với grid nó bổ sung thêm phần hạn chế của flex đó chính là thiết kế cho lưới 2 chiều, Việc xây dựng layout trở nên linh hoạt hơn bao giờ hết.
Đương nhiên điểm hạn chế của của thuộc tính này vẫn sẽ không tránh khỏi việc không được support ở các trình duyệt cũ.

- Struct example

```
.parent {
    display: grid;
    grid-template-columns: 200px 200px 200px;
    grid-template-rows: 100px 100px;
}
```
- 
[Tai lieu tham khao](https://css-tricks.com/snippets/css/complete-guide-grid/)

## Note
- Ngoài các kiểu trên các bạn có thể sử dụng thêm các thuộc tính position để dựng layout, Việc lựa chọn thuộc tính nào phụ thuộc rất nhiều vào việc support của trình duyệt.

