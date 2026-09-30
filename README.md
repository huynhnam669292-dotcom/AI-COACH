# 🧭 AI COACH – TRỢ LÝ HUẤN LUYỆN NĂNG LỰC TỰ CHỦ TRONG RA QUYẾT ĐỊNH CỦA HỌC SINH THPT TRONG MÔI TRƯỜNG SỐ

Ứng dụng web Chatbot được thiết kế theo giao diện chuẩn **ChatGPT**, tích hợp đầy đủ bộ quy tắc huấn luyện gồm **6 Năng Lực (NL1 – NL6)**, **Cơ chế giàn giáo giảm dần hỗ trợ (3-2-1-0)**, **Bộ nhận diện bẫy số** và **Bản đồ quyết định**.

---

## 🚀 1. CÁCH TRUY CẬP VÀ SỬ DỤNG TRANG WEB

Trang web được thiết kế theo kiến trúc **Zero-Dependency (Không cần cài đặt thư viện rườm rà)**, chạy mượt mà trên mọi thiết bị (máy tính Windows, Mac, iPad, điện thoại iOS/Android).

### Cách 1: Mở trực tiếp trên máy Mac / Windows (Nhanh nhất)
1. Mở Finder (hoặc File Explorer trên Windows).
2. Tìm đến thư mục:
   ```bash
   /Users/huynhtranduy/.gemini/antigravity/scratch/ai-coach-web
   ```
3. Nhấp đúp chuột vào tệp **`index.html`** để mở ngay trên trình duyệt (Google Chrome, Safari, Microsoft Edge, Cốc Cốc).
4. Hoặc trên Terminal của máy Mac, gõ:
   ```bash
   open /Users/huynhtranduy/.gemini/antigravity/scratch/ai-coach-web/index.html
   ```

---

### Cách 2: Chạy Web Server Cục Bộ (Localhost)
Nếu bạn muốn chạy dạng máy chủ nội bộ:
```bash
cd /Users/huynhtranduy/.gemini/antigravity/scratch/ai-coach-web
python3 server.py
```
Sau đó truy cập trình duyệt tại địa chỉ: **`http://localhost:8000`**

---

### Cách 3: Đưa lên mạng Internet MIỄN PHÍ để cả trường / cả lớp truy cập (Khuyên dùng)
Bạn có thể dễ dàng tạo một đường link web công khai (ví dụ: `https://ai-coach-thpt.vercel.app`) để học sinh truy cập bằng điện thoại:

#### 1. Đưa lên Vercel (Khuyên dùng - 30 giây):
- Truy cập [vercel.com](https://vercel.com) và đăng nhập bằng tài khoản Google/GitHub.
- Kéo thả toàn bộ thư mục `ai-coach-web` vào trang chủ Vercel.
- Nhận ngay đường link web HTTPS vĩnh viễn miễn phí để chia sẻ cho học sinh.

#### 2. Đưa lên GitHub Pages / Netlify:
- Đẩy thư mục mã nguồn lên GitHub.
- Vào **Settings > Pages > Branch: main** và chọn Save.
- Trang web sẽ tự động hoạt động trực tuyến.

---

## ⚙️ 2. HƯỚNG DẪN CẤU HÌNH & QUẢN LÝ (DÀNH CHO QUẢN TRỊ VIÊN / GIÁO VIÊN)

Bấm vào nút **"⚙️ Quản lý & Cài đặt AI"** ở góc dưới thanh bên trái để mở Bảng Điều Khiển:

### 1. Cấu hình Trí tuệ Nhân tạo (Tab: "Cấu hình AI & API")
Hệ thống hỗ trợ 3 chế độ hoạt động linh hoạt:
- **Google Gemini API (Khuyên dùng):**
  - Đăng ký và lấy API Key miễn phí tại: [Google AI Studio](https://aistudio.google.com/app/apikey).
  - Nhập khóa API vào ô `API Key` (dạng `AIzaSy...`).
  - Chọn model: `gemini-2.0-flash` (tốc độ siêu nhanh) hoặc `gemini-1.5-pro` (suy luận sâu).
  - Bấm **"Kiểm tra kết nối API"** để xác nhận thành công.
- **OpenAI API:**
  - Nhập khóa `sk-...` và chọn model `gpt-4o-mini` hoặc `gpt-4o`.
- **Chế độ Giả lập Ngoại tuyến (Offline Coach Engine):**
  - Không cần mạng Internet, không cần nhập API Key.
  - Hệ thống tích hợp sẵn thuật toán thông minh mô phỏng đầy đủ 15 nguyên tắc của AI Coach (từ chối chọn hộ, phát hiện bẫy số flash sale, kích thích học sinh tư duy).

---

### 2. Quản lý Nội dung Huấn luyện (Tab: "System Prompt Huấn Luyện")
- Toàn bộ Prompt 15 phần được tích hợp sẵn trong tệp `system-prompt.js` và hiển thị trực tiếp trong ô soạn thảo.
- Giáo viên có thể bổ sung các tình huống cụ thể của trường lớp, quy định ứng xử số, hoặc bấm **"Khôi phục nguyên bản"** bất kỳ lúc nào.

---

### 3. Theo dõi & Đánh giá Quá trình của Học sinh (Tab: "Dữ liệu & Nhật ký")
- Xem danh sách toàn bộ các phiên giải quyết vấn đề của học sinh.
- Kiểm tra số lượng tin nhắn, mức độ tự chủ đạt được.
- Nút **"Xuất file JSON"**: Tải về toàn bộ dữ liệu đối thoại để giáo viên phục vụ công tác nghiên cứu khoa học sư phạm, đánh giá năng lực học sinh.
- Tải file Markdown tóm tắt từng phiên trò chuyện qua nút Tải xuống trên thanh tiêu đề.

---

## 🧠 3. TÍNH NĂNG NỔI BẬT DÀNH CHO HỌC SINH THPT

1. **Khung 6 Năng Lực (NL1 – NL6) Trực Quan:**
   - Đèn chỉ báo tiến độ sáng dần theo từng bước:
     - **NL1:** Nhận diện vấn đề & mục tiêu
     - **NL2:** Chủ động tìm kiếm thông tin
     - **NL3:** Kiểm chứng & đánh giá nguồn
     - **NL4:** Xác định & cân nhắc nhiều phương án
     - **NL5:** Ra quyết định dựa trên căn cứ
     - **NL6:** Phản tư & điều chỉnh
2. **Cơ chế Giàn giáo 3-2-1-0:**
   - Dễ dàng chuyển đổi mức hỗ trợ từ **Mức 3 (Hỗ trợ cao)** xuống **Mức 0 (Tự chủ hoàn toàn)**.
3. **Bộ Cảnh Báo Bẫy Số Thời Gian Thực:**
   - Tự động phát hiện khi học sinh gặp phải các yếu tố: Flash sale, đồng hồ đếm ngược, KOL/KOC review, tâm lý FOMO, số đông bầy đàn.
4. **🧭 Bản Đồ Quyết Định Của Tôi:**
   - Khi hoàn thành quá trình, AI sẽ tự động lập Bản Đồ Quyết Định chuẩn mực, kích hoạt hiệu ứng pháo hoa chúc mừng 🎉 và cung cấp chức năng **In ấn / Xuất file PDF**.
5. **Nhập liệu bằng giọng nói (Voice Mic):**
   - Học sinh có thể nhấn vào biểu tượng micro để nói trực tiếp thay vì gõ văn bản.

---

## 📁 4. CẤU TRÚC TỆP DỰ ÁN

```text
ai-coach-web/
├── index.html        # Giao diện chính ChatGPT hiện đại, phản hồi nhạy
├── style.css         # Bảng định kiểu chuyên nghiệp, hỗ trợ in ấn PDF
├── app.js            # Xử lý logic AI, gọi API Gemini/OpenAI, engine offline
├── system-prompt.js  # Hệ thống chỉ dẫn gốc chuẩn 15 phần của AI Coach
├── server.py         # Máy chủ HTTP cục bộ hỗ trợ chạy nhanh
└── README.md         # Tài liệu hướng dẫn sử dụng và quản lý chi tiết
```
