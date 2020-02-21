# Instalar Apache na instancia EC2
## acessar a internet pelas configurações do apache
- instancia Amazon Linux 2 AMI (HVM), SSD Volume Type 
## Acessar EC2
- no terminal
### Permitir acesso
sudo su
### Atualizar maquina
yum update -y
### Instalar httpd
yum install -y httpd.x86_64
### Start service
systemctl start httpd.service
systemctl enable httpd.service
### Testar funcionamento
curl localhost:80
### Visualizar no web browser
- no grupo de segurança liberar a porta 80
- copiar IP publico da instancia
- no browser:
http://IPpuiblic:80
### Configurar visulização do browser
- no terminal da instancia</br>
echo "Hello World" > /var/www/html/index.html
- ou </br>
echo "Hellow World from $(hostname -f)" > /var/www/html/index.html
