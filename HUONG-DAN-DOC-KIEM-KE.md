# Đọc gì, theo thứ tự nào để nắm chắc luồng kiểm kê mới

Có 3 file, cùng nằm trong `coordination/`, và đều đã có bản trên mạng:

| Gọi tắt | File | Bản trên mạng |
|---|---|---|
| **Trang phân tích** | `kiem-ke-mo-hinh-moi-phan-tich.html` | https://nguyenvanchiens.github.io/Thuyet-Trinh-Kiem-Ke-CCDC/kiem-ke-mo-hinh-moi-phan-tich.html |
| **Màn minh hoạ** | `minh-hoa-tao-dot-kiem-ke.html` | https://nguyenvanchiens.github.io/Thuyet-Trinh-Kiem-Ke-CCDC/minh-hoa-tao-dot-kiem-ke.html |
| **Slide** | `thuyet-trinh-kiem-ke-mo-hinh-moi.html` | https://nguyenvanchiens.github.io/Thuyet-Trinh-Kiem-Ke-CCDC/ |

Đọc tổng khoảng 1 tiếng. Phần A đọc chữ, phần B vừa đọc vừa bấm demo, phần C đọc chi tiết và chỗ chưa chốt, phần D tập trình bày.

Trên trang phân tích, mọi chỗ có nhãn cam **❓ Hỏi anh Đạt · câu N** là **chưa chốt**. Bấm nhãn sẽ nhảy tới câu đó ở mục 12.

---

## A. Hiểu vì sao phải làm lại (Trang phân tích, 15 phút)

**A1. Mục 01 · Tóm tắt.** Kiểm kê tách thành hai việc:
- *Kiểm* là việc của hành chính, đi theo **nơi đặt** đồ: người, tầng/phòng, kho.
- *Xác nhận* là việc của **người giữ** đồ.

Khung vàng cuối mục: điều đầu tiên cần hỏi anh Đạt là có đi theo hướng này không.

→ **Đọc xong:** nói được ý chính trong 1 câu: "hành chính đi kiểm theo nơi đặt đồ, người giữ đồ xác nhận". Đây là câu mở đầu khi trình bày.

**A2. Mục 02 · Bài toán cần giải.** Ba câu công ty cần trả lời sau mỗi đợt:
- nhân viên nào chưa được kiểm;
- tài sản nào chưa được kiểm;
- ai chịu trách nhiệm cho từng món.

Ràng buộc đã chốt: kiểm kê **không sinh phiếu** và **không sửa** bảng tài sản.

→ **Đọc xong:** biết mô hình mới phải trả lời được 3 câu nào. Mọi màn hình, báo cáo ở các mục sau đều để trả lời 3 câu này.

**A3. Mục 03 · V4 đang làm gì và sai ở đâu.** Sáu lỗi của V4, kèm chỗ trong code. Mục này để trả lời câu "V4 đang chạy, sao phải đổi?". Cần nhớ 3 lỗi gốc:
- một món nằm trong hai danh sách (theo người và theo vùng);
- kiểm theo vùng không ghi ai giữ;
- không ai xác nhận kết quả.

→ **Đọc xong:** kể được 3 lỗi đó kèm ví dụ (2 chiếc ghế bị ghi "Không thấy" ở Tầng 3 trong khi đang ở phòng họp tầng 5). Đây là lý do thuyết phục anh Đạt phải đổi.

**A4. Mục 04 · Ba cách đã cân nhắc.** Đọc lướt. Chỉ cần khi bị hỏi "sao không giữ kiểu theo người hoặc theo vùng như V4".

→ **Đọc xong:** chuyển sang phần B.

## B. Hiểu luật và luồng (Trang phân tích + Màn minh hoạ, 35 phút)

**B1. Mục 05 · Mô hình đề xuất.** Đọc kỹ. Đây là luật cốt lõi.
- Hai tầng: Kiểm và Xác nhận.
- Bảng "Luật chia phần lúc mở đợt": mỗi tài sản vào **đúng một** phần:
  - đồ ở kho vào phần kho;
  - đồ có người giữ, đặt ở tầng/phòng vào phần vùng;
  - còn lại vào phần người;
  - đồ ở kho mà thiếu mã vùng: xem câu 1.
- Danh sách người là **mọi nhân viên đang làm**, kể cả người chưa giữ món nào.

→ **Đọc xong:** cầm một món bất kỳ (laptop của anh Minh, ghế ở Tầng 3, màn hình trong kho) là nói ngay được nó thuộc phần nào và ai ký. Chưa nói được thì đọc lại bảng luật trước khi sang B2.

**B2. Mục 06 · Luồng kiểm kê từ đầu đến cuối.** Đọc bảng **Bối cảnh** trước (anh Minh, anh Sơn, anh Tú, Kho MB, anh Nam), rồi mở Màn minh hoạ bên cạnh. Bấm **"Làm lại từ đầu"** ở thanh vàng trên cùng. Mỗi bước: đọc trên trang phân tích, rồi làm đúng bước đó trên demo.

| Bước ở mục 06 | Làm trên Màn minh hoạ | Phải nắm được |
|---|---|---|
| 1. Tạo đợt kiểm kê | Menu **Kiểm kê** → **+ Tạo đợt** → chọn VN01: bị chặn vì KK0012 đang mở. Chọn VN02 | Chỉ nhập tên đợt và công ty. Mỗi công ty chỉ một đợt đang mở |
| 2. Xem trước | Bấm **Tiếp: xem trước** | Hệ tự lấy người và tài sản. Thấy số phần người (kể cả người 0 món), số vùng, số kho, cảnh báo đồ ghi ở người đã nghỉ. Chọn người xác nhận kho |
| 3. Mở đợt | Bấm **Mở đợt**, rồi bấm vào đợt **KK0012** để xem màn chi tiết | Danh sách được chụp và khoá lúc mở. Phần anh Sơn đang "Chưa kiểm" |
| 4. Hành chính đi kiểm | Menu **App kiểm kê (mobile)** → bấm KK0012 → tab **Người** → **anh Sơn** → **Quét tem** → bấm vài tem đồ của anh Sơn → bấm tem **Ghế xoay** → **Ghi nhận ở đây** → bấm **Tem lạ** → **Về danh sách** → bấm một món chưa kiểm → **Không thấy** → **Xong phần** | Không chọn "theo người / theo vùng" như V4: bấm phần đang đứng trước mặt. Một nút Quét: app tự nhận ra món của ai. Quét phải đồ chỗ khác thì chỉ ghi nhận, không đổi người giữ. Mã lạ bị từ chối |
| 4 (tiếp) | Vẫn ở App: thử **+ Thêm tài sản**, gõ "máy tính bảng". Thử bấm một món, chọn **Hỏng** (phải chụp ảnh), tích **cần in lại tem** | Thêm tài sản dùng khi tem mất. Hỏng bắt buộc có ảnh |
| 4 (kho) | Ở App: tab **Kho** → **Kho chưa rõ** → quét 2 món → Xong phần | Kho do **người xác nhận kho** ký, không phải người đi kiểm |
| 5. Nhân viên xác nhận | Menu **NV xác nhận kiểm kê** (có số 1) → phiếu **XN0153**. Hoặc ở App đổi **Đăng nhập app bằng: anh Sơn** | Anh Sơn nhận **một** phiếu khi **mọi** phần có đồ của anh (phần anh Sơn + Tầng 3) đã xong. Xác nhận trên web hay app đều được |
| 6. Không đồng ý | Trong phiếu XN0153: **Không đồng ý** → tích **Máy chiếu** → ghi lý do → Gửi. Sang **App** (chị Lan) → Tầng 3 đang "Mở lại" → bấm Máy chiếu → **Có, nhưng đang ở chỗ khác** → Xong phần. Quay lại phiếu XN0153 → **Đồng ý** | Không đồng ý thì phải ghi lý do. Chỉ phần chứa món bị tích mới mở lại. Đã đồng ý thì khoá, không mở lại được |
| 7. Theo dõi | Menu **Kiểm kê** → KK0012 → xem 5 tab. Bấm **+ Thêm nhân viên** → sang **App**: người mới có phần 0 món → **Không giữ món nào · Xong phần** | Bốn con số trả lời: còn phần nào chưa kiểm, ai chưa xác nhận, ngoại lệ gì. Người vào giữa đợt thì thêm tay |
| 8. Đóng đợt | Menu **Kiểm kê** → KK0012 → **Đóng đợt**. Sang **App**: không còn đợt | Đóng xong thì mọi thứ khoá. Ai chưa xác nhận bị ghi "chưa xác nhận". Ngoại lệ là việc hành chính tự xử lý sau |

Đọc nốt bảng **"Khác V4 ở đâu, tóm lại"** cuối mục 06.

→ **Đọc xong:** tự kể lại luồng 8 bước mà không nhìn trang, theo ví dụ anh Sơn: tạo đợt → hệ lấy danh sách → mở đợt → chị Lan quét → anh Sơn nhận phiếu → không đồng ý → kiểm lại → đồng ý → đóng đợt. Kể được thì đã nắm luồng; phần C chỉ còn là chi tiết.

## C. Chi tiết và chỗ chưa chốt (Trang phân tích, 15 phút)

**C1. Mục 07 · Lợi ích.** 8 ý. Để trả lời câu "được gì".

→ **Đọc xong:** chọn 3 ý muốn nhấn khi trình bày. Gợi ý: không sót người mới, không món nào nằm hai nơi, mọi món có người chịu trách nhiệm.

**C2. Mục 08 · Thao tác trên mobile.** Đọc lại điều vừa bấm ở B2:
- ví dụ chị Lan kiểm anh Sơn;
- bảng "Quét ra gì thì app làm gì";
- bảng so với V4;
- phần **"Xuống kho thì sao: người xác nhận kho"**.

→ **Đọc xong:** giải thích được cho anh Đạt vì sao mobile không còn bước chọn "theo người / theo vùng", và vì sao kho cần một người ký.

**C3. Mục 09 · Thao tác trên web.** Mở đợt, trong đợt, đóng đợt.

→ **Đọc xong:** biết quản lý làm được những gì trên web: tạo, theo dõi, thêm nhân viên, mở lại phần, nhắc, đóng.

**C4. Mục 10 · Báo cáo.** Năm báo cáo. Hai báo cáo chính: tiến độ kiểm, tiến độ xác nhận.

→ **Đọc xong:** nói được báo cáo nào trả lời câu nào trong 3 câu ở mục 02.

**C5. Mục 11 · Cái giá và rủi ro.** Để trả lời thẳng khi bị hỏi "mất gì".

→ **Đọc xong:** chuẩn bị sẵn câu trả lời cho điểm khó nhất: API mobile đổi nhiều, phải báo bên app sớm.

**C6. Mục 12 · Đã chốt và câu hỏi cho anh Đạt.** Đọc kỹ.
- "Đã chốt": những gì không cần hỏi lại.
- "Số liệu thật": đếm từ dữ liệu nạp V5 (3.557 món thuộc diện kiểm). Nhớ 3 con số để nói: một người đứng tên 543 món (câu 3), 13 món VN02 nằm ở Kho MB (câu 4), chỉ 192 món có ngày kiểm cuối trong 2025–2026 (câu 6, 8).
- 8 câu hỏi, mỗi câu có ví dụ và đề xuất. Câu 1–5 là câu chính, câu 6–7 là câu nhỏ, hỏi nhanh, câu 8 là phạm vi mới.
  1. Ai xác nhận Kho MB, Kho MN (số liệu: "kho chưa rõ" 0 món, không cần hỏi phần đó).
  2. Nhân viên công ty này cầm tài sản công ty kia.
  3. Đồ chung ở các tầng đứng tên ai (số liệu: một người đứng tên 543 món ở 20 vùng, 8 người từ 50 món).
  4. Kho MB thuộc VN01, Kho MN thuộc VN02. Tài sản không có mã công ty thì tính vào đợt VN01 như V4 (đề xuất: có, và liệt kê ở báo cáo ngoại lệ "thiếu mã công ty").
  5. Ba luật xác nhận.
  6. Đóng đợt có ghi ngày kiểm cuối lên tài sản không.
  7. Món "chờ thanh lý, không sử dụng" vẫn kiểm như V4 (19 món; trạng thái "đang sử dụng" đã bỏ khỏi V4 và V5 không có; chỉ báo, không cần quyết).
  8. Có làm hai màn xem tổng quát không: menu riêng **Báo cáo kiểm kê** (chọn nhiều công ty, nhiều đợt, mỗi đợt một cột, kèm lần kiểm cuối), và "Tài sản của tôi" cho nhân viên trên web, app. Demo: menu **Báo cáo kiểm kê**, **Tài sản của tôi**.

→ **Đọc xong:** ghi sẵn ra giấy 8 câu này kèm đề xuất của mình, để trong buổi gặp hỏi lần lượt và ghi câu trả lời của anh Đạt bên cạnh.

## D. Tập trình bày (Slide)

Mở Slide, chuyển slide bằng phím ←/→. Bấm **N** để hiện ghi chú lời nói dưới mỗi slide, **F** để toàn màn hình. Slide 16 là danh sách câu hỏi; slide 17 là đề nghị bước tiếp theo.

→ **Đọc xong:** nói thử một lượt cả 17 slide, nhìn ghi chú. Chỗ nào cần demo thì mở Màn minh hoạ, làm đúng kịch bản ở B2.

---

## Tự kiểm tra: trả lời trôi chảy được là đã nắm chắc

| Câu | Đáp án ngắn |
|---|---|
| Mở đợt, hệ lấy gì? Người mới chưa có món nào có được lấy không? | Mọi nhân viên đang làm và mọi tài sản của công ty. Có, người mới vẫn có phần |
| 120 món ở Tầng 3 đứng tên anh Sơn: ai kiểm, ai ký? | Hành chính kiểm theo phần Tầng 3. Anh Sơn ký |
| Khi nào anh Sơn nhận phiếu? | Khi **mọi** phần có đồ của anh đã xong |
| Một món có nằm ở 2 phần được không? | Không, mỗi món đúng một phần |
| Trên mobile có phải chọn "theo người" hay "theo vùng" không? | Không. Bấm vào phần đã chia sẵn |
| Quét phải chiếc ghế của phòng họp trên bàn anh Sơn thì sao? | App cảnh báo. Ghi nhận thì lưu vết ở cả hai phần, **không đổi người giữ** |
| Tem mất thì sao? | + Thêm tài sản, tìm theo mã hoặc tên |
| Anh Sơn không đồng ý thì sao? | Bắt buộc ghi lý do. Phần chứa món bị tích mở lại, kiểm lại, anh Sơn xác nhận lần 2 |
| Anh Sơn đã đồng ý, quản lý có mở lại được không? | Không, kết quả đã khoá |
| Đồ trong kho ai ký? | Người xác nhận kho, chọn lúc mở đợt (ai cụ thể: chờ câu 1) |
| Đóng đợt khi còn người chưa xác nhận? | Ghi "chưa xác nhận", không tự coi là đồng ý |
| Kiểm kê có sửa người giữ hay vị trí trên bảng tài sản không? | Không. Chỉ ghi nhận và báo cáo; hành chính tự lập phiếu sau |

---

## Đọc xong hết thì làm gì

1. **Trước buổi gặp:** tự trả lời bảng trên. Câu nào chưa trả lời được thì hỏi tôi. Bấm **"Làm lại từ đầu"** trên Màn minh hoạ để dữ liệu demo về ban đầu.
2. **Trong buổi gặp anh Đạt:**
   - trình bày theo slide, demo theo bảng ở B2;
   - xin anh Đạt **duyệt hướng đi** trước;
   - hỏi lần lượt 8 câu ở mục 12. Cách tiện nhất: mở màn minh hoạ, menu **Câu hỏi cần chốt** (`minh-hoa-tao-dot-kiem-ke.html?man=cau`). Mỗi câu có nút mở đúng màn demo; ghi câu trả lời ngay dưới mỗi câu, họp xong bấm **Chép câu trả lời** rồi gửi tôi.
   - Nếu anh Đạt hỏi "nhân viên nào chưa được kiểm": trong một đợt là tab **Xác nhận** ở chi tiết đợt; nhiều đợt là menu **Báo cáo kiểm kê**, tab **Theo nhân viên**.
3. **Sau buổi gặp:** gửi tôi câu trả lời của anh Đạt cho từng câu. Tôi sẽ:
   - cập nhật trang phân tích: chuyển các câu đã có trả lời sang "Đã chốt" và gỡ nhãn ❓;
   - sửa Màn minh hoạ theo đúng câu trả lời (ví dụ "kho chưa rõ");
   - đếm số liệu thật cho câu 2, câu 3 và kho chưa rõ nếu bạn cấp dump hoặc kết nối DB chỉ đọc;
   - rồi mới làm thiết kế DB và API theo mô hình mới, gửi bên app trước khi code.
