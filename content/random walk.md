---
title: Random Walk
date: 2026-09-30
---
Bài viết này được thực hiện trong quá trình học tập của tôi từ bài viết gốc https://tuhocquantfinance.com/2026/01/13/random-walk/ 
Một số ý quan trọng trong bài viết gốc: 
- tư duy xác định (Deterministic) và tư duy ngẫu nhiên (Stochastic). 
- cơ chế hoạt động và 3 trụ cột của bước đi ngẫu nhiên (random walk)
Đây có thể xem là phần ghi chú của tôi trong quá trình nghiên cứu và hệ thống hóa kiến thức. 
quant -> khát vọng mô hình hóa thế giới -> câu hỏi nghi vấn cần đặt ra là liệu có tồn tại mô hình để người làm quant có thể mô hình hóa được hay không? 

## Từ xác định đến ngẫu nhiên 
- Trong nhiều thế kỷ, khoa học bị thống trị bởi tư duy xác định (deterministic). Một đại diện của tư tưởng này là giả thuyết về "Ác quỷ Laplace" - nếu biết vị trị và vận tốc của mọi hạt trong vũ trụ, ta có thể suy luận ra chính xác quá khứ và tương lai. Tư duy này hoạt động tốt khi NASA phóng tàu vũ trụ lên sao hỏa bằng các định luật Newton. 
- Trong tài chính, người ta mơ về 1 công thức toán học đóng $y -= f(x)$. Thực tế thì giá cổ phiếu nó không đi theo một đường thẳng hay một đường cong, ta k thể dùng gia tốc của cổ phiếu hôm nay để dự đoán giá cho ngày mai. 
-  Tài chính là một hệ thống phức tạp tự quy chiếu. Nếu các nhà đầu tư đều biết giá ngày mai sẽ tăng, hôm nay họ sẽ mua và giá sẽ tăng vào ngày hôm nay. 
- Ngẫu nhiên khác với vô định hay hỗn loạn $\to$ là sự kết hợp giữa **xu hướng giá dài hạn** và **biến động trong ngắn hạn**. 
- Tuy nhiên, khi đem vào thị trường tài chính, thì giá cổ phiếu nó không vận hành như thế, chúng nhảy múa, rung lắc và đảo chiều. Bạn không thể dùng vận tốc tăng trưởng hôm qua để khẳng định chắc chắn giá ngày hôm nay. 
- Đây là lúc ta cần thế giới Ngẫu nhiên (Stochastic). Ngẫu nhiên không có nghĩa là vô định hay hỗn loạn. 
- trong thế giới ngẫu nhiên, rủi ro không phải sai số, nó là bản chất. 
- các quant hiện đaị tin rằng: “việc dự báo tương lai từ dữ liệu quá khứ là vô ích” $\to$ họ tập trung vào việc mô hình hóa ngẫu nhiên và rủi ro $\to$  *với tôi thì đây là chỗ trống cho một người mới như tôi, tôi sẽ chọn miếng bánh mà ít người làm, có thể xem đây là thị trường ngách mà tôi chọn.* 
- Với một số quỹ lớn, sự thành công không đến từ việc đoán đúng giá, mà từ việc hiểu rõ biên độ của sự rung lắc để thực hiện các chiến lược phòng vệ nhằm triệt tiêu sự ngẫu nhiên. $\to$ Với tôi, nếu tư duy ngược lại, bản chất của thị trường trong thế giới ngẫu nhiên rủi ro k phải sai số, vậy tại sao lại phải cố gắng triệt tiêu sự ngẫu nhiên.  Và nếu triệt tiêu thì câu hỏi là triệt tiêu bằng cách nào và bằng cái gì. 
- tài sản thực tế có đuôi béo dẫn đến các biến đông cực đoan diễn ra thường xuyên hơn việc áp phân phối chuẩn vào. 
	![[Pasted image 20261005164628.png]]
	![[Pasted image 20261006114614.png]]
## Trò chơi tung đồng xu 
ta sẽ bắt đầu với mô hình đơn giản nhất. Hãy tưởng tượng ta sẽ tham gia một trò chơi tung đồng xu và điểm số bắt đầu từ vạch xuất phát (con số 0). 
	- Mỗi lần tung được mặt ngửa, bạn bước sang phải (+1)
	- Mỗi lần tung được mặt sấp, bạn bước sang trái (-1) 
	Lúc này quỹ đạo đường đi sẽ tạo ra một hình răng cưa không thể đoán trước, được gọi là bước đi ngẫu nhiên (random walk). Vị trí cuối cùng sau nhiều lần tung chính là tổng tích lũy của tất cả các bước đi đơn lẻ. 

Các nhà khoa học dùng mô hình này để mô phỏng thị truờng dựa trên Giả thuyết Thị trường Hiệu quả (EMH): "Mọi thông tin đã được phản ánh ngay vào giá hiện tại". Vì tin tức xuất hiện ngẫu nhiên nên biến động giá tiếp theo cũng phải mang tính ngẫu nhiên. 
![[Pasted image 20261006114649.png]]
## ba trụ cột của bước đi ngẫu nhiên
- Bước đi ngẫu nhiên có 3 tính chất cực kỳ quan trọng sau đây: 
	- Tính không có trí nhớ (Markov property): đồng xu không có trí nhớ, việc hôm nay tung được mặt úp hay ngửa không làm tăng hay giảm khả nnawg ngày mai bạn lại tung được mặt ngửa. Ánh xạ sang thế giới tài chính, điều này có nghĩa là mức giá của hôm nay đã chứa đựng tất cả lịch sử của giá quá khứ. Để dự đoán ngày mai, dữ liệu quan trong trọng nhất là hôm nay, còn việc hôm qua tăng hay giảm bao nhiêu không hề giúp ích cho dự đoán đó. 
	- Kỳ vọng bằng 0: đây là trò chơi công bằng, có kỳ vọng bằng 0. 
		Với tôi thì khi ánh xạ sang thị trường tài chính, nếu một chuỗi giá có kỳ vọng bằng 0, bạn tham gia mua bán thì kỳ vọng lợi nhuận của bạn sẽ là âm, bạn phải chịu rủi ro về trượt giá và một mức phí giao dịch cố định, bạn càng giao dịch nhiều thì chi phí giao dịch tích lũy càng cao. 
	- Rủi ro tăng theo thời gian: Dù trung bình bạn đứng yên, nhưng càng tung đồng xu nhiều lần, bạn càng có khả năng đi rất xa khỏi vạch xuất phát (về cả hai phía). Sau $n$ lần tung, độ lệch chuẩn vị trí của bạn là $\sqrt{n}$. Rủi ro không tăng gấp đôi, rủi ro răng theo căn bậc hai của thời gian. 
	![[Pasted image 20261006115906.png]]
## Vấn đề khi mô hình hóa bằng random walk 
- Bằng cách sử dụng hệ số nhị thức, ta có thể tính toán xác suất để một cổ phiếu dùng tại vị trí bất kỳ sau một số bước thời gian cố định. Tuy nhiên, khi ánh xạ sang thị trường, sẽ có một số vấn đề phát sinh: 
	- Tính rời rạc: cổ phiếu được khớp liên tục từng mili giây, trong khi random walk chỉ mô tả các mốc thời gian cố định $\to$ tức là ta cần một công cụ để chuyển bài toán từ rời rạc sang liên tục. 
	- bước nhảy không đổi: trong mô hình tung đồng xu, giá tăng giảm theo giá trị tuyệt đối của đơn vị. Thực tế, giá biến động có lúc nhiều, có lúc ít. $\to$ tức là khi mô hình hóa ta cần phải mô tả được cơ chế này, chứ không phải là áp nguyên $\pm 1$ vào. 
	- Giá trị tuyệt đối: random walk coi bước nhảy từ 10 lên 11 y hệt 100 lên 101. Ánh xạ qua thị trường thì cái nhà đầu tư quan tâm là tỷ suất sinh lời, nó là phần trăm. 
## Liên hệ giữa PnL của một alpha với random walk. 
-  Điểm khác nhau: 
	random walk thì mỗi bước đi là $\pm 1$, nhưng alpha thì nó khác, PnL của nó là tổng tích lũy của lợi nhuận hàng ngày (gain_daily); gain_daily rõ ràng có các giá trị khác nhau $\to$ câu hỏi đặt ra là liệu có cách nào xác định alpha đó có PnL là do tín hiệu của nó hay chỉ đơn giản là may mắn 
- Về mặt công thức tích lũy: 
	- Random walk đơn giản: $S_n = S_0 + \sum_{i=1}^{n} X_i$, trong đó $X_i$ chỉ nhận hai giá trị rời rạc là $\pm 1$ 
	- PnL của alpha: $PnL_t = \sum_{i=1}^t gain_i$. Mỗi bước nhảy $gain_i$ là một biến ngẫu nhiên liên tục có phân phối. 
- Về mặt kỳ vọng (Liệu là tín hiệu hay may mắn): 
	- Alpha không có tín hiệu (may mắn thuần túy): Kỳ vọng lợi nhuận hằng ngày bằng 0. PnL lúc này sẽ là một random walk thuần túy. Dù PnL có thể tăng trong ngắn hạn nhờ may mắn, kỳ vọng dài hạn của nó vẫn trở về vạch xuất phát, tuy nhiên nếu thêm phần phí giao dịch vào thì dài hạn nó sẽ cắm đầu. 
	- Alpha có tín hiệu thực sự (true edge): Kỳ vọng lợi nhuận lúc này mang giá trị dương ($\mu > 0$). PnL lúc này tương đương với một  Random walk có xu hướng. 
Tóm lại, trong ngắn hạn, nhiễu ngẫu nhiên sẽ lấn áp tín hiệu. Sự khác biệt lớn nhất giữa một Alpha có tín hiệu và một random walk may mắn chỉ bộc lộ qua thời gian đủ dài (N lớn). Nhưng N đủ lớn là bao nhiêu thì tôi không biết, quan sát N quá lớn có khi sẽ làm bạn bỏ lỡ lúc "ăn mạnh" của alpha, nhưng không quan sát có thể bạn sẽ nhầm lẫn sữa tín hiệu thật và sự may mắn. 
