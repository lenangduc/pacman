# pacman
search algorithm

1. thuật toán DFS(tìm kiếm theo chiều sâu)
b1: lấy ra trạng thái bắt đầu bằng câu lệnh problem.getStartState()
b2: xét trạng thái bắt đầu có phải là kết thúc hay chưa. nếu đúng thì return về rỗng. 
b3: khai báo:
	- mystack: lưu bằng stack và lưu các node chưa xét đến 
	- path: lưu bằng stack và lưu đường đi. 
	- visited: lưu bằng mảng 1 chiều và lưu các node đã ghé qua. 
b4: đẩy vào các giá trị ban đầu cho mystack là trạng thái bắt đầu, còn path là trống.
b5: xét vòng lặp while đến khi nào mystack rỗng. 
	+ lấy node hiện tại trong mystack, 
	+ lấy path dẫn đến node hiện tại trong path.
	+ xét node hiện tại có trong visited hay không. 
	+ xét điểm hiện tại có phải là kết thúc hay không. nếu kết thúc thì trả về path. 
	+ vòng for để lấy node tiếp theo, direction, cost của các điểm lần kề và cập nhật lại path, mystack.
cứ lặp mãi cho đến khi mystack rỗng. 

2. thuật toán BFS( tìm kiếm chiều rộng)
+ tương tự như trên. chỉ cần thay stack bằng queue là được. 

3. thuật toán ucs ( uniformCostSearch) 
dùng cho đồ thị có trọng số.
dùng priorityQueue. 
làm tương tự như trên nhưng có 1 số điều thay đổi nhỏ:
	- thay stack bằng priorityQueue. 
	- xét trạng thái ban đầu thì độ ưu tiên = 0.
	- độ ưu tiên phí sau sẽ bằng độ ưu tiên phí trước cộng cost từ node hiện tại đến node tiếp theo
	- cập nhật lại mystack, path thì cx phải cập nhật lại độ ưu tiên. 
4. thuật toán A*.
làm tương tự câu 3 nhưng có 1 số điều nhỏ cần thay đổi. 
	- độ ưu tiên phí sau sẽ bằng độ ưu tiên phí trước cộng cost từ node hiện tại đến node tiếp theo
		cộng với giá trị lấy được từ hàm đánh giá heuristic.
 
