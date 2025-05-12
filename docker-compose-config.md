version: '3.8'

services:
  web-custom: #Thay đổi tên Service theo yêu cầu thay đổi port, name
    build:
      context: ./docker/nginx
      dockerfile: Dockerfile
    ports:
      - "8081:80" #Thay đổi port máy chủ thành 8081
    volumes:
      - ./app:/var/www/html
      - ./docker/nginx/conf:/etc/nginx/conf.d
    depends_on:
      - php-custom #Cập nhật thay đổi để trỏ đến tên service mới
    networks:
      - app-network

  php-custom: #Tên service đã thay đổi
    build:
      context: .
      dockerfile: ./docker/php/Dockerfile
    volumes:
      - ./app:/var/www/html
    expose:
      - "9000"
    networks:
      - app-network

  db-custom: #tên service đã thay đổi
    image: mysql:latest
    environment:
      MYSQL_ROOT_PASSWORD: root # Giữ lại dòng này
      MYSQL_DATABASE: users
      # Xóa hai dòng sau:
      # MYSQL_USER: root
      # MYSQL_PASSWORD: ""
    ports:
      - "3308:3306" #port đã thay đổi 
    volumes:
      - db_data:/var/lib/mysql
    networks:
      - app-network

  phpmyadmin:
    image: phpmyadmin/phpmyadmin:latest
    ports:
      - "8080:80"
    environment:
      PMA_HOSTS: db-custom #cập nhật tên service
      PMA_PORT: 3306 #giữ nguyên vì posrt trong container vẫn là 3306
      PMA_USER: root
      PMA_PASSWORD: root
      PMA_ARBITRARY: 0
      PHP_UPLOAD_MAX_FILESIZE: 2M # Thêm dòng này
    depends_on:
      - db-custom #Cập nhật thay đổi để trỏ đến tên service mới
    networks:
      - app-network
    #extra_hosts: bỏ 2 dòng này vì với PMA_HOSTS:db-custom thì Docker compose tự động phân giải tên service trong mạng
      #- "db-custom:127.0.0.1" #Cập nhật thay đổi để khớp với tên service mới của dâtbase

networks:
  app-network:
    driver: bridge

volumes:
  db_data: