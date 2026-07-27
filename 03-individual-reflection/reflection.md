# 03 — Individual Reflection

## Đóng góp của Quân trong nhóm

| Hoạt động | Quân đã làm gì? | Kết quả |
|---|---|---|
| Scan cá nhân | Đưa ra 10 problems từ góc nhìn thực tế của Gia sư & Kỹ sư AI (Q&A ngoài giờ, soạn/chấm bài tập, báo cáo phụ huynh...) | Đưa Candidate "Trợ lý cho gia sư và học sinh" vào danh sách 3 candidate thảo luận của nhóm |
| Pitch | Pitch Candidate "Trợ lý gia sư và học sinh" (tự động hóa sắp lịch và hỗ trợ Q&A học sinh) | Bài được đưa vào shortlist 3 candidate của nhóm |
| Challenge | Thảo luận và cùng nhóm phân tích Candidate gia sư | Nhóm chỉ ra candidate bị gộp 2 workflow khác nhau (Sắp lịch & Q&A học sinh), giúp nhận ra rủi ro khi chưa thu hẹp được bottleneck |
| Workflow | Đóng góp tư duy bóc tách các bước trong current/future workflow | Nhóm áp dụng cách phân tách chi tiết từng bước (Input/Output/Handoff/Bottleneck) sang bài toán chọn chính (AI Gym Coach) |
| Research | Nghiên cứu lăng kính giải pháp (Rule vs Workflow vs Agent) và các sản phẩm tham chiếu (Kaia Motion Coach, Tempo Studio) | Nhóm nhận ra không cần build Agent phức tạp từ đầu mà chọn mô hình Workflow hẹp |
| Rule / Workflow / Agent | Lập luận chọn Workflow, phản biện việc chọn Agent quá sớm | Nhóm thống nhất chọn mức Workflow (Camera check -> Pose estimation -> Rule rubric -> Cue ngắn) và đưa ra quyết định Not Yet |

## Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì |
|---|---|---|---|---|
| Scan | Gợi ý bổ sung các pain point lặp lại/tốn thời gian theo vai trò gia sư | Giúp mở rộng lăng kính quan sát các vấn đề lặp lại khi dạy học và đi làm | Gợi ý một số bài toán quá rộng (như kẹt xe giờ cao điểm) không phù hợp giải bằng AI | Lọc giữ các bài toán có workflow rõ ràng (Q&A ngoài giờ, chấm bài tập, báo cáo phụ huynh) |
| Workflow | Nhờ AI chuyển mô tả các bước thành sơ đồ dạng quy trình | Giúp hình dung nhanh chuỗi thao tác Current State và Future State | AI có xu hướng gộp bước xử lý và bỏ qua các bước kiểm tra ranh giới (Camera check, Confidence gate) | Tách nhỏ thành các bước chi tiết có Human Boundary, kiểm tra confidence và phương án Fallback rõ ràng |
| Research | Tìm kiếm sản phẩm tương tự trên thị trường (Kaia, Tempo...) | Tổng hợp nhanh mô hình kỹ thuật và cách các ứng dụng xử lý chuyển động | Đưa ra một số nhận định tiết kiệm thời gian mà không có nguồn kiểm chứng | Chỉ giữ các thông tin chính thức, rút ra bài học về camera setup và confidence check thay vì copy nguyên bản |
| Problem Statement | Nhờ AI đóng vai trò phản biện các field còn mơ hồ | Chỉ ra các metric chưa được đo lường thực tế và rủi ro false alert | AI đề xuất chuyển bài toán thành Agent tự động lập kế hoạch tập luyện quá sớm | Giữ nguyên mức chọn Workflow, giới hạn scope ở 1 bài bodyweight squat và bổ sung điều kiện Not Yet |

## Bài học của Quân

- **Problem tốt phải có workflow và bottleneck cụ thể:** Bài toán gia sư ban đầu bị gộp 2 workflow khác nhau (sắp xếp lịch và hỏi đáp Q&A), làm cho actor và metric bị mờ nhạt. Khi bóc tách rõ từng workflow mới tìm đúng bottleneck cần giải quyết.
- **Phân định rõ Rule, Workflow và Agent:** Không phải bài toán AI nào cũng cần build Agent. Với các bài toán vận động hay giáo dục, mô hình Workflow tuyến tính kết hợp Rule rubric và Confidence gate sẽ an toàn và thực tế hơn Agent tự quyết.
- **Dữ liệu và Baseline là điều kiện tiên quyết:** Không thể chốt "Go" khi chưa có observed test thật và chưa đo được baseline. Quyết định "Not Yet" thể hiện sự chặt chẽ trong việc kiểm chứng giả thuyết sản phẩm.
- **AI chỉ đóng vai trò hỗ trợ draft:** Con người (Gia sư, PT, người dùng) bắt buộc phải đóng vai trò định nghĩa rubric, thiết lập ranh giới an toàn (Human Boundary) và kiểm tra chất lượng cuối cùng.

Nếu làm lại:

```text
Tôi sẽ bóc tách bài toán Gia sư thành 2 Problem Card độc lập (Card Hỗ trợ Q&A ngoài giờ và Card Sắp xếp lịch) ngay từ bước Scan cá nhân thay vì gộp chung, để khi pitch với nhóm có một bottleneck duy nhất, sắc nét và có success metric dễ đo lường hơn.
```
