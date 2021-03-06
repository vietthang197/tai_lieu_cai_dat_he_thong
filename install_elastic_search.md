# Cài đặt Elastic search trên centos

 * Tải bản cài đặt linux x86_64 trên trang : https://www.elastic.co/downloads/elasticsearch
 * Thực hiện giải nén file: **elasticsearch-8.1.1-linux-x86_64.tar.gz** và copy ra phân vùng khác
   * `tar -xf elasticsearch-8.1.1-linux-x86_64.tar.gz -C /app/programs`
 * Thực hiện start elasticsearch:
   * `cd /app/programs/elasticsearch-8.1.1/bin `
   * `./elasticsearch`
   * Sau khi chạy thì elastic sẽ print ra password ở màn hình console, username mặc định của elastic là 
   `elastic` và mật khẩu chính là ở console đó, như ở trong ví dụ mật khẩu là vùng bôi đỏ trên ảnh:
   ![](step_1.PNG)
   * Nếu như bạn bỏ qua hoặc quên mật khẩu, hãy chạy script reset lại mật khẩu elasticsearch:
    `/app/programs/elasticsearch-8.1.1/bin/elasticsearch-reset-password`
   * Truy cập vào trang : https://localhost:9200/ điền account: elastic/4vY+*0HCL1Cc5Tr7ZqSA màn hình sẽ hiển thị như sau:
   ![](step_2.PNG)
# Tắt bỏ ssl certificate cho elasticsearch
   
 * Mặc định elasticsearch bật ssl, nếu như ta dùng ở local không public ra bên ngoài thì hoàn toàn không cần.
 * Để tắt ssl, truy cập vào folder config: `/app/programs/elasticsearch-8.1.1/config/elasticsearch.yml` và sửa như sau
 ![](step_3.PNG)