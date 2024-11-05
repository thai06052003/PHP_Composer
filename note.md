# Package Manager

- CCoong cu quản lý gói / thư viện / dêpndencies
- Javascript: npm, yarn, ...
- PHP: composer

## File config

- Javascript: package.json
- PHP: composer.json

### Lưu ý require packages:
- "require": {
        "phpmailer/phpmailer": "*"  <!-- Lấy phiên bản mới nhất -->
        "phpmailer/phpmailer": "^6.9.1"  <!-- Lấy phiên bản 6.9.1 -->
    }
- composer require phpmailer/phpmailer  <!-- dùng câu lệnh trong Terminal để cài đặt (auto cài phiên bản mới nhất) -->
- composer remove phpmailer/phpmailer  <!-- dùng câu lệnh trong Terminal để xóa thư viện hoặc có thể xóa trong require rồi dùng câu lệnh update -->

#### Lưu ý require-dev packages:
- "require": {
        "phpmailer/phpmailer": "*"  <!-- Lấy phiên bản mới nhất -->
        "phpmailer/phpmailer": "^6.9.1"  <!-- Lấy phiên bản 6.9.1 -->
    }
- composer require phpmailer/phpmailer --dev  <!-- dùng câu lệnh trong Terminal để cài đặt (auto cài phiên bản mới nhất) -->
- composer remove phpmailer/phpmailer --dev  <!-- dùng câu lệnh trong Terminal để xóa thư viện hoặc có thể xóa trong require rồi dùng câu lệnh update -->

#### Lưu ý xóa:
- Có thể xóa vendor và tạo lại bằng update
- Có thể xóa lock và tạo lại bằng update hoặc install (nhưng không khuyến khích vì sẽ phát sinh lỗi không mong muốn)

****** Câu lệnh
composer init:
composer install:
composer update:
composer remove: