# API CI and Docs

Hướng dẫn nhanh

1. Cập nhật postman_environment.json biến base_url cho đúng
2. Commit postman_collection.json và postman_environment.json vào repo
3. Tạo secret GH_PAGES_TOKEN với quyền push
4. Push lên nhánh main để workflow chạy

Kết quả mong đợi
- Link chạy CI: (update ở đây khi có)
- Link tài liệu công khai: https://<your-github-username>.github.io/<repo-name>/

Nếu bạn muốn public doc trên Postman thay vì GitHub Pages
1. Import file postman_collection.json vào Postman
2. Tạo public workspace hoặc public documentation theo hướng dẫn Postman
3. Lấy Postman Public link và dán vào đâu cần
