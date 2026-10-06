# Báo cáo Bài 2: Cấu hình phân quyền Nhóm và sudoers bằng visudo

## 1. Dòng cấu hình đã thêm vào hệ thống (sudoers)
Đã sử dụng lệnh `sudo visudo` và thêm cấu hình sau vào cuối tệp `/etc/sudoers` để cấp quyền chạy các lệnh quản lý dịch vụ (không cần mật khẩu) cho nhóm `devops-admin`:

```bash
%devops-admin ALL=(ALL) NOPASSWD: /usr/bin/systemctl start *, /usr/bin/systemctl stop *, /usr/bin/systemctl restart *, /usr/bin/systemctl status *
