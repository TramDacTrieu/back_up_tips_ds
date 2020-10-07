# Điều Kiện Tiên Quyết

1. Biết kiến thức về Heroku

2. Biết kiến thức về Python

3. Có tài khoản Chatwork (╯°□°）╯︵ ┻━┻   

4. Get API Token ChatWork API

5. Set Up WebHook ChatWork

# Chơi Thôi

1. Đăng nhập vào tài khoản chatwork
2. Get API Token
3. Định hình trước URL để call
4. Ở bài viết này sẽ dùng Heroku -> nên url có dạng `xxx.herokuapp.com/xxx`
5. Đặt url của bạn vào đăng kí webhook -> url của tôi `xxx.herokuapp.com/webhook`
6. Chúng ta sẽ sử dụng 1 project có sẵn trên heroku được viết bằng python
7. Cách deploy lên heroku thì đọc lại bài này [DeplyToHeroku](/DeplyToHeroku) 
8. Deploy app này lên https://devcenter.heroku.com/articles/getting-started-with-python#prepare-the-app
9. Chúng ta sẽ chỉnh sửa code 1 xíu

> Một số khái niệm cần biết
ví dụ:
-- roomid là gì?
là id của 1 room chat trong chatwork (có thể là giữa 2 người hoặc là 1 nhóm chat)
-- Chatwork API token là gì?
là token để access vào API
-- Trong sample mẫu thì sẽ sử dụng python (framework django):
nếu chưa có kiến thức phần này nên xem qua 1 tí

> đây là code nè đồ ngốc


# Test Endpoint Thôi

> chưa có hình ảnh đâu! đang chuẩn bị
