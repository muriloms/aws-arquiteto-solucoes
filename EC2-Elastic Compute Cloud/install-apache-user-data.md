# Instalar Apache na instancia EC2 utilizando o User Data
- Criar nova instancia Amazon Linux 2 AMI (HVM), SSD Volume Type 
- Na aba "Configure Instance", adicionar o seguinte código em "Advanced Details" "User data"
#!/bin/bash </br>
# install httpd (Linux 2 version) </br>
yum update -y </br>
yum install -y httpd.x86_64 </br>
systemctl start httpd.service </br>
systemctl enable httpd.service </br>
echo "Hellow World from $(hostname -f)" > /var/www/html/index.html </br>
