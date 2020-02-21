## No Linux ou MAC
chmod 0400 namefile.pem
ssh -i namefile.pem ec2-user@IPpublic
- namefile.pem é o arquivo gerado pela aws quando criar a instancia
- IPpublic é o IP disponível nas configurações da instancia

## No windowns 10
ssh -i C:\CaminhoAteOArquivo\namefile.pem ec2-user@IPpublic
- se houver erro, entre nas configurações avançadas de segurando do arquivo namefile.pem e libere a permissão para seu usuário
