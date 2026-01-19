# Cantunsee Result
![Test result](images/test-result.png)


# SOFT-test

Dự án này là bài thực hành kiểm thử với JUnit 5. Tôi viết một class để phân tích điểm học sinh và dùng Maven để chạy Unit Test cho nó.

Chức năng chính

countExcellentStudents(List<Double> scores)
Đếm số học sinh đạt loại Giỏi (>= 8.0). Điểm < 0 hoặc > 10 thì bỏ qua.

calculateValidAverage(List<Double> scores)
Tính điểm trung bình của các điểm hợp lệ trong danh sách (chỉ lấy điểm từ 0 đến 10).

Cấu trúc dự án

Project được tổ chức theo chuẩn Maven:

src/main/java/nigalas/ : mã nguồn chính (StudentAnalyzer.java)

src/test/java/nigalas/ : mã kiểm thử (StudentAnalyzerTest.java)

pom.xml : cấu hình Maven + JUnit 5 + JDK

Yêu cầu hệ thống

Java JDK: 23

Apache Maven: 3.6.0 trở lên

Có thể làm bằng VS Code (có Extension Pack for Java)

Cách chạy test

Mở terminal tại thư mục có pom.xml rồi chạy:

mvn clean test


Nếu đúng hết thì Maven sẽ chạy toàn bộ test và báo BUILD SUCCESS.