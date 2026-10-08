Theo tôi tra cứu thì có 3 lý do mà phương sai này được coi là đẹp. 
1.  phương sai tích lũy đúng bằng độ dài khoảng thời gian $t$. 
2. thời gian là thước đo tự nhiên của sự không chắc chắn: 
	- Phân phối chuẩn của số gia: Trong quá trinh Weiner ($W_t$), số gia biến động giữa thời điểm $s$ và $t$ luôn tuân theo phân phối chuẩn $(W_t - W_s) \sim N(0, t - s)$ với kỳ vọng bằng $0$ và phương sai bằng chính khoảng thời gian trôi qua. 
		Vấn đề lúc này tại sao khi nén không thời gian thì phân phối của số gia lại chuẩn: 
3. Cầu nối tại nên quá trình Wiener mượt mà: Việc giữ cho phương sai bằng đúng thời gian $t$ đảm bảo rằng khi cho số bước nhảy tiến về vô hạn ($n \to \infty$ và $\Delta t \to 0$), quỹ đạo gãy khúc thô ráp của _Random Walk_ hội tụ chuẩn xác về **Quá trình Wiener** ($W_t$) liên tục. Phương sai $\sigma^2$ trong các mô hình liên tục như Bachelier hay Chuyển động Brown Hình học (GBM) thực chất chính là sự mịn hóa hoàn hảo của phương sai trong mô hình rời rạc
# Tại sao lại là phân phối chuẩn? 
- Khi xét khoảng thời gian từ $s$ đến $t$ (có độ dài $\Delta t = t-s$), ta có thể chia khoảng thờ8i gian này cực ngắn $\delta t = \frac{t - s}{n}$ 
- số gia biến động $W_t - W_s$ thực chất chính là tổng tích lũy của $n$ cú sốc ngẫu nhiên cực nhỏ và độc lập diễn ra liên tục trong từng khoảng thời gian $\delta t$ 
	$$(W_t - W_s) = \sum_{i=1}^n \Delta W_i$$
- Theo **Định lý Giới hạn Trung tâm (Central Limit Theorem - CLT)**, khi số lượng bước nhảy $n \to \infty$ ($\delta t \to 0$), tổng của vô số các biến ngẫu nhiên độc lập, cùng phân phối có phương sai hữu hạn sẽ **tự động hội tụ về một Phân phối Chuẩn (Gaussian Distribution)**
# Tại sao kỳ vọng lại bằng đúng $t - s$ 
- $$\text{Var}(W_t - W_s) = \sum_{i=1}^n \text{Var}(\Delta W_i)$$
- Khi nén thời gian $\delta t \to 0$, để phương sai của chuyển động không bị triệt tiêu về $0$ cũng như không bùng nổ lên vô tận khi $n \to \infty$, độ lớn của mỗi bước nhảy không gian $\Delta x$ phải được thiết lập theo tỉ lệ căn bậc hai của thời gian: $\Delta x = \sqrt{\delta t}$
- Do đó, phương sai của mỗi bước nhảy nhỏ bằng: $$\text{Var}(\Delta W_i) = (\sqrt{\delta t})^2 = \delta t = \frac{t - s}{n}$$
- **Tính dừng của số gia (Stationary Increments):** Mức độ phân tán (phương sai) của số gia $(W_t - W_s)$ chỉ phụ thuộc duy nhất vào **độ dài khoảng thời gian trôi qua** $(t - s)$, chứ không phụ thuộc vào mốc thời gian bắt đầu $s$ (nghĩa là $W_t - W_s$ có cùng phân phối với $W_{t-s} - W_0 = W_{t-s} \sim N(0, t - s)$)
**Tóm lại:** Nhờ sự kết hợp giữa **Định lý Giới hạn Trung tâm** (biến tổng các bước nhảy thành phân phối chuẩn) và **phép chuẩn hóa bước nhảy** $\Delta x = \sqrt{\Delta t}$ (giúp phương sai không bị bùng nổ), phân phối của số gia trong Quá trình Wiener hội tụ mượt mà về dạng chuẩn tuyệt đẹp $(W_t - W_s) \sim N(0, t - s)$57
---

Đến đây thì xuất hiện thêm câu hỏi: "Quy tắc $\sqrt{t}$ này ảnh hưởng đến việc năm hóa chỉ số sharpe (nhân với $\sqrt{252}$ ) như nào?"
