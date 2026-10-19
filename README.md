# CNTT1-nh-p-m-n-c-ng-ngh-th-ng-tin-Session11_Ex08
### 1. Phân tích lỗi

| Vị trí | Lỗi vi phạm | Hậu quả AutoFilter |
| --- | --- | --- |
| **A1:E4** | Tiêu đề báo cáo đè trên Header, có dòng trống | Nhận nhầm Hàng 1 làm Header thay vì Hàng 5. |
| **Hàng 8** | Hàng trống ngắt giữa bảng | Bị dừng quét, bỏ qua dữ liệu từ Hàng 9 trở đi. |
| **Hàng 9** | Dòng tổng kết chèn ngang bảng | Tính gộp dòng tổng vào dữ liệu, làm sai kết quả. |
| **Ô B7** | `Trần Thị Bình  ` (thừa khoảng trắng) | Bị bỏ sót do so sánh chuỗi sai khác (`"A"` $\neq$ `"A "`). |

---

### 2. Bảng dữ liệu chuẩn

```text
[A1] TỔNG SỐ CNTT: =COUNTIF(C4:C, "CNTT")

+-----+---------------+-------------+----------------+------------+
| STT | Họ và Tên     | Khoa / Viện | Điểm Xét Duyệt | Trạng Thái |  <-- Header
+-----+---------------+-------------+----------------+------------+
| 1   | Nguyễn Văn An | CNTT        | 8.5            | Đã duyệt   |
| 2   | Trần Thị Bình | CNTT        | 7.9            | Chờ duyệt  |
| 3   | Lê Minh Châu  | Điện tử     | 8.2            | Đã duyệt   |
+-----+---------------+-------------+----------------+------------+

```

---

### 3. Sửa dữ liệu & Thao tác lọc

* **Xóa khoảng trắng:** Dùng `=TRIM(B4)` ở cột phụ $\rightarrow$ Copy $\rightarrow$ Paste Value đè lại cột B.
* **Thao tác lọc:**
1. Bấm **`Ctrl + Shift + L`** bật Filter.
2. Cột **Khoa / Viện**: Chọn **CNTT**.
3. Cột **Điểm Xét Duyệt**: Chọn *Filter by condition* $\rightarrow$ *$\ge$ 8.0* $\rightarrow$ **OK**.
