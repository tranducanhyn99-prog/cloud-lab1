# My First Cloud Website - Lab 01

Trang web tĩnh phục vụ đồ án thực hành **Lab 01: Deploy Your First Static Website to the Cloud**.
Môn học: **Introduction to Cloud Computing**
Giảng viên: **Trương Thị Ngọc Phượng**

---

## 📁 Cấu trúc thư mục

```text
cloud-lab1/
├── assets/
│   ├── avatar.svg         # Ảnh avatar sinh viên
│   └── cloud.svg          # Hình minh họa kiến trúc Cloud Computing
├── index.html             # Trang web chính (Semantic HTML5, đầy đủ 4 section yêu cầu)
├── style.css              # Custom CSS responsive, tối ưu desktop & mobile
├── report.html            # Mẫu báo cáo HTML định dạng in ấn/PDF xuất sắc
├── Lab01_Report.md        # Mẫu báo cáo Markdown với đầy đủ 5 câu trả lời E5
└── README.md
```

## 🚀 Hướng dẫn Triển khai lên GitHub Pages (Option B)

1. **Cập nhật thông tin cá nhân (Họ tên & MSSV):**
   - Mở file `index.html` và chỉnh sửa:
     - Họ và tên: `Trần Đức Anh` &rarr; đổi thành tên của bạn nếu cần.
     - MSSV: `23520001` &rarr; đổi thành MSSV của bạn.
   - Làm tương tự trong file `Lab01_Report.md` và `report.html`.

2. **Tạo repository trên GitHub:**
   - Đăng nhập vào [GitHub](https://github.com/).
   - Tạo một repository mới ở chế độ **Public** với tên: `cloud-lab1`.

3. **Đẩy mã nguồn lên GitHub:**
   ```bash
   git add .
   git commit -m "feat: complete Lab 01 static website"
   git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/cloud-lab1.git
   git branch -M main
   git push -u origin main
   ```

4. **Kích hoạt GitHub Pages:**
   - Trên GitHub, vào repo `cloud-lab1` &rarr; **Settings** &rarr; mục **Pages** (bên menu trái).
   - Tại phần **Build and deployment**:
     - **Source**: Chọn `Deploy from a branch`
     - **Branch**: Chọn `main` và thư mục `/ (root)`
     - Bấm **Save**.
   - Đợi khoảng 1 - 2 phút, GitHub sẽ hiển thị thông báo:
     > *"Your site is live at https://<YOUR_GITHUB_USERNAME>.github.io/cloud-lab1/"*
   - Tích chọn **Enforce HTTPS** (nếu chưa bật).

5. **Thu thập 4 ảnh minh chứng (Screenshots E1 - E4):**
   - **E1 – Desktop website:** Mở trang web trên trình duyệt máy tính, chụp ảnh toàn màn hình có thấy rõ Họ tên và MSSV.
   - **E2 – Mobile website:** Bấm F12 trên trình duyệt &rarr; chuyển sang chế độ thiết bị di động (Toggle device toolbar) &rarr; chụp ảnh hiển thị responsive.
   - **E3 – Hosting dashboard:** Chụp màn hình trang **Settings &rarr; Pages** trên GitHub thể hiện trạng thái đã deploy thành công.
   - **E4 – HTTPS verification:** Mở trình duyệt ẩn danh (Incognito), truy cập link `https://<YOUR_GITHUB_USERNAME>.github.io/cloud-lab1/`, chụp rõ thanh địa chỉ có icon ổ khóa HTTPS.

6. **Xuất báo cáo PDF & Đóng gói nộp bài:**
   - Dán 4 ảnh vào file Word hoặc file `report.html` (mở trong Chrome rồi ấn `Ctrl + P` &rarr; Save as PDF) thành file `Lab01_Report_<MSSV>.pdf`.
   - Nén thư mục thành file ZIP: `Lab01_<MSSV>_<HovatenKhongDau>.zip` (Ví dụ: `Lab01_23520001_NguyenVanA.zip`).
   - Nộp file ZIP và dán link HTTPS lên LMS của trường!
