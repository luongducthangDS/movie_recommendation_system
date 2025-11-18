🎬 Movie Recommendation System  
Giới thiệu  
Project xây dựng một hệ thống gợi ý phim dựa trên dữ liệu MovieLens. Hệ thống có thể đề xuất phim cho người dùng dựa trên hành vi đánh giá trước đó và sự tương đồng giữa các người dùng hoặc phim.

Bài toán  
Input: dữ liệu người dùng (userId), phim (movieId), và điểm đánh giá (rating).
Output: danh sách các bộ phim được gợi ý cho một người dùng hoặc cho một bộ phim bất kỳ.
Target: giúp người dùng khám phá những bộ phim phù hợp với sở thích của họ.

Phương pháp  
+ TF-IDF (Term Frequency – Inverse Document Frequency)
  Dùng để mã hoá nội dung văn bản (title + genres).
  Mỗi phim được biểu diễn thành một vector trong không gian từ vựng.

+ Cosine Similarity
  Đo độ tương đồng giữa các vector TF-IDF.
  Tìm ra các phim có nội dung gần nhất với phim đầu vào.

Quy trình:
  Tiền xử lý dữ liệu phim (tựa phim, thể loại).
  Tạo ma trận TF-IDF.
  Tính cosine similarity giữa các phim.
  Trả về Top-K phim tương tự.

Dataset
MovieLens 25M: tập dữ liệu công khai chứa hơn 25 triệu đánh giá từ hơn 160.000 người dùng.
Link tải: https://grouplens.org/datasets/movielens/25m/
Do file dataset rất lớn (>600MB), repo này không chứa trực tiếp dữ liệu.
