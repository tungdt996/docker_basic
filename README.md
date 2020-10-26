# 1.KIẾN TRÚC DOCKER
- Docker có kiến trúc client- server. 
- Docker server ( deamon) nằm trong docker host chịu trách nhiệm build, run, distrubute Docker container
- Docker clinet(có thể nằm cùng server với daemon) là phương thức chính để người dùng thao tác với Docker. Khi gõ lệnh thì clinet sẽ gửi request đến server thông qua API.
- Docker registry là nơi lưu trữ các image (vd: docker hub) hoặc tự tạo ra.
- Docker object nằm trong docker host bao gồm IMAGE và container.
Image là template chứa các package cần thiết cho service chạy trong container

<img src="https://luanbn.files.wordpress.com/2015/08/server_side_code_flow.png">

# 2.CÀI ĐẶT DOCKER (EE cho doanh nghiệp, CE cho dev-cá nhân)
 - update package
      - sudo apt-get update
 - install package cần thiết cho docker
      - sudo apt install apt-transport-https ca-certificates curl software-properties-common
 - Add Docker’s official GPG key (add key bản free)
      - curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
 - Verify that you now have the key with the fingerprint
(xác nhận key)
      - sudo apt-key fingerprint 0EBFCD88
 - set đường dẫn đến thư mục tải các bản update tiếp theo 
(nằm trong /etc/apt/source.list)
      - sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable
 - update lại package sau khi add thêm đường dẫn
      - sudo apt-get update
 - install docker
      - sudo apt-get install docker-ce
