# QUY TRÌNH TROUBLESHOOTING NỘI BỘ CHO NHÓM STARTUP

## 1. Thiết kế mẫu Bug Report Template

Để tránh tình trạng thành viên nhắn tin lỗi không rõ ràng trong nhóm chat, nhóm sẽ sử dụng mẫu báo cáo lỗi gồm 4 thành phần bắt buộc: Context, Expected, Actual và Log.

### BUG REPORT TEMPLATE

**1. Context (Bối cảnh)**
- Tên dự án:
- Công cụ đang sử dụng (Docker, Git, Python...):
- Phiên bản phần mềm:
- Hệ điều hành:
- Các thao tác đã thực hiện trước khi xảy ra lỗi:

**2. Expected (Kết quả mong đợi)**

- Mô tả kết quả mà thành viên mong muốn nhận được.
- Ví dụ: Docker khởi chạy thành công và ứng dụng truy cập được qua cổng 8080.

**3. Actual (Kết quả thực tế)**

- Mô tả điều gì đã xảy ra.
- Ví dụ: Docker không khởi chạy được do cổng 8080 đang được sử dụng bởi một tiến trình khác.

**4. Log (Nhật ký lỗi)**

- Dán thông báo lỗi đầy đủ.
- Đính kèm ảnh chụp màn hình nếu cần.
- Cung cấp đoạn log liên quan để nhóm có thể xác định nguyên nhân.

**Quy định:** Thành viên phải điền đầy đủ 4 phần trước khi gửi yêu cầu hỗ trợ lên nhóm chat. Không gửi những câu hỏi chung chung như "Docker bị lỗi, sửa thế nào?".

---

## 2. Quy trình tra cứu bắt buộc 3 bước

Trước khi nhờ đồng đội hỗ trợ, mỗi thành viên phải thực hiện quy trình sau:

### Bước 1: Googling (Tìm kiếm trên Google)

- Sử dụng từ khóa chính xác trong thông báo lỗi.
- Kết hợp các toán tử tìm kiếm như `site:`, dấu ngoặc kép `" "` để tìm thông tin phù hợp.
- Ưu tiên tài liệu chính thức và các bài hướng dẫn có nguồn đáng tin cậy.

Ví dụ:

```text
"Docker port is already allocated" solution
```

Mục tiêu: Tìm nguyên nhân và giải pháp đã được ghi nhận.

### Bước 2: Community Search (Tìm kiếm cộng đồng)

- Tìm kiếm các vấn đề tương tự trên Stack Overflow và GitHub Issues.
- Ưu tiên câu trả lời có nhiều lượt upvote, bình luận tích cực và được Maintainer xác nhận.
- Kiểm tra phiên bản phần mềm và hệ điều hành có phù hợp hay không.
- Đọc các bình luận mới để tìm giải pháp cập nhật.

Ví dụ:

```text
site:stackoverflow.com "Docker port is already allocated"
```

Mục tiêu: Tham khảo kinh nghiệm thực tế từ cộng đồng lập trình viên.

### Bước 3: AI Translation (Nhờ AI giải thích và hỗ trợ)

- Sao chép thông báo lỗi và cung cấp Context cho AI.
- Yêu cầu AI giải thích nguyên nhân bằng ngôn ngữ dễ hiểu.
- Nhờ AI đề xuất các bước sửa lỗi cụ thể.
- Yêu cầu AI giải thích chức năng và rủi ro của từng câu lệnh trước khi thực hiện.
- Đối chiếu câu trả lời của AI với tài liệu chính thức trước khi áp dụng.

Ví dụ Prompt:

```text
Tôi đang gặp lỗi Docker port is already allocated.

Hệ điều hành: Windows 11.
Công cụ: Docker Desktop.
Mục tiêu: Chạy ứng dụng trên cổng 8080.

Hãy:
1. Phân tích nguyên nhân gây ra lỗi.
2. Đề xuất các bước khắc phục từ đơn giản đến phức tạp.
3. Giải thích chức năng từng câu lệnh.
4. Cảnh báo những lệnh có thể ảnh hưởng đến hệ thống.
5. Đưa ra nguồn tài liệu chính thức để kiểm chứng.

Không đề xuất lệnh nguy hiểm khi chưa giải thích rõ tác động.
```

---

## 3. Quy định khi yêu cầu hỗ trợ trong nhóm

Sau khi thực hiện đủ 3 bước nhưng vẫn không giải quyết được vấn đề, thành viên mới được gửi Bug Report lên nhóm.

Khi gửi cần:
- Đính kèm Bug Report Template đã điền đầy đủ.
- Ghi rõ những cách đã thử.
- Đính kèm đường dẫn tài liệu đã tham khảo.
- Nêu rõ kết quả của từng lần thử.

Sau khi lỗi được giải quyết, người xử lý cần cập nhật cách khắc phục vào kho tài liệu nội bộ để các thành viên khác có thể tra cứu.

## 4. Kết luận

Việc xây dựng quy trình Troubleshooting giúp nhóm Startup quản lý lỗi khoa học, giảm tình trạng hỏi trùng lặp và tránh làm trôi thông tin trong nhóm chat.

Quy trình 3 bước Googling → Community Search → AI Translation khuyến khích thành viên chủ động tìm hiểu và tự xử lý khoảng 80% vấn đề thông thường trước khi nhờ hỗ trợ.

Đồng thời, Bug Report Template giúp người hỗ trợ nắm bắt vấn đề nhanh chóng, tiết kiệm thời gian và nâng cao hiệu quả làm việc nhóm.
