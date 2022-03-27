# Cài đặt Elastic search trên centos

 * Tải bản cài đặt linux x86_64 trên trang : https://www.elastic.co/downloads/elasticsearch
 * Thực hiện giải nén file: **elasticsearch-8.1.1-linux-x86_64.tar.gz** và copy ra phân vùng khác
   * tar -xf elasticsearch-8.1.1-linux-x86_64.tar.gz -C /app/programs
 * Cấu hình tắt bỏ ssl certificate ở : `/app/programs/elasticsearch-8.1.1/config/elasticsearch.yml`
   * ![](step_1.PNG)