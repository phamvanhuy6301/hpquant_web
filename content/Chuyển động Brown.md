Phần này cũng là ghi chú của tôi khi xem bài viết gốc: https://tuhocquantfinance.com/2026/01/17/brownian-motion/

## Từ phấn hoa đến giá cổ phiếu. 
- như trước đó trong bài [[random walk]] ta đã nhận định được một vấn đề của random walk là nó có tính rời rạc, giá cổ phiếu lại liên tục. Tức là ta cần một công cụ để chuyển random walk từ rời rạc sang liên tục. Các nhà toán học thực hiện một thao tác "nén thời gian và không gian". Khi khoảng thời gian giữa các bước nhảy tiến dần về vô hạn $dt \to 0$, quỹ đạo gãy sẽ hội tụ thành một dòng chảy liên tục gọi là Wiener Process hay chuyển động Brown. 
	Cho một khoảng thời gian $t$ với $n$ bước nhảy, ta thu nhỏ kích thước của mỗi bước nhảy tương ứng với tốc độ thời gian. 
	- thời gian: $\Delta t = t/n$ 
	- không gian: mỗi bước nhảy có độ lớn là $\pm \sqrt{\Delta t}$ 
	Do phương sai tỷ lệ thuận với số bước, nếu mỗi bước có độ lớn $\pm \sqrt{\Delta t }$, lúc này phương sai sau $n$ bước là 
		$$
		Var(S_t) = n \times (\sqrt{\Delta t})^2 = n \times \frac{t}{n} = t
		$$
Đây là một kết quả đẹp: phương sai chuyển động bằng đúng khoảng thời gian trôi qua => thế tại sao nó lại coi là đẹp? [[Phương sai chuyển động bằng đúng khoảng thời gian trôi qua ]]

