# 📘 HƯỚNG DẪN TOÀN BỘ CÔNG THỨC EXCEL (TỪ CƠ BẢN → NÂNG CAO)

> Dành cho IT, sinh viên, dân văn phòng – học từ gốc, có ví dụ & cách dùng chi tiết.

---

## 📌 1. NHÓM CÔNG THỨC CƠ BẢN

> Ví dụ chung: giả sử bạn có bảng dữ liệu sau

| A (Số liệu) | B (Giá trị) |
|------------|-------------|
| 1 | 10 |
| 2 | 20 |
| 3 | 30 |
| 4 | 40 |
| 5 | 50 |

### 1.1. SUM – Tính tổng

**Bảng ví dụ:**

| Ô | Giá trị |
|---|--------|
| A1 | 10 |
| A2 | 20 |
| A3 | 30 |

```excel
=SUM(A1:A3)
```
➡ Kết quả: **60**
```excel
=SUM(A1:A10)
```
➡ Cộng tất cả giá trị từ A1 đến A10

---

### 1.2. AVERAGE – Tính trung bình

**Bảng ví dụ:**

| A | |
|---|---|
| 10 | |
| 20 | |
| 30 | |

```excel
=AVERAGE(A1:A3)
```
➡ Kết quả: **20**
```excel
=AVERAGE(B1:B10)
```
➡ Lấy giá trị trung bình

---

### 1.3. MIN / MAX – Giá trị nhỏ nhất / lớn nhất
```excel
=MIN(C1:C10)
=MAX(C1:C10)
```

---

### 1.4. COUNT / COUNTA / COUNTBLANK
```excel
=COUNT(A1:A10)      ' Đếm số
=COUNTA(A1:A10)     ' Đếm ô có dữ liệu
=COUNTBLANK(A1:A10) ' Đếm ô trống
```

---

## 📌 2. NHÓM ĐIỀU KIỆN (LOGIC)

### 2.1. IF – Điều kiện

**Bảng ví dụ:**

| A (Điểm) |
|---------|
| 7 |

```excel
=IF(A1>=5,"Đạt","Rớt")
```
➡ Kết quả: **Đạt**
```excel
=IF(A1>=5,"Đạt","Rớt")
```

---

### 2.2. IF lồng nhau
```excel
=IF(A1>=8,"Giỏi",IF(A1>=6,"Khá","Trung bình"))
```

---

### 2.3. AND / OR / NOT
```excel
=IF(AND(A1>=5,B1>=5),"Đạt","Rớt")
=IF(OR(A1>=9,B1>=9),"Giỏi","Bình thường")
```

---

## 📌 3. NHÓM TÌM KIẾM – TRA CỨU

### 3.1. VLOOKUP (CỔ ĐIỂN)

**Bảng dữ liệu:**

| A (Mã SV) | B (Tên) |
|----------|---------|
| SV01 | An |
| SV02 | Bình |
| SV03 | Chi |

**Ô cần tra:** `A5 = SV02`

```excel
=VLOOKUP(A5,A1:B3,2,FALSE)
```
➡ Kết quả: **Bình**
```excel
=VLOOKUP(A2,A:B,2,FALSE)
```
❌ Hạn chế: chỉ tìm từ trái sang phải

---

### 3.2. HLOOKUP
```excel
=HLOOKUP(A1,A1:D5,2,FALSE)
```

---

### 3.3. XLOOKUP (KHUYÊN DÙNG)

**Bảng dữ liệu:**

| A (ID) | B (Lương) |
|-------|-----------|
| 1 | 8,000 |
| 2 | 10,000 |
| 3 | 12,000 |

**Ô tra:** `A5 = 3`

```excel
=XLOOKUP(A5,A1:A3,B1:B3,"Không có")
```
➡ Kết quả: **12,000**
```excel
=XLOOKUP(A2,A:A,B:B,"Không tìm thấy")
```
✅ Thay thế VLOOKUP + HLOOKUP

---

### 3.4. INDEX + MATCH (CHUẨN IT)
```excel
=INDEX(B:B, MATCH(A2, A:A, 0))
```

---

## 📌 4. NHÓM XỬ LÝ CHUỖI (TEXT)

### 4.1. LEFT / RIGHT / MID

**Bảng ví dụ:**

| A (Chuỗi) |
|-----------|
| IT-PHONG-01 |

```excel
=LEFT(A1,2)   ' IT
=RIGHT(A1,2)  ' 01
=MID(A1,4,5)  ' PHONG
```
```excel
=LEFT(A1,4)
=RIGHT(A1,2)
=MID(A1,2,5)
```

---

### 4.2. LEN – Độ dài chuỗi
```excel
=LEN(A1)
```

---

### 4.3. TRIM – Xóa khoảng trắng
```excel
=TRIM(A1)
```

---

### 4.4. CONCAT / TEXTJOIN
```excel
=CONCAT(A1," ",B1)
=TEXTJOIN(", ",TRUE,A1:A5)
```

---

## 📌 5. NHÓM NGÀY GIỜ

### 5.1. TODAY / NOW

```excel
=TODAY()  ' 2025-12-16
=NOW()    ' 2025-12-16 21:00
```
```excel
=TODAY()
=NOW()
```

---

### 5.2. YEAR / MONTH / DAY
```excel
=YEAR(A1)
=MONTH(A1)
=DAY(A1)
```

---

### 5.3. DATEDIF – Tính số ngày/tháng/năm
```excel
=DATEDIF(A1,B1,"d")
```

---

## 📌 6. NHÓM TOÁN HỌC

### 6.1. ROUND / ROUNDUP / ROUNDDOWN
```excel
=ROUND(A1,2)
```

---

### 6.2. ABS / MOD / POWER / SQRT
```excel
=ABS(A1)
=MOD(A1,3)
=POWER(A1,2)
=SQRT(A1)
```

---

## 📌 7. NHÓM THỐNG KÊ

**Bảng ví dụ:**

| A (Điểm) | B (Lớp) |
|---------|--------|
| 4 | A |
| 6 | A |
| 8 | B |
| 9 | B |

```excel
=COUNTIF(A1:A4,">5")      ' KQ: 3
=SUMIF(A1:A4,">5",A1:A4) ' KQ: 23
=AVERAGEIF(A1:A4,">5")  ' KQ: 7.67
```

---

## 📌 8. NHÓM XỬ LÝ LỖI

```excel
=IFERROR(A1/B1,0)
=ISERROR(A1)
=ISBLANK(A1)
```

---

## 📌 9. NHÓM NÂNG CAO (EXCEL HIỆN ĐẠI)

**Bảng ví dụ:**

| A (Tên) | B (Điểm) |
|--------|----------|
| An | 4 |
| Bình | 7 |
| Chi | 9 |

### 9.1. FILTER
```excel
=FILTER(A1:C10, B1:B10>5)
```

---

### 9.2. SORT / SORTBY
```excel
=SORT(A1:B10,2,-1)
```

---

### 9.3. UNIQUE
```excel
=UNIQUE(A1:A20)
```

---

### 9.4. SEQUENCE
```excel
=SEQUENCE(10)
```

---

## 📌 10. COMBO THỰC TẾ (RẤT HAY DÙNG)

```excel
=IFERROR(XLOOKUP(A2,A:A,B:B),"Không có")
```

```excel
=TEXTJOIN(" - ",TRUE,UNIQUE(A1:A10))
```

---

## 📌 11. GỢI Ý CÁCH HỌC NHANH

✅ Học theo nhóm công thức
✅ Thực hành bảng điểm, bảng lương
✅ Kết hợp Power Query + Pivot Table

---

## 📌 12. ĐỀ XUẤT TÊN REPO GITHUB

- `excel-formula-master`
- `excel-cheatsheet-md`
- `excel-for-it`
- `excel-complete-guide`

---

✍️ Tác giả: Phong  
📂 Định dạng: Markdown (.md)

