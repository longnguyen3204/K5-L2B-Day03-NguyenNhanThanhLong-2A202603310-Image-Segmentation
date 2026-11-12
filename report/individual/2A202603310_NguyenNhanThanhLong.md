# Báo cáo thực hành Day 3 — điền trực tiếp trong fork của bạn

- Mã học viên theo lớp: 2A202603310
- Ngày / CVAT local: 11/11/2026
- Công cụ đã dùng: CVAT

## 1. Bài đã nộp

Ghi tên ZIP đúng như file trong `submissions/` và số ảnh đã vẽ, Save. Chưa làm hoặc export lỗi thì ghi `chưa có`, không tạo ZIP rỗng. Cột điểm là điểm tối đa của task, **không phải điểm tự chấm**.

| Task | File ZIP đúng tên | Hoàn thành mấy ảnh | Điểm tối đa (coach chấm sau) |
| --- | --- | ---: | ---: |
| easy_semantic | easy_semantic.zip | 3 / 3 | 20 |
| medium_instance | medium_instance.zip | 3 / 3 | 32 |
| hard_panoptic | hard_panoptic | 2 / 2 | 30 |
| cp1_holes | chưa có | 0 / 1 | 3 |
| cp2_slice | chưa có | 0 / 1 | 3 |
| cp5_occlusion | chưa có | 0 / 1 | 3 |
| cp3_thin | chưa có | 0 / 1 | 3 |
| cp4_curb | chưa có | 0 / 1 | 3 |
| cp6_coverage | chưa có | 0 / 1 | 3 |
| **Tổng tối đa** | | 8 | **100** |

## 2. Một quyết định trước khi dùng gợi ý

Chọn object đầu tiên bạn tự vẽ ở `medium_instance`, trước khi xem bất kỳ đề xuất tự động nào cho object đó. Ghi ảnh/vị trí đủ để tìm lại; “quy tắc biên” là lý do bạn chọn hoặc dừng mask ở ranh đó.

- Ảnh, vị trí và object Medium đầu tiên tự vẽ: ảnh: 000000181542.jpg, object: người phụ nữ.
- Class và quy tắc tôi dùng để chọn biên: class: person
- Nếu dùng gợi ý sau đó: vùng gợi ý đúng; hành động giữ và lý do: giữ nguyên phần mask tự động của người phụ nữ

## 3. Một lỗi tôi tìm thấy và sửa

- Task/ảnh/vùng: Task gán nhãn Instance Segmentation / Ảnh 000000181542.jpg / Vùng tay áo trái (góc phải của object) và khu vực tà áo phía dưới của người phụ nữ.
- Lỗi thuộc loại: sai lớp / thiếu-thừa vật / gộp-tách / biên / phủ vùng / khác: Biên & Thừa vật
- Bằng chứng tôi nhìn thấy: Khi dùng công cụ tự động bắt biên của OpenCV, đường viền ở phần tà áo dài rủ xuống gần bánh trước xe máy bị kéo lẹm sang vùng tối của lốp xe. Ngoài ra, ở vùng mép tay áo bên phải ảnh, đường biên đi hơi rộng, bao trùm cả phần pixel bóng mờ tiếp giáp với mặt đường/xe phía sau.
- Quy tắc và hành động sửa: Ranh giới của class person chỉ bao gồm cơ thể và trang phục thuộc về người đó, không bao gồm bóng đổ hay vật thể giao cắt phía sau. Chuyển sang chế độ chỉnh sửa điểm, giữ phím Shift để xóa bớt các điểm neo bị lẹm vào bánh xe máy, sau đó kéo sát các điểm viền ôm đúng theo nếp gấp vải áo dài và bàn chân.
- Sau sửa đã Save và export lại chưa? Đã bấm Save và export.

## 4. Ba ca chưa chắc hoặc đã cân nhắc

Mỗi ca là một **vùng cụ thể** khiến bạn phải cân nhắc hai cách hiểu. Ghi dấu hiệu nhìn thấy hoặc quy tắc đã dùng, rồi nêu quyết định hoặc câu hỏi cho coach. Không cần ba lỗi; ca đã quyết định được cũng hợp lệ.

| Ảnh/vị trí | Hai cách hiểu có thể | Quy tắc/chứng cứ | Quyết định hoặc câu hỏi cho coach |
| --- | --- | --- | --- |
| 1 | … | … | … |
| 2 | … | … | … |
| 3 | … | … | … |
