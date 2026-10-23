# BÀI LÀM – THI THỬ HACKATHON 01

- **Mã đề:** Thi thử
- **Họ tên:** Đỗ Thành Chung
- **Lớp:** CNTT03
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):** Windows

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
 pwd
 ls -Force
 mv -Path ".\nhap_hang.txt" -Destination ".\docs\"
 mv -Path ".\logo_van_phong_pham.PNG" -Destination ".\media\"
  rm .\temp_131.tmp
  cd .\logs\
  Get-ChildItem
  cd..
 


```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
 Directory: C:\Users\Admin\Downloads\starter-kit(3)\starter-kit\van-phong-pham-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/23/2026   8:35 AM                backup
d-----        10/23/2026   8:37 AM                data
d-----        10/23/2026   8:45 AM                docs
d-----        10/23/2026   8:37 AM                logs
d-----        10/23/2026   8:46 AM                media
------        10/19/2026   9:41 AM             78 .env
-a----        10/19/2026  10:00 AM           2253 bai_lam.md

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
 Get-Content .\logs\shop.log | Select-String "ERROR"
 Get-Content .\logs\shop.log | Select-String "ERROR" > .\logs\daily_report.txt
  Get-Content .\logs\daily_report.txt -TotalCount 2


```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2025-10-28 08:24:28 [ERROR] Thanh toan bi tu choi
2025-10-28 08:30:28 [ERROR] Thanh toan bi tu choi

```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] Heading 1: tên dự án
- [ ] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [ ] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [ ] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [ ] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [ ] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
 .\auto_report.ps1


```

### Nội dung file logs/auto_report.txt

```text
Dang loc log..."
=== BAO CAO LOI ===
Hoan thanh!

```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
(Get-Content .\logs\shop.log | Select-String "ERROR").Count

```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
6

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
Get-Content .\logs\shop.log | Select-String "WARNING"
Get-Content .\logs\shop.log | Select-String "ERROR"
```

### Nội dung file logs/tong_hop.txt

```text
 === TONG HOP LOG ===


2025-10-28 08:51:28 [WARNING] Thoi gian tai trang cham
2025-10-28 08:54:28 [WARNING] Anh san pham dung luong lon
2025-10-28 08:57:28 [WARNING] Thoi gian tai trang cham
 
2025-10-28 08:24:28 [ERROR] Thanh toan bi tu choi
2025-10-28 08:30:28 [ERROR] Thanh toan bi tu choi
2025-10-28 08:33:28 [ERROR] Ket noi kho du lieu that bai
2025-10-28 08:39:28 [ERROR] Ket noi kho du lieu that bai
2025-10-28 08:42:28 [ERROR] Ket noi kho du lieu that bai
2025-10-28 09:12:28 [ERROR] Thanh toan bi tu choi

```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/don_ban_thang_10.xlsx`, không cần ghi vào đây.
