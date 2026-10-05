1. Phân tích lỗi
- `bookingReservation.priceKey` sai vì JavaScript sẽ tìm thuộc tính có tên `priceKey`
- Trong object không có thuộc tính `priceKey` nên kết quả là `undefined`
- Khi lấy `undefined` để tính tiền sẽ làm kết quả thành `NaN`
- Sửa thành `bookingReservation[priceKey]` để lấy đúng `roomPrice`

Tại sao Dot Notation bị sai?

- `bookingReservation.priceKey` → tìm thuộc tính `priceKey`
- `bookingReservation[priceKey]` → lấy giá trị của biến `priceKey` là `"roomPrice"` rồi tìm thuộc tính `roomPrice`

2. Test Cases
-Test 1: `priceKey = "roomPrice"`
  - Sai: `undefined`, tổng tiền `NaN`
  - Đúng: giá phòng `1500000`, tổng tiền `1950000`

-Test 2: `checkInHour = 13`
  - Phụ thu: `0`
  - Tổng tiền: `1500000`