# Thuyet-Trinh-Kiem-Ke-CCDC

Bộ slide thuyết trình kiểm kê tài sản CCDC trên V5 theo mô hình mới: kiểm theo nơi đặt, xác nhận theo người giữ (16/11/2026). Toàn bộ nằm trong `index.html`, mở bằng trình duyệt là chạy.

Phím tắt:

- `→` / `Space` / `PageDown`: slide sau. `←` / `PageUp`: slide trước. `Home` / `End`: slide đầu, slide cuối.
- `N`: bật/tắt ghi chú người trình bày.
- `F`: toàn màn hình.
- Bấm vào 1/3 bên trái slide để lùi, phần còn lại để tiến. Trên cảm ứng thì vuốt.
- Màn hình hẹp (điện thoại) hiện các slide xếp dọc.
- In ra PDF (Ctrl+P): mỗi slide một trang.

**Luồng mới (họp 19/11/2026, anh Đạt đã duyệt 20/11): kiểm theo vùng và theo nhân viên.** Tài sản có cột Chung / Riêng; đợt vẫn theo công ty; phần nhân viên chỉ có đồ Riêng; kiểm vùng bắt đầu trắng, thêm từng món, có 3 cảnh báo và lưu vết; chốt vùng sinh phiếu theo người quản lý nhóm CCDC.

- `kiem-ke-theo-vung-phan-tich.html`: trang phân tích luồng mới, số liệu thật, 6 câu còn mở.
- `minh-hoa-kiem-ke-theo-vung.html`: màn minh hoạ bấm được: Công cụ dụng cụ (Chung / Riêng), Đợt kiểm kê, Kiểm vùng, Kiểm kê của tôi, Phiếu duyệt của tôi, Báo cáo, và menu **App kiểm kê (mobile)** (khung điện thoại: quét tem, cảnh báo, chốt vùng, xác nhận phiếu, đồ riêng; mở thẳng `?man=app`). Đổi người đăng nhập ở thanh trên cùng. Mở thẳng: `?man=kiemvung&vung=T4_HOP`, `?man=phieu&vai=hung`, `?man=bc&tab=cg`.

Các tài liệu bên dưới là của mô hình 16/11 (kiểm theo nơi đặt, xác nhận theo người giữ), giữ để đối chiếu.

Tài liệu kèm theo:

- `HUONG-DAN-DOC-KIEM-KE.md`: hướng dẫn đọc tuần tự để nắm trọn luồng (trang phân tích → màn minh hoạ → slide), mỗi bước ghi đọc xong làm được gì, cuối file là 12 câu tự kiểm tra và việc cần làm trước, trong, sau buổi gặp anh Đạt.
- `kiem-ke-mo-hinh-moi-phan-tich.html`: phân tích mô hình kiểm kê mới (kiểm theo nơi đặt, xác nhận theo người giữ), có ví dụ một đợt từ đầu đến cuối, thao tác mobile, web và báo cáo. Hướng đã thống nhất; mục 12 là các câu cần anh Đạt chốt (16/11/2026).
- `minh-hoa-tao-dot-kiem-ke.html`: màn minh hoạ web cho mô hình mới: danh sách đợt, form tạo đợt hai bước, chi tiết đợt (5 tab báo cáo, chi tiết từng phần) màn xác nhận của nhân viên (menu "NV xác nhận kiểm kê") và app mobile (menu "App kiểm kê", mở thẳng bằng `?vai=app`; đăng nhập app bằng chị Lan để đi kiểm: quét, thêm tài sản, tình trạng, tem; hoặc bằng anh Sơn để xác nhận phiếu, `?vai=app&tk=son`). Thêm menu **Báo cáo kiểm kê** (tab Theo tài sản `?man=bc` và Theo nhân viên `?man=bcnv`; chọn nhiều công ty, nhiều đợt, mỗi đợt một cột), menu **Câu hỏi cần chốt** để hỏi anh Đạt và ghi câu trả lời ngay trong buổi họp (`?man=cau`) và **Tài sản của tôi** cho nhân viên trên web (`?man=toi`) lẫn app (`?vai=app&tk=son&man=ts`), chờ anh Đạt chốt câu 8. Các màn dùng chung dữ liệu. Có kịch bản demo; dữ liệu giả.
- `thuyet-trinh-v31.html`: bộ slide cũ theo thiết kế v3.1, giữ để đối chiếu. Mô hình mới thay phần kiểm theo phiên của v3.1.
- `kiem-ke-tai-san-v3.html`: thiết kế v3.1 (database, API, luật nghiệp vụ, phân quyền, kế hoạch). Sẽ được thay bằng thiết kế mới khi các câu hỏi được chốt; 16/11/2026 bỏ phần sinh phiếu điều chuyển.
- `kiem-ke-tai-san-v2.html`: thiết kế v2, bản trước, giữ để đối chiếu.
