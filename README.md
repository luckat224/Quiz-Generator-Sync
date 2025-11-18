# 🎓 Quiz Generator - Tự Động Tạo Bài Tập

Ứng dụng web thông minh giúp bạn **tự động phân loại** và tạo bài tập trắc nghiệm từ dữ liệu văn bản.

## ✨ Tính Năng

### 🤖 Phân Tích Thông Minh
- **Tự động nhận diện** loại câu hỏi:
  - ✅ Trắc nghiệm (Multiple Choice)
  - ✅ Đúng/Sai (True/False)
  - ✅ Tự luận (Short Answer)
- **Không cần format JSON** - Chỉ cần nhập text thông thường!

### 📝 Nhập Dữ Liệu Dễ Dàng
```
1. Câu hỏi trắc nghiệm?
A. Đáp án 1
B. Đáp án 2
C. Đáp án 3
D. Đáp án 4
Đáp án: B

2. Câu hỏi đúng/sai:
a. Phát biểu 1 (Đúng)
b. Phát biểu 2 (Sai)
c. Phát biểu 3 (Đúng)

3. Câu tự luận: Giải thích...?
```

### 🎯 Làm Bài Tập
- Hiển thị câu hỏi đẹp mắt
- Kiểm tra đáp án tự động
- Hiển thị điểm số real-time
- Xáo trộn câu hỏi
- Reset để làm lại

### 💾 Lưu Trữ & Xuất Dữ Liệu
- Tự động lưu vào LocalStorage
- Xuất ra file JSON
- Copy JSON để chia sẻ

## 🚀 Cách Sử Dụng

### 1. Mở File
```bash
# Chỉ cần mở file trong trình duyệt
start index.html
```
Hoặc double-click vào file `index.html`

### 2. Nhập Dữ Liệu
- Vào tab **"Nhập Dữ Liệu"**
- Paste hoặc nhập câu hỏi của bạn
- Click **"Phân Tích & Tạo Quiz"**

### 3. Làm Bài
- Chuyển sang tab **"Làm Bài Tập"**
- Trả lời các câu hỏi
- Xem điểm số

### 4. Xuất Dữ Liệu (Optional)
- Tab **"Xuất Dữ Liệu"**
- Copy JSON hoặc tải file

## 📋 Định Dạng Nhập Liệu

### Trắc Nghiệm
```
Câu hỏi của bạn?
A. Đáp án 1
B. Đáp án 2
C. Đáp án 3
D. Đáp án 4
Đáp án: B
```
Hoặc:
```
Câu hỏi?
A) Đáp án 1
B) Đáp án 2
Đáp án: B) Đáp án 2
```

### Đúng/Sai
```
Câu hỏi chính:
a. Phát biểu thứ nhất (Đúng)
b. Phát biểu thứ hai (Sai)
c. Phát biểu thứ ba (Đúng)
```

### Tự Luận
```
Giải thích khái niệm X?
```
(Không cần đáp án cụ thể)

## 🎨 Giao Diện

- ✨ **Modern & Đẹp mắt** - Gradient background
- 📱 **Responsive** - Hoạt động tốt trên mobile
- 🎯 **Dễ sử dụng** - Interface trực quan
- ⚡ **Nhanh chóng** - Không cần server

## 💡 Tips

1. **Mỗi câu hỏi cách nhau bằng 1 dòng trống**
2. **Trắc nghiệm phải có "Đáp án:"** ở cuối
3. **Đúng/Sai phải có (Đúng) hoặc (Sai)** sau mỗi phát biểu
4. **Hỗ trợ cả A. B. C. D. và A) B) C) D)**

## 🔧 Công Nghệ

- HTML5
- Vanilla JavaScript
- Tailwind CSS
- LocalStorage API
- No Dependencies!

## 📦 Cài Đặt

Không cần cài đặt! Chỉ cần:
1. Clone hoặc download file `index.html`
2. Mở bằng trình duyệt
3. Bắt đầu sử dụng!

## 🎯 Use Cases

- 📚 Giáo viên tạo đề thi nhanh
- 🎓 Học sinh ôn tập
- 💼 Training nhân viên
- 📝 Tạo quiz từ tài liệu

## 🤝 Đóng Góp

Mọi đóng góp đều được chào đón! 
- Fork repo
- Tạo branch mới
- Submit pull request

## 📄 License

MIT License - Tự do sử dụng!

## 🌟 Features Sắp Tới

- [ ] Import từ file Word/PDF
- [ ] Thêm hình ảnh vào câu hỏi
- [ ] Chế độ thi thời gian
- [ ] Xuất ra PDF
- [ ] AI tự động tạo câu hỏi

---

Made with ❤️ for Education
