# 02 — Group Problem Statement

## Thành viên nhóm

https://docs.google.com/spreadsheets/d/1kX_tFy11pHg4HhjHPoy0xwzTR06p4niJp6rQ1tuqks8/edit?gid=0#gid=0

## Phase 3 — Group Convergence

### Bước 3.1 — Trình bày ba candidate cuối của team

Sau khi mỗi thành viên pitch các Problem Card cá nhân, nhóm đưa ba candidate dưới đây vào vòng thảo luận cuối:

- Candidate 1 — AI Gym Coach
  - Problem: Người mới tập gym không biết rep nào cần chú ý và phải sửa gì khi tự tập
  - Actor: Người mới tập 0–12 tháng, không có PT theo sát
  - Workflow: Xem mẫu → quay một set → tua lại video → vẫn tự đoán rep nào sai
  - Bottleneck: Khó tìm đúng rep và hiểu cue cần áp dụng
  - AI hypothesis ban đầu: AI Gym Coach nhận diện từng rep, đánh dấu rep cần xem và đưa một cue ngắn

- Candidate 2 — Giải thích phiếu xét nghiệm
  - Problem: Bệnh nhân nhận phiếu xét nghiệm nhưng không hiểu thuật ngữ, chỉ số và khoảng tham chiếu
  - Actor: Bệnh nhân, nhất là người lớn tuổi hoặc không có kiến thức y khoa
  - Workflow: Nhận phiếu → tự tìm từng chỉ số → đọc nhiều nguồn → hoang mang → hỏi lại bác sĩ
  - Bottleneck: Khó diễn giải thông tin đúng với ngữ cảnh
  - AI hypothesis ban đầu: AI Agent giải thích thuật ngữ và hỗ trợ chuẩn bị câu hỏi cho bác sĩ

- Candidate 3 — Trợ lý cho gia sư và học sinh
  - Problem: Gia sư mất thời gian sắp xếp lịch và trả lời các câu hỏi cơ bản lặp lại của học sinh
  - Actor: Gia sư và học sinh
  - Workflow: Trao đổi lịch qua chat → đổi lịch nhiều vòng → gia sư trả lời lại các câu hỏi cơ bản
  - Bottleneck: Candidate đang gộp hai workflow khác nhau là sắp lịch và hỏi đáp
  - AI hypothesis ban đầu: AI Agent hỗ trợ sắp lịch và làm trợ lý hỏi đáp cơ bản

### Bước 3.2 — Cluster

Ba candidate không trùng về domain nhưng cùng có một pattern là người dùng thiếu hỗ trợ đúng thời điểm trong một workflow đang phải xử lý thủ công. AI Gym Coach thuộc nhóm feedback kỹ năng theo ngữ cảnh vì người tập đang thực hiện động tác nhưng không tự nhìn ra điểm cần sửa. Bài toán phiếu xét nghiệm thuộc nhóm giải thích thông tin chuyên môn vì bệnh nhân đọc được dữ liệu nhưng không hiểu ý nghĩa và cần boundary rõ với bác sĩ. Bài toán gia sư thuộc nhóm điều phối và hỏi đáp giáo dục vì có nhiều trao đổi lặp lại qua chat, tuy nhiên candidate này đang gộp hai pain và hai workflow khác nhau

### Bước 3.3 — Shortlist

- Người mới không nhận ra điểm cần sửa khi tự tập gym
  - Vì sao vào shortlist: Workflow có thể quan sát, bottleneck rõ, có thể pilot bằng một bài bodyweight squat và đo bằng rubric của PT
  - Rủi ro / điều chưa rõ: Camera một góc có thể không thấy đủ cơ thể; feedback sai có thể ảnh hưởng người tập

- Bệnh nhân không hiểu phiếu xét nghiệm
  - Vì sao vào shortlist: Actor và impact xã hội rõ, pain có thể quan sát qua việc tự tra cứu và hỏi lại bác sĩ
  - Rủi ro / điều chưa rõ: Thông tin phụ thuộc tuổi, giới tính, bệnh sử và mẫu xét nghiệm; team không có chuyên môn y khoa đủ sâu

- Gia sư phải sắp lịch và trả lời câu hỏi cơ bản lặp lại
  - Vì sao vào shortlist: Tần suất lặp cao, có thể so sánh Rule, Workflow và Agent
  - Rủi ro / điều chưa rõ: Candidate đang gộp scheduling với Q&A nên actor, bottleneck và success metric chưa thống nhất

### Bước 3.4 — Score để đồng thuận

Điểm từ 1–5 dùng để ép nhóm nói rõ lý do chứ không thay thế thảo luận. `Pain có evidence` hiện chỉ là đánh giá sơ bộ vì team chưa bổ sung interview hoặc survey thật

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Không nhận ra điểm cần sửa khi tự tập gym | 5 | 5 | 3 | 5 | 4 | 5 | 4 | **31** |
| Không hiểu phiếu xét nghiệm | 5 | 4 | 3 | 5 | 3 | 4 | 2 | **26** |
| Sắp lịch gia sư + Q&A học sinh | 3 | 3 | 2 | 4 | 4 | 5 | 4 | **25** |

**Candidate nhóm chọn:** Người mới tập gym không biết rep nào cần chú ý, dấu hiệu nào đang lặp lại và phải thử điều chỉnh gì ở rep tiếp theo khi tập một mình

*Vì sao chọn:* Actor, current workflow và bottleneck đều cụ thể hơn hai candidate còn lại. Nhóm có thể thu nhỏ thành bodyweight squat, đo thời gian tìm rep, mức đồng thuận với PT, khả năng hiểu cue và mức thay đổi giữa các set

*Vì sao không chọn candidate giải thích phiếu xét nghiệm:* Impact lớn nhưng rủi ro y khoa cao, thông tin cần nhiều context cá nhân và team chưa có chuyên gia chịu trách nhiệm nội dung. Bài này cũng chưa chứng minh cần Agent thay vì phiếu dễ hiểu, glossary và workflow có bác sĩ review

*Vì sao không chọn candidate gia sư và học sinh:* Candidate đang gộp hai vấn đề khác nhau là scheduling và Q&A. Scheduling có thể chỉ cần Calendar + Rule, còn Q&A cần nguồn học liệu và metric chất lượng riêng nên nhóm chưa xác định được bottleneck duy nhất


## Phase 4 — Quick Validation + Research giải pháp

### Bước 4.1 — Quick validation

- Interview người tập 0–12 tháng
  - Số người / số mẫu: 5
  - Tín hiệu xác nhận cần tìm: Họ có thường quay video, mất bao lâu để tìm rep cần xem và có hiểu mình phải sửa gì ở rep tiếp theo không
  - Tín hiệu phản bác: Họ đã có PT, dùng gương là đủ hoặc không muốn bật camera
  - Nhóm sẽ sửa problem thế nào: Thu hẹp actor hoặc chuyển về video/checklist

- Interview PT
  - Số người / số mẫu: 2
  - Tín hiệu xác nhận cần tìm: Ba lỗi nào của squat có thể quan sát ổn định từ một góc camera
  - Tín hiệu phản bác: PT không đồng ý dùng một ngưỡng chung cho mọi người
  - Nhóm sẽ sửa problem thế nào: Dùng rubric theo khoảng và chỉ feedback cue an toàn

- Observed test squat không tạ
  - Số người / số mẫu: 5
  - Tín hiệu xác nhận cần tìm: Người dùng có đặt camera đúng, hiểu cue và sửa được ở rep sau không
  - Tín hiệu phản bác: Che khuất khớp, camera sai góc, cue làm mất tập trung
  - Nhóm sẽ sửa problem thế nào: Thêm bước kiểm tra camera hoặc dừng real-time feedback

#### Evidence từ desk research

- Nghiên cứu app sửa squat trên điện thoại
  - Tín hiệu xác nhận: Một thử nghiệm nhỏ với 20 người mới tập cho thấy nhóm dùng feedback từ app cải thiện kỹ thuật squat tốt hơn nhóm chỉ xem video
  - Tín hiệu phản bác / giới hạn: Mẫu nhỏ, chỉ tập trung vào squat và không chứng minh hệ thống phù hợp cho mọi bài tập
  - Nhóm sửa problem thế nào: Pilot chỉ một bài squat không tạ

- Kaia Motion Coach và Tempo
  - Tín hiệu xác nhận: Computer vision có thể theo dõi landmark và đưa feedback, tức hướng kỹ thuật là khả thi
  - Tín hiệu phản bác / giới hạn: Tempo yêu cầu góc nhìn, khoảng cách, ánh sáng và không bị che khuất; thiết bị vẫn có thể sai
  - Nhóm sửa problem thế nào: Bắt buộc kiểm tra camera và confidence trước khi feedback

- Nghiên cứu feedback khi resistance training
  - Tín hiệu xác nhận: Visual hoặc verbal feedback có thể hỗ trợ performance và kỹ thuật
  - Tín hiệu phản bác / giới hạn: Feedback máy không phải lúc nào cũng tốt hơn feedback từ người thật
  - Nhóm sửa problem thế nào: Không định vị hệ thống là PT thay thế

Insight sau desk research: Pain không phải là người dùng thiếu thêm một video hướng dẫn
Pain nằm ở việc video không nhìn thấy rep hiện tại của họ và không phản hồi đúng lúc
Tuy nhiên camera một góc cũng không nhìn thấy toàn bộ cơ thể trong mọi điều kiện, vì vậy scope phải hẹp và có fallback rõ

### Bước 4.2 — Research giải pháp đã có

- Kaia Motion Coach 
  - Họ giải quyết phần nào: Dùng camera trước của điện thoại hoặc tablet để theo dõi landmark, đánh giá movement/posture và đưa feedback nghe nhìn theo thời gian thực
  - Điểm mạnh: Không yêu cầu wearable hoặc cảm biến riêng
  - Khoảng trống / rủi ro: Là sản phẩm cho vận động và MSK care, không chứng minh mọi cue đều phù hợp với gym tự do
  - Bài học cho nhóm: Smartphone camera có thể đủ cho prototype nhưng cần scope bài tập rõ

- Tempo Studio 
  - Họ giải quyết phần nào: Dùng cảm biến 3D để đếm rep và hỗ trợ form guidance
  - Điểm mạnh: Có hardware và trải nghiệm tập tích hợp
  - Khoảng trống / rủi ro: Cần toàn thân không bị che, đúng khoảng cách, đúng hướng và ánh sáng phù hợp; hướng dẫn cũng nói metric có thể sai
  - Bài học cho nhóm: Camera setup và confidence check là một phần bắt buộc của workflow

Research takeaway: Không nên build một Agent tự chọn bài, tăng tạ và quyết định thay PT
Hướng phù hợp hơn là một Workflow hẹp: camera → pose landmarks → rule theo rubric → một cue ngắn → người tập tự điều chỉnh



## Phase 5 — Workflow + Problem Statement

### Bước 5.1 — Current workflow 

```
CURRENT STATE — quay 10 rep rồi tự xem lại

[1 Chọn bài squat từ video hoặc chương trình trên mạng]
→ [2 Xem mẫu và cố nhớ các điểm cần chú ý]
→ [3 Dựa điện thoại vào chai nước/tripod rồi bấm quay]
→ [4 Thực hiện khoảng 10 rep]
→ [5 Dừng tập và tua lại gần như toàn bộ video]  <-- bottleneck
→ [6 Vẫn không chắc rep nào sai và phải sửa điều gì]
→ [7 Tập set tiếp theo hoặc chờ hỏi PT/người quen]

Feedback latency: sau set, sau buổi tập hoặc không có
Tổng thời gian chủ động giả định: khoảng 7–17 phút cho set đầu, chưa tính thời gian chờ PT
```

- Bước 1 — Chọn bài tập
  - Actor: Người tập
  - Input: Mục tiêu buổi tập, video hoặc chương trình online
  - Output: Chọn bodyweight squat
  - Thời gian/tần suất: 1–2 phút, mỗi buổi
  - Handoff: Bài đã chọn được chuyển sang bước xem mẫu
  - Bottleneck: Không

- Bước 2 — Xem mẫu và ghi nhớ cue
  - Actor: Người tập
  - Input: Video mẫu và các cue chung
  - Output: Các cue người tập cố ghi nhớ
  - Thời gian/tần suất: 1–3 phút, mỗi buổi
  - Handoff: Cue trong trí nhớ được mang sang bước setup/tập
  - Bottleneck: Có thể quên cue khi bắt đầu vận động

- Bước 3 — Đặt camera
  - Actor: Người tập
  - Input: Điện thoại, chai nước hoặc tripod
  - Output: Góc quay dự kiến thấy toàn thân
  - Thời gian/tần suất: 1–2 phút, mỗi set
  - Handoff: Góc quay được dùng để ghi video set
  - Bottleneck: Chưa biết camera có thấy đủ khớp không

- Bước 4 — Thực hiện set
  - Actor: Người tập
  - Input: Bài squat, cue đã nhớ và góc quay
  - Output: Video một set khoảng 10 rep
  - Thời gian/tần suất: 30–90 giây, mỗi set
  - Handoff: Video cả set được chuyển sang bước review
  - Bottleneck: Không có feedback trong lúc thực hiện

- Bước 5 — Tua video và tìm rep cần xem
  - Actor: Người tập
  - Input: Video cả set
  - Output: Một hoặc vài rep người tập nghi ngờ cần xem
  - Thời gian/tần suất: 2–5 phút, mỗi set
  - Handoff: Rep nghi ngờ được chuyển sang bước tự diễn giải
  - Bottleneck: Điểm nghẽn chính vì phải tua nhiều lần nhưng vẫn có thể chọn sai rep

- Bước 6 — Tự diễn giải
  - Actor: Người tập
  - Input: Rep vừa tìm được và kiến thức cá nhân
  - Output: Nhận định chưa chắc chắn về dấu hiệu/cue
  - Thời gian/tần suất: 1–3 phút, mỗi set
  - Handoff: Nhận định được dùng cho set sau hoặc gửi cùng video cho PT
  - Bottleneck: Người mới không chắc mình hiểu đúng

- Bước 7 — Tập tiếp hoặc hỏi PT
  - Actor: Người tập hoặc PT
  - Input: Video, rep nghi ngờ và câu hỏi
  - Output: Tập tiếp, dừng hoặc nhận feedback muộn
  - Thời gian/tần suất: Ngay sau set hoặc phải chờ PT
  - Handoff: Feedback quay lại người tập ở set sau/buổi sau
  - Bottleneck: Handoff ra PT có thể chậm hoặc không xảy ra

**Bottleneck chính:** Người tập phải dừng buổi tập và tua lại cả set nhưng vẫn không biết chính xác rep nào cần chú ý, dấu hiệu nào đang xảy ra và nên thử thay đổi điều gì ở rep tiếp theo


### Bước 5.2 — Future workflow

```
FUTURE STATE — pilot chỉ cho bodyweight squat

[1 Người tập chọn squat và đọc safety note]
→ [2 Camera check: đủ sáng, toàn thân trong khung, đúng góc]
→ [3 Người tập thực hiện set; AI nhận diện chuyển động và tách từng rep]
→ [4 Confidence gate kiểm tra có đủ dữ liệu hay không]
→ [5 Rule so sánh dấu hiệu với rubric do PT xác nhận]
→ [6 Hệ thống đánh dấu rep và đưa tối đa 1 cue ngắn]
→ [7 Người tập thử điều chỉnh ở rep tiếp theo]
→ [8 Sau set xem đúng rep cần chú ý và summary tiến bộ]

Human boundary:
- PT định nghĩa và duyệt rubric
- Người tập tự quyết định tiếp tục, dừng lại hoặc hỏi chuyên gia
- Người tập phải dừng khi đau, chóng mặt hoặc mất thăng bằng
- Hệ thống không chẩn đoán chấn thương, không tăng tạ và không thay PT

Fallback:
- Confidence thấp, khớp bị che hoặc camera sai góc → không đưa cue
- App hướng dẫn đặt lại camera hoặc chuyển sang phân tích sau set
- Điện thoại xử lý chậm → vẫn đánh dấu rep sau set nhưng không feedback real-time
- Tripod/giá đỡ dùng cho bài cố định; gimbal chỉ là phụ kiện tùy chọn
```

- Bước 1 — Chọn bài và xác nhận boundary
  - Owner: Người thực hiện
  - Actor: Người tập
  - Input: Mục tiêu buổi tập và safety note
  - Output: Chọn bodyweight squat, xác nhận boundary
  - Thời gian/tần suất: 20–30 giây, mỗi buổi
  - Handoff / boundary: Chuyển bài đã chọn sang camera check; người tập vẫn có quyền dừng

- Bước 2 — Kiểm tra camera
  - Owner: Người + Rule
  - Actor: Người tập và camera check
  - Input: Live frame, ánh sáng, góc quay
  - Output: Pass/fail điều kiện camera
  - Thời gian/tần suất: 30–90 giây, mỗi set
  - Handoff / boundary: Không đạt thì đặt lại máy hoặc phân tích sau set; đạt mới chuyển video cho AI

- Bước 3 — Thực hiện set và nhận diện pose
  - Owner: Người + AI
  - Actor: Người tập và pose/rep model
  - Input: Bài bodyweight squat và video stream đã qua camera check
  - Output: Video set, từng rep và pose landmarks
  - Thời gian/tần suất: 30–90 giây, mỗi set
  - Handoff / boundary: Người thực hiện động tác; AI chỉ xuất rep/landmarks/confidence sang Rule, không tự kết luận đúng sai

- Bước 4 — Kiểm tra confidence
  - Owner: Rule
  - Actor: Confidence gate
  - Input: Landmarks và confidence
  - Output: Cho phép chấm hoặc no-cue
  - Thời gian/tần suất: Dưới 1 giây, mỗi rep
  - Handoff / boundary: Confidence thấp thì không đưa cue và chuyển rep sang summary

- Bước 5 — Đối chiếu rubric
  - Owner: Rule
  - Actor: Rule engine
  - Input: Ba dấu hiệu được hỗ trợ và rubric PT
  - Output: Dấu hiệu cần chú ý hoặc không có lỗi
  - Thời gian/tần suất: Dưới 1 giây, mỗi rep
  - Handoff / boundary: Chỉ được dùng rubric/cue do PT duyệt

- Bước 6 — Đánh dấu rep và hiển thị cue
  - Owner: Rule / giao diện
  - Actor: Hệ thống
  - Input: Dấu hiệu, timestamp và cue đã duyệt
  - Output: Đánh dấu rep và tối đa một cue
  - Thời gian/tần suất: Dưới 1 giây, mỗi rep
  - Handoff / boundary: Cue được chuyển cho người tập; không được chẩn đoán hoặc chọn mức tạ

- Bước 7 — Người tập quyết định
  - Owner: Người thực hiện
  - Actor: Người tập
  - Input: Cue ngắn và cảm nhận cơ thể
  - Output: Tiếp tục, điều chỉnh, bỏ qua cue hoặc dừng
  - Thời gian/tần suất: Ở rep tiếp theo
  - Handoff / boundary: Người tập là người ra quyết định cuối; đau/chóng mặt thì dừng và hỏi chuyên gia

- Bước 8 — Xem summary hoặc handoff cho PT
  - Owner: Rule + người
  - Actor: Hệ thống, người tập hoặc PT
  - Input: Rep, cue, confidence và timestamps
  - Output: Summary cùng đúng rep cần xem
  - Thời gian/tần suất: Dưới 10 giây để mở rep sau set
  - Handoff / boundary: Người tập xem lại; rep bị flag có thể handoff cho PT review

#### Before/after impact

- Số bước
  - Trước: 7
  - Sau kỳ vọng trong pilot: 8
  - Ghi chú: Tăng một bước kiểm soát nhưng giảm effort thủ công

- Tổng thời gian
  - Trước: Khoảng 7–17 phút cho set đầu, chưa tính chờ PT
  - Sau kỳ vọng trong pilot: Khoảng 2–4 phút cho set đầu
  - Ghi chú: Giả định cần đo lại; AI/Rule chạy đồng thời khi người dùng tập

- Số bước thủ công
  - Trước: 7/7
  - Sau kỳ vọng trong pilot: 5/8 bước có người tham gia
  - Ghi chú: Người vẫn chọn bài, setup, thực hiện set, quyết định và review

- Bottleneck chính
  - Trước: Bước 5, tua video 2–5 phút nhưng vẫn có thể chọn sai rep
  - Sau kỳ vọng trong pilot: Camera setup/confidence và review case khó với PT
  - Ghi chú: Bottleneck mới là điểm kiểm soát chấp nhận được

- Thời gian tìm đúng rep cần xem
  - Trước: Tua gần như toàn bộ video, baseline cần đo
  - Sau kỳ vọng trong pilot: Dưới 10 giây sau set
  - Ghi chú: App đánh dấu timestamp của rep

- Feedback trong lúc tập
  - Trước: Không có hoặc đến sau set
  - Sau kỳ vọng trong pilot: Dưới 1 giây sau rep
  - Ghi chú: Chỉ feedback khi confidence đủ cao

- Mức đồng thuận với PT khi phát hiện 3 lỗi mục tiêu
  - Trước: Chưa có hệ thống
  - Sau kỳ vọng trong pilot: Tối thiểu 85%
  - Ghi chú: Đo trên video test do PT gán nhãn

- False alert
  - Trước: Không áp dụng
  - Sau kỳ vọng trong pilot: Không quá 15%
  - Ghi chú: Tránh cue sai làm người tập rối

- Cue áp dụng được ở rep kế tiếp
  - Trước: Chưa có
  - Sau kỳ vọng trong pilot: Ít nhất 80% người test hiểu đúng cue
  - Ghi chú: Đo bằng quan sát và câu hỏi sau set

- Số lỗi kỹ thuật trên 10 rep
  - Trước: Baseline từ set đầu không feedback
  - Sau kỳ vọng trong pilot: Giảm ít nhất 30% ở set thứ ba
  - Ghi chú: PT chấm bằng cùng rubric

- Bài tập được hỗ trợ
  - Trước: Người dùng tự xem nhiều video
  - Sau kỳ vọng trong pilot: 1 bài squat không tạ
  - Ghi chú: Không mở rộng trước khi đạt metric

- Rủi ro mới
  - Trước: Feedback muộn, chủ quan hoặc không có
  - Sau kỳ vọng trong pilot: False feedback, lệ thuộc cue, video riêng tư và camera bị che
  - Ghi chú: Dùng confidence gate, boundary, consent và fallback để kiểm soát; feedback sai do góc quay hoặc occlusion phải chuyển sang fallback

#### Metric contract: baseline → target → cách đo

Các baseline chưa được đo bằng user test được ghi rõ là giả định cần validation, không được xem là kết quả thật

- Thời gian tìm đúng rep cần xem
  - Baseline hiện tại: Giả định 2–5 phút để tua lại một set 10 rep, cần đo lại với 5 người dùng
  - Target sau cải thiện: Dưới 10 giây sau khi set kết thúc
  - Cách đo trong pilot: Bấm giờ từ lúc kết thúc set đến khi người dùng mở đúng timestamp được PT đánh dấu

- Feedback latency
  - Baseline hiện tại: Sau set, sau buổi tập hoặc không có
  - Target sau cải thiện: Dưới 1 giây sau rep khi confidence đạt ngưỡng
  - Cách đo trong pilot: So sánh timestamp kết thúc rep với timestamp cue xuất hiện trên bản ghi màn hình

- Đồng thuận khi phát hiện 3 dấu hiệu
  - Baseline hiện tại: Current workflow không có hệ thống tự phát hiện; self-evaluation baseline sẽ đo ở set đầu
  - Target sau cải thiện: Tối thiểu 85% đồng thuận với PT
  - Cách đo trong pilot: Hai PT gán nhãn độc lập; so sánh output hệ thống trên bộ video giữ riêng

- False alert
  - Baseline hiện tại: Không áp dụng vì current workflow chưa có cảnh báo tự động
  - Target sau cải thiện: Không quá 15%
  - Cách đo trong pilot: Tính số rep hệ thống cảnh báo nhưng hai PT không gán nhãn trên tổng số rep bị cảnh báo

- Khả năng hiểu cue
  - Baseline hiện tại: Không có cue chuẩn; baseline đo bằng cách hỏi người dùng sau khi tự xem video
  - Target sau cải thiện: Ít nhất 80% người test nói lại đúng cue và biết cần thử gì ở rep tiếp theo
  - Cách đo trong pilot: Hỏi lại ngay sau set bằng hai câu cố định và chấm theo rubric

- Số dấu hiệu kỹ thuật trên 10 rep
  - Baseline hiện tại: Số lỗi do hai PT chấm ở set đầu không feedback
  - Target sau cải thiện: Giảm ít nhất 30% ở set thứ ba
  - Cách đo trong pilot: PT chấm blind set đầu và set ba bằng cùng rubric, sau đó so sánh số lỗi trung bình


### Bước 5.3 — Problem Statement v0

- **Actor:** Người mới tập gym 0–12 tháng, thường tự tập không có PT theo sát, đang dùng video/gương để kiểm tra form và muốn tự luyện bodyweight squat

- **Workflow:** Chọn squat 1–2 phút → xem mẫu 1–3 phút → setup điện thoại 1–2 phút → quay khoảng 10 rep trong 30–90 giây → dừng và tua video 2–5 phút → tự đoán lỗi/cue 1–3 phút → tập tiếp hoặc handoff video cho PT

- **Bottleneck:** Bước 5, người tập phải tua lại gần như toàn bộ video trong khoảng 2–5 phút để tìm rep cần xem nhưng vẫn có thể chọn sai rep và chưa biết cue nào phù hợp

- **Impact:** Tổng workflow chủ động mất khoảng 7–17 phút cho set đầu chưa tính chờ PT, cùng một dấu hiệu có thể lặp qua nhiều rep, người tập giảm tự tin và có thể tiếp tục một kỹ thuật chưa phù hợp

- **Success Metric:** Từ baseline giả định 2–5 phút tìm rep và không có feedback real-time xuống dưới 10 giây để mở đúng rep, feedback dưới 1 giây khi đủ confidence, ≥85% đồng thuận với PT, false alert ≤15%, ≥80% hiểu cue và giảm ≥30% lỗi ở set ba; đo bằng timed test, video PT gán nhãn, câu hỏi hiểu cue và PT chấm blind set đầu/set ba

- **Boundary:** Pilot chỉ làm bodyweight squat cho người trưởng thành khỏe mạnh và ba dấu hiệu do PT duyệt. AI chỉ tách rep/pose; Rule quyết định no-cue/cue từ thư viện đã duyệt; người tập quyết định tiếp tục hoặc dừng; PT review case bị flag. Không dùng khi đau/chấn thương, không chẩn đoán, không kê bài, không chọn mức tạ, không thay PT; nếu AI sai hoặc confidence thấp thì bỏ cue, flag rep và chuyển sang video/checklist/PT

#### Phản biện Problem Statement v0

- Actor: nhóm 0–12 tháng vẫn còn rộng; cần validation xem pain tập trung ở người tập bao nhiêu buổi mỗi tuần, đã từng quay video hay chưa và có sẵn sàng dùng điện thoại trong phòng gym không
- Workflow: các mốc 1–3 phút, 2–5 phút và tổng 7–17 phút hiện là baseline giả định; phải quan sát ít nhất 5 người thực hiện cùng một task để xác nhận
- Bottleneck: cần kiểm tra pain lớn hơn nằm ở việc tìm đúng rep hay ở việc không biết diễn giải cue, vì hai điểm này có thể dẫn đến hai solution khác nhau
- Impact: chưa có evidence để kết luận hệ thống làm giảm chấn thương, vì vậy impact chỉ nên dừng ở thời gian xem lại, việc lặp dấu hiệu, sự tự tin và khả năng tiếp tục kỹ thuật chưa phù hợp
- Success Metric: target đã rõ nhưng cần chốt cách hai PT xử lý trường hợp bất đồng, cách tính false alert và điều kiện một người được xem là hiểu đúng cue trước khi pilot
- Boundary: cần ghi vào test protocol chính xác ba dấu hiệu được hỗ trợ, nhóm người bị loại khỏi pilot, cách xử lý video, trường hợp phải dừng và cách handoff rep bị flag cho PT


## Phase 6 — Rule / Workflow / Agent + Decision

### Bước 6.0 — Ma trận độ phù hợp với AI

- Độ mơ hồ
  - Đánh giá: Thấp trong scope pilot
  - Lý do: Chỉ kiểm tra ba dấu hiệu của bodyweight squat theo rubric do PT thống nhất, không tự kết luận mọi kỹ thuật đúng hay sai

- Độ phức tạp
  - Đánh giá: Cao
  - Lý do: Cần nối nhiều bước gồm camera check, rep detection, pose landmarks, confidence gate, rule, feedback và summary

- Nhu cầu tự quyết bước tiếp theo
  - Đánh giá: Thấp
  - Lý do: Hệ thống không cần tự lập kế hoạch, chỉ chạy lại cùng workflow cho từng rep

**Ô phù hợp:** Độ phức tạp cao + độ mơ hồ thấp → Workflow điều phối nhiều bước rõ ràng

Bài toán không cần Agent ở scope pilot. Phần pose estimation dùng AI/computer vision, nhưng quyết định feedback bị giới hạn bởi rubric, rule và confidence threshold


### Bước 6.1 — So sánh Rule / Workflow / Agent

- **No AI / process fix**
  - Phương án cho bài toán: Video hướng dẫn chuẩn, checklist 3 cue, gương và buổi hướng dẫn ban đầu với PT
  - Khi nào đủ: Đủ nếu người tập quan sát và tự sửa được
  - Rủi ro: Không có feedback khách quan trong rep hiện tại
  - Kết luận: Dùng làm baseline và fallback

- **Rule**
  - Phương án cho bài toán: Người dùng tự quay video, hệ thống tính một vài góc rồi so với ngưỡng cố định
  - Khi nào đủ: Đủ cho một lỗi rất rõ, một góc camera và một cơ thể mẫu
  - Rủi ro: Ngưỡng cứng dễ báo sai, landmark chưa chắc ổn định
  - Kết luận: Dùng bên trong workflow

- **Workflow**
  - Phương án cho bài toán: Camera check → rep detection → pose estimation → confidence gate → rule → đánh dấu rep → cue ngắn → history
  - Khi nào đủ: Phù hợp vì các bước tuyến tính và mỗi bước có boundary
  - Rủi ro: Sai landmark, nhận nhầm rep hoặc cue không phù hợp nếu rubric kém
  - Kết luận: **Chọn**

- **Agent**
  - Phương án cho bài toán: Agent tự chọn bài, đổi bài, điều chỉnh mức tạ và lập kế hoạch theo performance
  - Khi nào đủ: Chỉ cần nếu mục tiêu là coaching toàn bộ chương trình
  - Rủi ro: Quyền tự quyết quá lớn, rủi ro sức khỏe và scope rộng
  - Kết luận: Không chọn

**Mức chọn:** **Workflow**

*Vì sao chọn:* Pose estimation phù hợp cho bước quan sát chuyển động, rule phù hợp để kiểm tra một rubric hẹp, còn workflow giúp thêm camera check, confidence gate, feedback và fallback theo thứ tự rõ. Hệ thống không cần tự lập kế hoạch hoặc đổi mục tiêu nên Agent không mang thêm giá trị tương xứng với rủi ro

*Vì sao không chọn mức đơn giản hơn:* Video và checklist vẫn là baseline tốt nhưng không nhìn thấy rep hiện tại. Rule đơn lẻ chưa đủ vì trước khi áp dụng rule phải kiểm tra camera, landmark confidence và sau đó còn phải quản lý feedback/fallback

*Vì sao không chọn Agent:* Scope pilot không cần hệ thống tự đặt mục tiêu, chọn bài, đổi mức tạ hoặc tự quyết bước tiếp theo. Agent làm tăng quyền tự quyết và rủi ro sức khỏe nhưng không giải quyết bottleneck tốt hơn Workflow đã định nghĩa

**AI được phép làm:**

- Tách từng rep và lấy pose landmarks trong bài bodyweight squat được hỗ trợ
- Chỉ kiểm tra ba dấu hiệu đã được PT duyệt khi confidence đạt ngưỡng
- Đánh dấu timestamp và chọn tối đa một cue từ thư viện cue đã được duyệt
- Tạo summary để người tập hoặc PT xem lại sau set

**AI không được phép làm:**

- Chẩn đoán đau, chấn thương hoặc kết luận một người đủ an toàn để tiếp tục tập
- Chọn bài, kê chương trình, tăng mức tạ hoặc thay đổi mục tiêu của người dùng
- Đưa feedback ngoài bài tập, dấu hiệu hoặc góc camera đã được validation
- Bỏ qua confidence gate để cố đưa ra nhận xét

**Người thật kiểm tra và chịu trách nhiệm:**

- Hai PT thống nhất rubric, gán nhãn bộ test và review false positive/false negative
- Người tập quyết định tiếp tục, điều chỉnh, dừng lại hoặc hỏi chuyên gia
- Nhóm sản phẩm chỉ mở rộng scope sau khi metric và fallback đạt yêu cầu


### Bước 6.2 — Problem Statement v1

- **Actor:** Người mới tập gym 0–12 tháng, thường tự tập không có PT theo sát và đã từng dùng video/gương để kiểm tra form

- **Workflow:** Chọn squat → setup camera → quay khoảng 10 rep → tua lại video → tìm rep → tự đoán lỗi → thử sửa ở set sau

- **Bottleneck:** Mất thời gian tìm rep cần xem nhưng vẫn không biết dấu hiệu nào cần chú ý và phải điều chỉnh gì ngay ở rep kế tiếp

- **Impact:** Lặp lại cùng dấu hiệu qua nhiều rep, mất thời gian xem video, giảm tự tin và có thể tiếp tục kỹ thuật chưa phù hợp

- **Success Metric:** Trong pilot có giám sát: tìm đúng rep <10 giây, feedback <1 giây khi đủ confidence, ≥85% đồng thuận với PT, false alert ≤15%, ≥80% hiểu đúng cue và giảm ≥30% lỗi ở set thứ ba

- **Boundary:** Chỉ bodyweight squat cho người trưởng thành khỏe mạnh trong pilot; chỉ phản hồi dấu hiệu được hỗ trợ; không dùng khi đau/chấn thương; không chẩn đoán, kê bài, đổi mức tạ hoặc thay PT; gimbal là tùy chọn

- **AI intervention point:** Sau camera check, AI tách rep và lấy pose landmarks; confidence gate và rule quyết định có đánh dấu rep/đưa cue hay không

- **Mức chọn:** Workflow gồm camera check + rep detection + computer vision + rule + cue + history + fallback

- **Rủi ro & người thật kiểm tra:** Risk gồm occlusion, góc camera sai, body diversity, false feedback và người dùng phụ thuộc hệ thống. PT duyệt rubric, gán nhãn bộ test và review các false positive/negative trước khi mở rộng


### Bước 6.3 — Final decision

#### Cơ sở ra quyết định

- Người mới mất 2–5 phút tua video và thường không biết rep nào sai
  - Evidence hay giả định: Giả định từ scenario hiện tại, chưa có observed test thật
  - Ảnh hưởng đến quyết định: Bắt buộc đo baseline trước khi kết luận pain đủ lớn

- Hai PT có thể thống nhất ba dấu hiệu và cue phù hợp
  - Evidence hay giả định: Giả định chưa được kiểm chứng
  - Ảnh hưởng đến quyết định: Nếu không thống nhất được rubric thì rollback về video + checklist

- Feedback sai có thể khiến người dùng tiếp tục một kỹ thuật chưa phù hợp
  - Evidence hay giả định: Rủi ro được ghi rõ từ research và boundary
  - Ảnh hưởng đến quyết định: Không cho người dùng tự sử dụng trước khi đạt metric và có owner review

#### Checklist trước khi ra quyết định

- Actor và workflow đã rõ chưa?
  - Kết luận: Yes
  - Ghi chú: Đã thu hẹp về người mới 0–12 tháng tự tập bodyweight squat và thường quay video kiểm tra

- Baseline và success metric đã đo được chưa?
  - Kết luận: Not Yet
  - Ghi chú: Metric đã định nghĩa nhưng chưa có user test thật

- Có data/input đủ dùng chưa?
  - Kết luận: Not Yet
  - Ghi chú: Có pose model nền nhưng chưa có bộ video đại diện được PT gán nhãn cho rubric của nhóm

- Nếu AI sai, hậu quả có chấp nhận được không?
  - Kết luận: Not Yet
  - Ghi chú: Chỉ chấp nhận trong pilot không tạ, có giám sát và confidence gate

- Có người review/owner vận hành không?
  - Kết luận: Not Yet
  - Ghi chú: Cần ít nhất một PT chịu trách nhiệm rubric và review

- Có cách non-AI đơn giản hơn không?
  - Kết luận: Yes
  - Ghi chú: Video chuẩn, checklist, gương và PT session đầu tiên

**Decision:** **Not Yet**

*Lý do:* Hướng giải pháp có bằng chứng desk research về tính khả thi nhưng pain, baseline, rubric và chất lượng với người dùng thật của nhóm chưa được kiểm chứng. Nhóm chỉ nên làm prototype validation có giám sát, chưa đưa cho người dùng tự sử dụng

**Nếu Not Yet, cần validate:** Pain có đủ thường xuyên không, người dùng có hiểu cue không, hai PT có thống nhất rubric không, hệ thống có đạt các metric đã đặt ra không và fallback có ngăn feedback khi dữ liệu không đủ không

#### Prototype validation nhỏ nhất

1. Chỉ dùng bodyweight squat và ba dấu hiệu do hai PT thống nhất
2. Thu video có đồng ý từ tối thiểu 5 người mới tập ở góc camera quy định
3. Hai PT gán nhãn độc lập, xử lý các trường hợp bất đồng trước khi test model
4. Chạy prototype theo workflow camera check → tách rep → pose → confidence → rule → đánh dấu rep → cue
5. So sánh output với PT và đo agreement, false alert, feedback latency, thời gian tìm rep
6. Cho người dùng tập ba set có giám sát, hỏi lại nội dung cue và đo số lỗi trên 10 rep ở set đầu với set ba

#### Điều kiện để chuyển thành Go

- Pain được xác nhận qua ít nhất 5 interview và observed test
- Hai PT thống nhất được rubric cho ba lỗi mục tiêu
- Đạt các metric ≥85% agreement, ≤15% false alert, <1 giây feedback và <10 giây tìm đúng rep sau set
- Ít nhất 80% người test hiểu đúng cue và giảm ít nhất 30% lỗi ở set thứ ba
- Không có feedback khi confidence thấp và fallback hoạt động đúng

#### Exit / rollback

- Nếu hai PT không thống nhất được rubric, hạ xuống video hướng dẫn + checklist
- Nếu camera một góc không đạt metric, chuyển sang review video sau set hoặc yêu cầu hai góc quay
- Nếu feedback làm người tập rối hoặc sai nhiều hơn, dừng real-time feedback
- Nếu người dùng báo đau, chóng mặt hoặc mất thăng bằng, hệ thống phải dừng và hướng dẫn tìm hỗ trợ chuyên môn
