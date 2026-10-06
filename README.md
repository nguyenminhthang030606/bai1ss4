
 1. Phân tích lỗi

Lỗi nằm ở vòng lặp:

```c
for (int i = 1; i < so_luong_ly; i++)
```

Điều kiện `i < so_luong_ly` làm vòng lặp không xử lý ly cuối cùng.

Ví dụ nhập `3` ly thì chương trình chỉ chạy với:

```text
i = 1
i = 2
```

Đến `i = 3` thì điều kiện `3 < 3` sai nên vòng lặp kết thúc.

 Cách sửa

Đổi:

```c
i < so_luong_ly
```

thành:

```c
i <= so_luong_ly
```

 2. Test Cases

| Trường hợp kiểm thử | Dữ liệu đầu vào | Kết quả sai thực tế | Kết quả đúng mong đợi |
|---|---|---|---|
| TC01 - 3 ly cùng Size S | 3 ly: S, S, S | 60.000 VNĐ | 90.000 VNĐ |
| TC02 - 3 ly khác Size | 3 ly: S, M, L | 66.000 VNĐ | 106.000 VNĐ |
