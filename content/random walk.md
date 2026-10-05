---
title: Random Walk
date: 2026-09-30
---
Bài viết này được thực hiện trong quá trình học tập của tôi từ bài viết gốc https://tuhocquantfinance.com/2026/01/13/random-walk/ 
Đây có thể xem là phần ghi chú của tôi trong quá trình nghiên cứu và hệ thống hóa kiến thức. 
quant -> khát vọng mô hình hóa thế giới -> câu hỏi nghi vấn cần đặt ra là liệu có tồn tại mô hình để người làm quant có thể mô hình hóa được hay không? 

Trong tài chính, người ta mơ về 1 công thức toán học đóng $y -= f(x)$. Thực tế thì giá cổ phiếu nó không đi theo một đường thẳng hay một đường cong, ta k thể dùng gia tốc của cổ phiếu hôm nay để dự đoán giá cho ngày mai. 
- Tài chính là một hệ thống phức tạp tự quy chiếu. Nếu các nhà đầu tư đều biết giá ngày mai sẽ tăng, hôm nay họ sẽ mua và giá sẽ tăng vào ngày hôm nay. 
- Ngẫu nhiên khác với vô định hay hỗn loạn $\to$ là sự kết hợp giữa **xu hướng giá dài hạn** và **biến động trong ngắn hạn**. 
- trong thế giới ngẫu nhiên, rủi ro không phải sai số, nó là bản chất. 
- các quant hiện đaị tin rằng: “việc dự báo tương lai từ dữ liệu quá khứ là vô ích” $\to$ họ tập trung vào việc mô hình hóa ngẫu nhiên và rủi ro $\to$  *với tôi thì đây là chỗ trống cho một người mới như tôi, tôi sẽ chọn miếng bánh mà ít người làm, có thể xem đây là thị trường ngách mà tôi chọn.* 
- Với một số quỹ lớn, sự thành công không đến từ việc đoán đúng giá, mà từ việc hiểu rõ biên độ của sự rung lắc để thực hiện các chiến lược phòng vệ nhằm triệt tiêu sự ngẫu nhiên. $\to$ Với tôi, nếu tư duy ngược lại, bản chất của thị trường trong thế giới ngẫu nhiên rủi ro k phải sai số, vậy tại sao lại phải cố gắng triệt tiêu sự ngẫu nhiên.  Và nếu triệt tiêu thì câu hỏi là triệt tiêu bằng cách nào và bằng cái gì. 

• ⁃ tài sản thực tế có đuôi béo -> các biến đông cực đoan diễn ra thường xuyên hơn việc áp phân phối chuẩn vào.
# Trò chơi tung đồng xu 
ta sẽ bắt đầu với mô hình đơn giản nhất. Hãy tưởng tượng ta sẽ tham gia một trò chơi tung đồng xu và điểm số bắt đầu từ vạch xuất phát (con số 0). 
	- Mỗi lần tung được mặt ngửa, bạn bước sang phải (+1)
	- Mỗi lần tung được mặt sấp, bạn bước sang trái (-1) 
	Lúc này quỹ đạo đường đi sẽ tạo ra một hình răng cưa không thể đoán trước, được gọi là bước đi ngẫu nhiên (random walk). Vị trí cuối cùng sau nhiều lần tung chính là tổng tích lũy của tất cả các bước đi đơn lẻ. 

Các nhà khoa học dùng mô hình này để mô phỏng thị truờng dựa trên Giả thuyết Thị trường Hiệu quả (EMH): "Mọi thông tin đã được phản ánh ngay vào giá hiện tại". Vì tin tức xuất hiện ngẫu nhiên nên biến động giá tiếp theo cũng phải mang tính ngẫu nhiên. 

## Liên hệ giữa PnL của một alpha với random walk. 
-  Điểm khác nhau: 
	random walk thì mỗi bước đi là $\pm 1$, nhưng alpha thì nó khác, PnL của nó là tổng tích lũy của lợi nhuận hàng ngày (gain_daily); gain_daily rõ ràng có các giá trị khác nhau $\to$ câu hỏi đặt ra là liệu có cách nào xác định alpha đó có PnL là do tín hiệu của nó hay chỉ đơn giản là may mắn 