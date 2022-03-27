# Cài đặt oracle JDK 11 trên centos

 * Gỡ cài đặt bản open jdk đã cài đặt từ trước
   * `yum list java*`
   * `sudo yum -y remove java*`
 * Tải jdk trên trang chủ Oracle : https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html bản **rpm package**
 * Chạy lệnh cài đặt
   * `sudo rpm -i <rpm_file>`  (Ví dụ: jdk11_oracle_bin.rpm)
 * Gõ **java -version** và **javac -version** để kiểm tra