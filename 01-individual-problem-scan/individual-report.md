Quân, là kỹ sư AI và cũng là gia sư tự do tại nhà ở thành phố Hồ Chí Minh. Mỗi tuần anh ấy phải cân bằng với việc đi dạy và đi làm trên công ty.    

# 01 — Individual Problem Scan

## Scan rộng
| # | Lăng kính | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Học sinh nhắn tin hỏi trùng lặp các bài toán | Gia sư, Học sinh | Lặp lại 4-5 lần/tuần, mất 15-20 phút/lần |
| 2 | Lặp lại | Soạn và cá nhân hóa bài tập về nhà cho từng học sinh theo trình độ khác nhau | Gia sư | Mất khoảng 90 phút/ngày (cuối ngày) |
| 3 | Thời gian | Học sinh đặt nhiều câu hỏi trùng với thời gian Gia sư đang làm việc | Gia sư, Học sinh | Học sinh phải chờ reply 1-2 tiếng hoặc ngâm bài |
| 4 | Tốn thời gian | Chấm điểm & viết nhận xét chi tiết bài tập về nhà cho nhiều học sinh | Gia sư, Học sinh | Mất khoảng 120-180 phút/ngày |
| 5 | Tốn thời gian | Di chuyển giữa các nhà học sinh trong giờ cao điểm ở TP.HCM bị kẹt xe | Gia sư | Mất 45-60 phút/buổi di chuyển |
| 6 | AI có thể tốt hơn | Giải đáp thắc mắc và gợi ý từng bước (hint) cho học sinh khi tự học ở nhà | Gia sư, Học sinh | Học sinh phải chờ reply 1-2 tiếng hoặc ngâm bài |
| 7 | AI có thể tốt hơn | Tổng hợp tình hình học tập hàng tuần để báo cáo cho Phụ huynh | Gia sư, Phụ huynh | Mất 15-20 phút/học sinh, hay bị dồn vào cuối tuần |
| 8 | Khó khăn từ người khác | Trễ hạn thanh toán học phí hoặc quên đối chiếu số buổi đã học | Gia sư | Phải mất thời gian dò lại lịch sử dạy, tự soạn tin nhắn nhắc nhở tế nhị vào cuối tháng; đôi khi bị lệch số buổi giữa hai bên.
| 9 | Khó khăn từ người khác | Học sinh thường hay quên kiến thức sau 1 thời gian không ôn tập | Gia sư, Học sinh | Học sinh thường hay hỏi lại các kiến thức đã được học trong các buổi trước đó |
| 10 | Khó khăn từ người khác | Học sinh không hoàn thành bài tập về nhà hoặc làm đối phó sát giờ học | Gia sư, Học sinh | Tốn 20-30 phút đầu buổi học chỉ để chữa cháy, nhắc lại kiến thức cũ thay vì học bài mới, ảnh hưởng đến lộ trình đã lên sẵn.

## Top 3 nên chọn

| Rank | Problem | Bài toán gốc (Top 10) | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|---|
| 1 | **Hỗ trợ Q&A & Gợi ý tự học ngoài giờ** | Problem #3 & #6: Học sinh hỏi bài ngoài giờ / Gia sư đang làm việc, cần gợi ý hint tức thì | • Pain point thực tế & cấp thiết: Trực tiếp giải phóng quỹ thời gian bị cắt vụn trong giờ hành chính.<br>• AI có thế mạnh vượt trội: LLM đóng vai trò gia sư ảo gợi ý từng bước (hint) giúp học sinh tự tư duy thay vì cho đáp án trực tiếp.<br>• Tối ưu thời gian chờ của học sinh. | Quality improvement khó đo chính xác (Học sinh thực sự hiểu bài nhờ gợi ý hay chỉ cố trick AI để lấy đáp án?). |
| 2 | **Tự động hóa Vòng đời Bài tập về nhà (Soạn - Chấm - Nhận xét)** | Problem #2 & #4: Soạn bài tập cá nhân hóa & Chấm bài kèm nhận xét chi tiết | • Nỗi đau lớn nhất & Tốn nhiều thời gian nhất: Đang ngốn từ 3 - 4.5 tiếng/ngày vào cuối ngày.<br>• Cá nhân hóa cao: Tạo bài tập theo trình độ từng học sinh và đưa phản hồi tức thì.<br>• Impact trực tiếp và đo lường được đến chất lượng giảng dạy. | Scope dự án có thể quá rộng; việc xử lý dữ liệu/format bài làm của học sinh (ảnh chụp chữ viết tay, công thức) có khó khăn. |
| 3 | **Tổng hợp & Báo cáo tiến độ cho Phụ huynh** | Problem #7: Tổng hợp tình hình học tập hàng tuần để báo cáo cho Phụ huynh | • Workflow rõ ràng, dễ chuẩn hóa: Dữ liệu đầu vào từ các buổi học đã có sẵn.<br>• Giải quyết tình trạng dồn việc cuối tuần: Giảm bớt 15-20 phút/học sinh mỗi tuần.<br>• Tăng tính chuyên nghiệp và sự tin tưởng từ phía Phụ huynh. | Tiêu chuẩn đánh giá giọng văn và chất lượng báo cáo ("đủ hay, đủ chi tiết và cá nhân hóa") khó định lượng rõ ràng. |

## Problem Card #1

**Problem 1 câu:**  
Trong giờ hành chính khi Quân đang làm việc tại công ty, học sinh thường gửi 4-5 thắc mắc bài tập/tuần khiến học sinh phải chờ trả lời 1-2 tiếng (gián đoạn tư duy), còn Quân bị cắt vụn thời gian làm việc.

**Actor:**  
Gia sư tự do (Quân - Kỹ sư AI) và Học sinh tự học bài tại nhà.

**Thời điểm / bối cảnh:**  
Giờ hành chính (khi Quân đang làm việc ở công ty) hoặc buổi tối khi học sinh tự làm bài tập về nhà và gặp bài toán khó.

**Current workflow:**

```text
1. Học sinh gặp bài toán khó/vướng mắc khi tự học
2. Học sinh chụp ảnh hoặc nhắn tin câu hỏi qua Zalo/Messenger cho Gia sư
3. Gia sư nhận thông báo trong giờ làm việc tại công ty
4. Gia sư phải tạm dừng công việc hoặc tạm hoãn trả lời (học sinh chờ 1-2 tiếng)
5. Gia sư đọc đề bài, suy nghĩ hướng giải và soạn tin nhắn gợi ý từng bước (hint)
6. Học sinh đọc tin nhắn phản hồi và tiếp tục tự giải bài
```

**Bottleneck:**  
Bước 4 & 5 — Gia sư không thể phản hồi ngay lập tức do bận giờ làm việc công ty; đồng thời việc suy nghĩ và soạn gợi ý từng bước (hint) làm xao nhãng và cắt vụn thời gian làm việc của Quân (mất 15-20 phút/lần).

**Impact:**  
Mất khoảng 60-100 phút/tuần thời gian làm việc của Quân. Học sinh bị nản hoặc đứt gãy mạch suy nghĩ do phải chờ reply quá lâu (1-2 tiếng).

**Success metric:**  
Giảm thời gian phản hồi thắc mắc từ 1-2 tiếng xuống dưới 2 phút (qua AI Hint Bot); giảm 80% số lượt câu hỏi Quân phải trực tiếp can thiệp trả lời trong giờ làm việc mà vẫn đảm bảo học sinh hiểu bài.

**Non-AI alternative:**  
Quy định khung giờ cố định chỉ trả lời tin nhắn (ví dụ 20h-21h) hoặc soạn trước bộ PDF lời giải chi tiết. Tuy nhiên, cách này làm mất tính tức thì khi học sinh cần gợi ý để làm tiếp và lời giải chi tiết dễ khiến học sinh chép đáp án thay vì tự tư duy.

**AI hypothesis:**  
AI đóng vai trò "Gia sư ảo 24/7" (tích hợp LLM + RAG tài liệu giảng dạy), tự động phân tích câu hỏi/hình ảnh đề bài của học sinh và đưa ra các gợi ý theo dạng câu hỏi gợi mở (hints) từng bước, giúp học sinh tự tư duy giải bài mà không đưa ngay đáp án trực tiếp. Quân chỉ cần review các case khó.

**Quick gut:**  
Workflow + AI Assistant (Retrieval & Hint Generation).

### Draft current workflow

```text
CURRENT STATE — 1-2 tiếng chờ / 20 phút xử lý

[1 Học sinh gặp bài khó & nhắn câu hỏi: 2']
→ [2 Gia sư nhận thông báo trong giờ làm việc: 1']
→ [3 Gia sư bận việc / tạm hoãn trả lời: 60-120' ngâm bài]  <-- bottleneck (học sinh phải chờ)
→ [4 Gia sư mở tin nhắn, đọc đề bài: 3']
→ [5 Gia sư suy nghĩ hướng giải & soạn hint: 15']      <-- bottleneck (gia sư mất thời gian)
→ [6 Gửi tin nhắn gợi ý cho học sinh: 1']
```

### Draft future workflow

```text
FUTURE STATE — dưới 2 phút

[1 Học sinh gửi đề bài/câu hỏi: 30s]
→ [2 AI phân tích đề bài & tra cứu tài liệu (RAG): 30s]
→ [3 AI tự động soạn & gửi gợi ý từng bước (hint): 30s]
→ [4 Học sinh đọc hint & tiếp tục tự làm bài: 2']
→ [5 Gia sư review lại log câu hỏi (nếu cần): 2' cuối ngày]  <-- human boundary

Fallback: AI đưa hint chưa phù hợp / Học sinh bấm "Vẫn chưa hiểu" → Chuyển notification để Gia sư hỗ trợ trực tiếp.
```

---

## Problem Cards #2 và #3 — tóm tắt

| Card | Actor | Bottleneck | Metric | Quick gut | Vì sao chưa chọn làm #1 |
|---|---|---|---|---|---|
| **#2 Vòng đời Bài tập về nhà** | Gia sư | Soạn bài tập cá nhân hóa theo trình độ & Chấm bài, viết nhận xét chi tiết từng câu | 3-4.5 tiếng/ngày → 45 phút/ngày | Workflow + Generative AI | Scope dự án quá lớn (cần xử lý OCR chữ viết tay, hình ảnh, bài giải); Data access phức tạp. |
| **#3 Báo cáo Phụ huynh** | Gia sư | Tổng hợp dữ liệu số buổi, kết quả bài tập & viết nhận xét cá nhân hóa hàng tuần cho từng phụ huynh | 15-20 phút/học sinh → 3-5 phút/học sinh | Workflow / Automation | Tiêu chuẩn đánh giá giọng văn ("nhận xét đủ hay, đủ tinh tế và cá nhân hóa") khó định lượng hơn. |

