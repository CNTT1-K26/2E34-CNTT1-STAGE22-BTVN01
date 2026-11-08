# Báo Cáo Kỹ Thuật: Sử Dụng Toán Tử Tìm Kiếm Nâng Cao Tìm Giáo Trình Chính Thống

## 1. Mục tiêu
Sử dụng phối hợp các toán tử tìm kiếm nâng cao (Google Search Operators / Google Dorks) để truy xuất trực tiếp các tệp tài liệu chính thống từ máy chủ trường đại học, hạn chế tối đa rủi ro nhiễm mã độc và tránh các trang web quảng cáo, bắt nạp thẻ.

---

## 2. Bối cảnh (Roleplay)
Là một sinh viên đang trong quá trình ôn thi môn **Nhập môn Công nghệ Thông tin**, tôi cần gấp bản PDF chính thức của cuốn giáo trình do Học viện phát hành. Tuy nhiên, khi tìm kiếm bằng các từ khóa thông thường, Google liên tục trả về các kết quả từ các trang web chia sẻ tài liệu rác, yêu cầu nạp tiền, tải ứng dụng lạ hoặc chứa nhiều liên kết quảng cáo độc hại.

---

## 3. Yêu cầu nghiệp vụ & Chuỗi truy vấn (Search Query)

### Chuỗi truy vấn hoàn chỉnh:
```text
"giáo trình nhập môn công nghệ thông tin" filetype:pdf site:ptit.edu.vn -site:tailieu.vn -site:doc123.vn -site:slideshare.net
```

### Phân tích cú pháp:
* **`"giáo trình nhập môn công nghệ thông tin"`**: Dùng dấu ngoặc kép để bắt buộc Google tìm kiếm chính xác cụm từ này theo đúng thứ tự, tránh việc trả về các kết quả chỉ chứa từ rời rạc.
* **`filetype:pdf`**: Chỉ định định dạng tệp trả về là PDF.
* **`site:ptit.edu.vn`**: Giới hạn phạm vi tìm kiếm chỉ nằm trong tên miền chính thức của Học viện Công nghệ Bưu chính Viễn thông (`ptit.edu.vn`).
* **`-site:tailieu.vn -site:doc123.vn -site:slideshare.net`**: Sử dụng toán tử trừ (`-`) kết hợp `site:` để loại bỏ hoàn toàn các trang web rác, trang thu phí trung gian thường xuất hiện ở top đầu.

---

## 4. Yêu cầu đầu ra

### 4.1. Lý do toán tử `filetype:` giúp tiết kiệm thời gian
1. **Lọc trực tiếp định dạng tệp (Direct File Filtering):** Khi sử dụng các cụm từ như *"tải sách..."* hoặc *"download..."*, thuật toán của Google sẽ ưu tiên các trang web bài viết chuẩn SEO chứa nhiều quảng cáo hoặc trang trung gian. Trong khi đó, `filetype:pdf` ra lệnh cho công cụ tìm kiếm chỉ duyệt và trả về các đường dẫn liên kết trực tiếp đến tệp tin PDF.
2. **Loại bỏ bước trung gian và rủi ro an ninh:** Tránh được tình trạng bấm vào web -> chờ đếm ngược 30 giây -> bấm qua 3-4 trang quảng cáo -> nhận link hỏng hoặc file `.exe` giả mạo chứa mã độc. Sinh viên có thể xem trực tiếp hoặc tải tệp về ngay chỉ với 1 cú click.

---

### 4.2. Mô phỏng 3 kết quả đầu tiên sau khi áp dụng "Combo toán tử"

```text
================================================================================
[1] [PDF] Giáo trình Nhập môn Công nghệ Thông tin - Khoa CNTT1
    URL: https://portal.ptit.edu.vn/cntt/files/Giao_trinh_Nhap_mon_CNTT.pdf
    Mô tả: Tài liệu chính thức phục vụ giảng dạy và học tập môn Nhập môn Công nghệ 
    Thông tin tại Học viện Công nghệ Bưu chính Viễn thông. Bao gồm kiến thức cơ bản 
    về phần cứng, phần mềm, hệ điều hành và mạng máy tính.
--------------------------------------------------------------------------------
[2] [PDF] Đề cương chi tiết & Giáo trình Nhập môn CNTT - PTIT E-Learning
    URL: https://lms.ptit.edu.vn/pluginfile.php/12845/mod_resource/content/1/GiaoTrinh_NMCNTT_2026.pdf
    Mô tả: Tệp PDF giáo trình định dạng chuẩn phát hành trên hệ thống đào tạo trực 
    tuyến LMS của Học viện dành cho sinh viên hệ chính quy.
--------------------------------------------------------------------------------
[3] [PDF] Slide bài giảng và Giáo trình Nhập môn Công nghệ Thông tin
    URL: https://library.ptit.edu.vn/digital-assets/ict/nhap_mon_cntt_full.pdf
    Mô tả: Tài liệu lưu hành nội bộ do Trung tâm Thông tin Thư viện PTIT số hóa, 
    cung cấp nền tảng kiến thức cho sinh viên năm nhất Khoa Công nghệ Thông tin.
================================================================================
```