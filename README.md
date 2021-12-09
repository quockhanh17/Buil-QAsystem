# Buil-QAsystem
Chúng tôi thực hiện cài đặt hệ thống trên nền tảng Colab của Google. Với bước đầu tiên chúng tôi tiến hành đưa dữ liệu vào trong mảng, đồng thời sẽ đưa mô – đun Ktrain vào. Các bước tiếp theo chúng tôi tạo Search Index và QA Instance. Cuối cùng chúng tôi sẽ tiến hành gọi phương pháp để đưa ra câu trả lời.

Google Colab: https://colab.research.google.com

![333](https://user-images.githubusercontent.com/93696035/145383627-e77f0a13-a0d4-4115-a859-01a4e9059495.png)

## Cài đặt
  Chúng ta cần cài đặt mô - đun Ktrain trước khi tiến hành cài đặt hệ thống.
  
  Câu lệnh cài đặt: "!pip3 install -q ktrain"
  
![kq1](https://user-images.githubusercontent.com/93696035/145386248-7d9038a6-1bb7-4df5-9d1e-91d1673904c9.png)
  
### 1. Tải tập dữ liệu và nhập mô - đun Ktrain:

  Chúng tôi bắt đầu bằng các tải bộ dự vào một mảng có sử dụng thư viện Sklearn và nhập mô – đun Ktrain. Đồng thời ở bước đầu này chúng tối sẽ huấn luyện mô hình dữ liệu và sau đó loại bỏ 3 phần trong dữ liệu đó là headers, footers, quotes.
  
![code 1](https://user-images.githubusercontent.com/93696035/145384231-4983ade3-1b70-4269-9a0c-62f1dc4554de.png)

### 2. Tạo Search Index:
  Với bộ dữ liệu, chúng tôi sẽ cần tạo Search Index. Nó cho phép chúng tôi nhanh chóng và dễ dàng truy xuất các tài liệu có chứa các từ có trong câu hỏi. Những tài liệu như vậy có khả năng chứa câu trả lời và có thể được phân tích thêm để trích xuất câu trả lời của tài liệu đã được chọn. Vì các bài đăng của nhóm tin nhỏ và phù hợp với bộ nhớ chính, chúng tôi sẽ đặt thành giá trị lớn để tăng tốc quá trình lập Search Index. Điều này có nghĩa là kết quả sẽ không được in cho đến khi kết thúc.
  
![code 2](https://user-images.githubusercontent.com/93696035/145384918-b55bed00-a6d1-4dd2-b4e5-ca912cdc6d7d.png)

### 3. Tạo QA Instance:
  Ở phần này chúng tôi sẽ tạo QA Instance, với chủ yếu là xung quanh mô hình được đào tạo sẵn BertForQuestionAnswering.
  
![kq4](https://user-images.githubusercontent.com/93696035/145385325-6cae5af9-64e7-4f0a-b5ba-e598f728a094.png)

### 4. Đặt câu hỏi và cho ra kết quả:
  Chúng tôi sẽ viện dẫn phương pháp để đưa ra câu hỏi cho tập tin văn bản mà chúng tôi đã lập Search Index và lấy câu trả lời. Chúng tôi thực hiện các bước trên để định dạng và hiển thị 5 kết quả hàng đầu.
  
![code](https://user-images.githubusercontent.com/93696035/145385576-b28a214d-d409-427b-a926-574253b4b467.png)

