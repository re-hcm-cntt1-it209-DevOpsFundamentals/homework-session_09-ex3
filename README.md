# Bài 3: Đóng gói trang Web HTML tĩnh với Dockerfile

## Giới thiệu
Bài tập thực hành tạo một trang web HTML tĩnh đơn giản và đóng gói ứng dụng này vào Docker Image dựa trên base image Nginx Alpine.

## Chức năng đã làm
- Tạo trang `index.html` đơn giản với nội dung `<h1>Hello Docker Session 09!</h1>`.
- Viết `Dockerfile` 2 câu lệnh để copy `index.html` vào thư mục mặc định của Nginx Alpine (`/usr/share/nginx/html/index.html`).

## Hướng dẫn chạy chương trình

1. **Build Docker Image:**
```bash
docker build -t my-html-app:v1 .
```

2. **Khởi chạy Container từ Image:**
```bash
docker run -d -p 8081:80 --name html-app my-html-app:v1
```

3. **Kiểm tra kết quả:**
```bash
curl http://localhost:8081
```

Kết quả mong đợi trả về:
```html
<h1>Hello Docker Session 09!</h1>
```


## Ảnh chụp màn hình kết quả thực nghiệm
![Kết quả thực nghiệm](nginx_verification_result.png)
