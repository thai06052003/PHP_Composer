# Package Manager

- CCoong cu quản lý gói / thư viện / dêpndencies
- Javascript: npm, yarn, ...
- PHP: composer

# File config

- Javascript: package.json
- PHP: composer.json

### Lưu ý require packages:
- "require": {
        "phpmailer/phpmailer": "*"  <!-- Lấy phiên bản mới nhất -->
        "phpmailer/phpmailer": "^6.9.1"  <!-- Lấy phiên bản 6.9.1 -->
    }
- composer require phpmailer/phpmailer  <!-- dùng câu lệnh trong Terminal để cài đặt (auto cài phiên bản mới nhất nếu không chọn phiên bản) -->
- composer remove phpmailer/phpmailer  <!-- dùng câu lệnh trong Terminal để xóa thư viện hoặc có thể xóa trong require rồi dùng câu lệnh update -->

# Lưu ý require-dev packages:
- "require": {
        "phpmailer/phpmailer": "*"  <!-- Lấy phiên bản mới nhất -->
        "phpmailer/phpmailer": "^6.9.1"  <!-- Lấy phiên bản 6.9.1 -->
    }
- ^1.1.0: lên phiên bản cao nhất của bản 1
- 1.1.* : lên phiên bản cao nhất của 1.1.
- composer require phpmailer/phpmailer --dev  <!-- dùng câu lệnh trong Terminal để cài đặt (auto cài phiên bản mới nhất) -->
- composer remove phpmailer/phpmailer --dev  <!-- dùng câu lệnh trong Terminal để xóa thư viện hoặc có thể xóa trong require rồi dùng câu lệnh update -->

# Lưu ý xóa:
- Có thể xóa vendor và tạo lại bằng update
- Có thể xóa lock và tạo lại bằng update hoặc install (nhưng không khuyến khích vì sẽ phát sinh lỗi không mong muốn)

# Câu lệnh
composer init:
composer install:
composer update:
composer remove:
composer dump-autoload

# PSR-4 Autoload
- Để dễ dàng chia sẻ dùng lại code giữa các frameword, giữa các dự án ..., cộng đồng PHP thống nhất một cách thức tự động nạp thư viện theo một chuẩn bố trí thư viện
* Việc thống nhất đso hình thành một tiêu chuẩn nên tuân theo đó là PSR-4 Autoload
...
\<NamesapceName>(\<SubNamespaceNames>)*\<ClassName>
...
- Namespace: Tiền tố đầu tiên bắt buộc phải có - được hiểu là tên vendor. Tên này do bạn tự đặt, sao cho không xung đột với tên các thư viện khác.
- SubNamespaces: Các namespaces con (theo sau NameSpace đàu tiên - vendor)
- ClassName: Bắt buộc phải có và phải có tên file PHP trùng tên ClassName ở thư mục tương ứng với namespace cuối cùng (ClassName.php), trong file đó sẽ định nghĩa nội dung của code của lớp

# ClassMap Autoload

# Cài đặt Package theo phiên bản và cập nhật

# Composer Update và Composer Install

- Composer Update: Chạy các bản cập nhật trong file composer.json
- Composer Install: Ưu tiên chạy trong file composer.lock, nếu không có chạy trong file composer.json
- Composer install -no-dev --> Chỉ cài require
- Composer install  --> Cài cả require và required-dev

Tips: Clone Repository --> Composer install
Composer Update thường sử dụng ở môi trường dev