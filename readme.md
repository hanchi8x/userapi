## Cách cài đặt

1. Clone source

2. Cài đặt Laravel bằng lệnh sau

        composer install

3. Tao database trống tên tùy chọn

4. Fix file .env với thông tin database

        DB_DATABASE=your_database
        DB_USERNAME=your_username
        DB_PASSWORD=your_password

your_database, your_username, your_password là những thông tin database của bạn.

5. Chạy laravel bằng lệnh sau 

        php artisan serve

## Test api với 

1. Dùng API/login để đăng nhập

        POST http://localhost:8000/api/login?email=your_mail&password=your_password 
        Request Headers url HTTP/1.1
        Host: localhost:8000
        Content-Type: application/json
        Content-Length: 0

        Các tham số: 
        email: email muốn login
        password: mật khẩu

2. Dùng API/register để đăng ký

        POST http://localhost:8000/api/register?name=disired_name&email=disired_email&password=disired_password&c_password=disired_password
        Request Headers
        content-type: application/json

        Các tham số: 
        name: tên muốn tạo (tên hiển thị)
        email: mail dùng để đăng nhập
        password: mật khẩu dùng để đăng nhập
        c_password: mật khẩu dùng để đăng nhập

3. Dùng API/details để xem thông tin

        POST http://localhost:8000/api/details
        Request Headers
        authorization: Bearer .$accessToken 
        accept: application/json
        content-type: application/x-www-form-urlencoded

4. Dùng API/update để cập nhập thông tin

        POST http://localhost:8000/api/update?name=changes_name&address=changed_address&tel=tel 
        Request Headers
        accept: application/json
        content-type: application/x-www-form-urlencoded
        authorization: Bearer .$accessToken 

        Các tham số 
        name: tên muốn thay đổi
        address: địa chỉ của người dùng muốn thay đổi
        tel: số điện thoại của người dùng muốn thay đổi

Good Luck! 
Nếu có bất kỳ thắc mắc nào xin vui lòng liên hệ, 01227772057, Gặp A Cường.
