# BÀI LÀM – THI THỬ HACKATHON 02 (GAMEZONE)

- **Họ tên:** Hoa Việt Hoàng
- **Lớp:** CNTT3
- **Link repository:** https://github.com/hoaviethoang2002-lab/BTTH_CNTT3_Hoa-Viet-Hoang_26-10-2026.git
- **Hệ điều hành (Windows/macOS):** Windows

## 4.2. Thao tác CLI

### Các lệnh đã chạy

```shell
pwd
ls -Force -Recurse
mv .\cap-nhat.txt .\docs
mv .\logo-gamezone.PNG .\media
cp .\media\logo-gamezone.PNG .\backup
rm .\temp_207.tmp
cd .\logs
ls -Force
cd..
```

### Kết quả liệt kê toàn bộ dự án

```text
Directory: C:\Users\ADMIN\Downloads\de-on-tap-game\starter-kit\gamezone-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/26/2026   1:23 PM                backup
d-----        10/26/2026   1:17 PM                data
d-----        10/26/2026   1:21 PM                docs
d-----        10/26/2026   1:29 PM                logs
d-----        10/26/2026   1:22 PM                media
-a----        10/26/2026   1:10 PM             70 .env
-a----        10/26/2026   1:10 PM           1437 bai_lam.md


    Directory: C:\Users\ADMIN\Downloads\de-on-tap-game\starter-kit\gamezone-website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM           8542 logo-gamezone.PNG


    Directory: C:\Users\ADMIN\Downloads\de-on-tap-game\starter-kit\gamezone-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM           5814 giao-dich-thang-11.xlsx


    Directory: C:\Users\ADMIN\Downloads\de-on-tap-game\starter-kit\gamezone-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM             61 cap-nhat.txt


    Directory: C:\Users\ADMIN\Downloads\de-on-tap-game\starter-kit\gamezone-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:29 PM            858 

    Directory: C:\Users\ADMIN\Downloads\de-on-tap-game\starter-kit\gamezone-website\media


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/26/2026   1:10 PM           8542 logo-gamezone.PNG
```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
Get-ChildItem .\logs\game.log | Select-String "error" > .\logs\daily_report.txt
Get-Content .\logs\daily_report.txt
```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
logs\game.log:2:2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
logs\game.log:4:2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
```

## 4.4. README.md

> Chấm trực tiếp trên `README.md` ở gốc dự án.

- [x] Heading 1
- [x] Mô tả in đậm + in nghiêng
- [x] Bảng `Thư mục | Nội dung` (≥3 dòng)
- [x] Code block lệnh liệt kê
- [x] Task list (≥2 việc, ≥1 đã xong)
- [x] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report

### Lệnh chạy

```shell
..\auto_report_khung.ps1
Get-Content .\logs\auto_report.txt
```

### Nội dung file logs/auto_report.txt

```text
=== BAO CAO LOI GAMEZONE ===

2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:12:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:39:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:42:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:51:15 [ERROR] Loi luu tien trinh choi
```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
(Get-ChildItem .\logs\game.log | Select-String "error").Count
```

### Kết quả đếm

```text
6
```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
"=== TONG HOP LOG GAMEZONE ===">.\logs\tong_hop.txt
Get-ChildItem .\logs\game.log | Select-String "WARNING" >> .\logs\tong_hop.txt
(Get-ChildItem .\logs\game.log | Select-String "error").Count >> .\logs\tong_hop.txt
Get-Content .\logs\tong_hop.txt
```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG GAMEZONE ===

logs\game.log:19:2025-11-05 08:54:15 [WARNING] May chu qua tai CPU 90%


6

```

## 4.8. Excel

> Chấm trực tiếp trên file `data/giao_dich_thang_11.xlsx`.
