# -INT3401-8-P1-Pacman-Search
Mô tả thuật toán P1

[Q1, Q2, Q3, Q4]
4 giải thuật DFS, BFS, UCS và A* cơ bản tương tự nhau, chỉ khác nhau là cấu trúc được sử dụng lần lượt là Stack, Queue, PiorityQueue(UCS và A* với hàm tính cost riêng).

Hàm bên trong khởi tạo list: visitedNode cho các state đã được duyệt
Đầu tiên ta check xem state đầu có phải là state kết thúc hay chưa.

Push startState vào cấu trúc tương ứng, rồi bắt đầu duyệt các node kề của của nó và lưu các node này lại. Sau đó tiếp túc lấy các node ra và xét cho đến khi không còn node nào nữa hoặc đã đạt đến trạng thái goalState.
Trong quá trình di chuyển, tiến hành lưu lại node cha trong actions

[Q5]
Trong Q5, đề bài bắt chúng ta tìm và đi qua các góc bằng BFS. Và để làm được điều này ta phải xác định trạng thái ban đầu getStartState(), hàm mục tiêu isGoalState() và các trạng thái tiếp theo getSuccessors().

Bổ sung startState sẽ là vị trí khởi đầu của Pacman
Mục tiêu sẽ là 4 điểm góc và lưu trong visitedCorners, mỗi khi Pacman đi đến 1 góc thì sẽ lưu lại góc đó, và trạng thái kết thúc sẽ là khi Pacman đi qua hết 4 góc đồng nghĩa với len(visitedCorners) = 4

Hàm successors là 1 bước đi của Pacman đến 1 vị trí không dính tường, giá trị  

[Q6] 
Yêu cầu thiết kế heuristic cho problem corner ở trên
Heristic của em sẽ chọn là khoảng cách manhattan là đường chim bay từ vị trí hiện tại đến góc.
Đầu tiên sẽ check còn corners nào chưa đến và sẽ tính toán khoảng cách đến mỗi góc.

[Q7] Chưa hoàn thành

[Q8] Hoàn thành thuật toán tham lam để ăn hết các dots 
Làm như ví dụ 6
