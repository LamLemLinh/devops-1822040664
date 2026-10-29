# Bài tập GitHub Actions - Hoàng Lâm

- Họ tên: Hoàng Lâm
- MSSV: 1822040664
- Repository cần tạo: `devops-1822040664`
- Website sau khi deploy: `https://USERNAME.github.io/devops-1822040664/`

## Cách dùng
1. Giải nén ZIP.
2. Mở thư mục trong VS Code.
3. Tạo repository Public `devops-1822040664` trên GitHub.
4. Đưa toàn bộ nội dung thư mục này lên nhánh `main`, nhớ giữ thư mục `.github/workflows/`.
5. Vào Settings → Pages → Build and deployment → Source: GitHub Actions.
6. Vào Actions để xem workflow chạy.

## Kiểm thử thất bại theo đề
1. Mở `index.html`, xóa nguyên dòng `<title>Hoàng Lâm - Website CI/CD GitHub Actions</title>`.
2. Lưu, commit và push lên `main`.
3. Trong Actions, job `check` phải thất bại tại bước `Check HTML title`, job `deploy` bị bỏ qua vì `needs: check`.
4. Khôi phục dòng `<title>`.
5. Đổi `Phiên bản 1.0` thành `Phiên bản 2.0`, commit và push.
6. Chờ workflow thành công, mở URL Pages và tải lại trang.

## Đẩy code bằng Terminal trong VS Code
Sau khi tạo repository trống trên GitHub, chạy trong thư mục dự án (thay USERNAME):
```bash
git init
git branch -M main
git add .
git commit -m "Initial website and GitHub Actions workflow"
git remote add origin https://github.com/USERNAME/devops-1822040664.git
git push -u origin main
```
Nếu đã có remote `origin`, dùng `git remote set-url origin https://github.com/USERNAME/devops-1822040664.git`.
