1.Tạo thư mục và mở file:Bước 1.Mở Terminal (PowerShell hoặc Git Bash) tại thư mục gốc chứa bài tập của bạn (ví dụ D:\BAITAP\IT209_DEVOPS\). Chạy lệnh sau để tạo cấu trúc thư mục cho Bài 1:Bashmkdir -p homework/session_06/ex1
Sau đó, bạn mở thư mục này bằng VS Code (hoặc trình soạn thảo bất kỳ) và tạo một file mới có tên chính xác là README.md nằm bên trong thư mục ex1.2.Sao chép nội dung báo cáo:Bước 2.Copy toàn bộ đoạn văn bản dưới đây và dán vào file README.md vừa tạo:Markdown# Báo cáo Bài 1: Khảo sát FHS và Phân quyền File/Folder nâng cao

## 1. Nhật ký các lệnh đã thực hiện
Để khởi tạo cấu trúc thư mục và phân quyền theo yêu cầu, em đã chạy các lệnh sau trên terminal Linux:
- `sudo mkdir -p /var/www/my-app/public`
- `sudo mkdir -p /var/www/my-app/logs`
- `sudo chown -R $USER:www-data /var/www/my-app`
- `sudo chmod 750 /var/www/my-app/public`
- `sudo chmod 770 /var/www/my-app/logs`

## 2. Kết quả kiểm tra phân quyền
Đầu ra của lệnh `ls -la /var/www/my-app`:

(Dán kết quả copy từ Ubuntu của bạn vào đây)
3.Chèn kết quả thực tế từ Ubuntu:Bước 3.Mở cửa sổ Ubuntu (WSL) của bạn lên và chạy lệnh:Bashls -la /var/www/my-app
Bôi đen toàn bộ đoạn kết quả in ra trên màn hình (những dòng có chứa chữ drwxr-x--- và drwxrwx---), sau đó nhấn chuột phải để copy.Quay trở lại VS Code, dán đè đoạn kết quả đó vào thay cho dòng (Dán kết quả copy từ Ubuntu của bạn vào đây). Cuối cùng, nhấn Ctrl + S để lưu file.4.Đẩy bài lên GitHub:Bước 4.Quay lại cửa sổ Terminal (Git Bash/PowerShell bên Windows), gõ lần lượt 3 lệnh sau để đưa bài tập lên kho lưu trữ:Bashgit add homework/session_06/ex1/README.md
git commit -m "Nop bai 1 SS06 - Phan quyen FHS"
git push origin main
