<h1 style="text-align: center">Deploy</h1>

> **Heroku là gì?**

1. Nó là nền tảng đám mây cho phép các lập trình viên xây dựng, triển khai, quản lý và mở rộng ứng dụng (PaaS – Platform as a service).

2. Nó rất linh hoạt và dễ sử dụng, cung cấp cho một con đường đơn giản nhất để đưa sản phẩm tiếp cận người dùng. Nó giúp các nhà phát triển tập trung vào phát triển sản phẩm mà không cần quan tâm đến việc vận hành máy chủ hay phần cứng…

> **Điều kiện tiên quyết**

1. Tạo tài khoản heroku (không cần thẻ visa or master card)

2. Tải the Heroku Command Line Interface (CLI): https://devcenter.heroku.com/articles/getting-started-with-python#set-up

3. Có tài khoản github hoặc nếu không có thể dùng git của heroku

4. Tải git về máy: https://git-scm.com/

> **Tạo Postgres DB**

1. mở Heroku CLI lên

2. Thêm add-on: heroku addons:create heroku-postgresql:hobby-dev

> **Connect DB Local**

<img src="https://drive.google.com/uc?export=view&id=125QXdBSTp9JVm9k6LfS6FkgI35a3YLFR"></img>

1. Lấy thông tin kết nối DB

2. Tải Postgres : https://www.postgresql.org/download/

3. Start PgAdmin => tạo mới server => điền thông tin kết nối

<p align="center">
<img src="https://drive.google.com/uc?export=view&id=10vWKgZd1gn-CQ-WMODpXhJD9mVnaYeL9"></img>
</p>

> Note: Heroku bắt buộc phải chọn SSL require

<p align="center">

<p align="center">
<img src="https://drive.google.com/uc?export=view&id=1wiCoYWpAwfzJfngjGx0GShCZHP33qkEb"></img>
</p>

> **Chỉnh sửa URL và thông tin trong Spring**


---
Đây là config trong application.properties

> spring.datasource.url=jdbc:postgresql://ec2-3423826109.compute1.amazonaws.com:5432/dbutm1kdt39lna?currentSchema=public
spring.datasource.username=hhqdpmluyeoixs
spring.datasource.password=82cc6d3b82fcdd68c87378ae4b99262818be23c7103db79793850bffd43d8db1

---


> **Python Config**

1. Cần có file requirements.txt để điều thông tin các plugin và framework cần thiết
Ví dụ:

![i1.png](/deploy/i1.png)

2. Cần có file runtime.txt chứa thông tin version Python
Ví dụ:

![i2.png](/deploy/i2.png)

> **Deploy**

1. Ở giao diện app chọn tab deploy

![i3.png](/deploy/i3.png)

2. Chọn github và connect tài khoản và repo

![i4.png](/deploy/i4.png)

3. Click chọn Automatic Deploys (Để tự động build lại khi branch có thay đổi)

4. Click Deploy Branch





