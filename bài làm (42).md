**Method**

**Endpoint**

**Mục đích**

GET

/api/v1/list

Lấy danh sách dữ liệu

GET

/api/v1/detail

Xem chi tiết phần tử

POST

/api/v1/create

Thêm dữ liệu mới

PUT

/api/v1/update

Cập nhật thông tin

DELETE

/api/v1/delete

Xóa phần tử

GET

/api/v1/stats

Xem thống kê hoạt động
1.Bảo mật & Phân quyền: Luôn kiểm tra tính hợp lệ của yêu cầu theo các Endpoint
 2. Chain-of-Thought : Trước khi đưa ra câu trả lời cuối cùng, bạn bắt buộc phải phân rã vấn đề thành các bước logic và trình bày chi tiết bên trong mục . 
 3. Xử lý đứt gãy : Nếu phản hồi bị ngắt quãng do giới hạn độ dài token, hãy tự động duy trì sự nhất quán của ngữ cảnh ở lượt phản hồi tiếp theo dựa trên từ khóa . 
 4. Định dạng đầu ra: Luôn trả về kết quả theo cấu trúc JSON rõ ràng gồm các trường: route, status, reasoning_steps, và response_content.
 JSON

```
{
  "route": "/api/v1/create",
  "status": "SUCCESS",
  "reasoning_steps": [
    "Bước 1: Xác thực endpoint /api/v1/create hợp lệ và có quyền truy cập.",
    "Bước 2: Phân tích yêu cầu khởi tạo phiên tư vấn kiến trúc backend thương mại điện tử.",
    "Bước 3: Thiết lập ngữ cảnh chuyên gia, áp dụng phương pháp Chain-of-Thought để lập phác thảo giải pháp phân tách microservices."
  ],
  "response_content": "Đã khởi tạo thành công phiên tư vấn chuyên sâu cho hệ thống thương mại điện tử. Hệ thống đã sẵn sàng tiếp nhận các thông số kỹ thuật tiếp theo (như lưu lượng truy cập, CSDL) để tiến hành phân tích chi tiết."
}
```
