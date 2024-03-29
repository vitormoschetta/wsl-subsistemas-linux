# WSL

### Instalar WSL:
<https://docs.microsoft.com/pt-br/windows/wsl/install-manual>


### Instalar Distribuição Linux
A distribuição Linux pode ser baixada pela Microsoft Store.  
Basta abrir o Microsoft Store (Loja) pelo menu iniciar e procurar por Ubuntu e baixar.


### Executar o Ubuntu
No menu do Windows um ícono do Ubuntu ficará disponível, clique nele e informe os dados pedidos (usuario e senha do sistema).  


### Instalar Windows Terminal (no Windows)
Também pode ser baixado pela Microsoft Store.   
Esse terminal pode ser utilizado tanto para o PowerShel, cmd (windows) quanto para bash (linux).


### Instalar .NET (no WSL Ubuntu)
```
sudo wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb

sudo apt-get update
sudo apt-get install apt-transport-https
sudo apt-get update
sudo apt-get install dotnet-sdk-5.0
```


### Instalar GIT (no WSL Ubuntu)
O Git já vem instalado por padrão nas distribuições Ubuntu.


### Configurar SSH local e gravar chave publica no repositório remoto (GitHub, Bitbucket, etc)
Obs: O Git já vem instalado por padrão nas distribuições Ubuntu.


### Instalar VSCODE (no Windows)
<https://docs.microsoft.com/pt-br/windows/wsl/tutorials/wsl-vscode>  
Neste caso acessaremos o WSL (Ubuntu).


### Instalar Docker (no WSL Ubuntu)
<https://medium.com/codigorefinado/docker-no-linux-dentro-do-windows-10-com-wsl-2-f52b91931267>  
Acessaremos os container remotamente pelo VSCODE.


### Habilitar acesso Docker com usuário não root (no WSL Ubuntu)
```
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker 
```


### Instalar Portainer como interface grafica para Containeres ((no WSL Ubuntu)
```
docker run -d -p 9000:9000 --name portainer --restart always --network=host -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer
```

Obs: O Windows mapeia automaticamente a porta 9000 do localhost do WSL Ubunto para a mesma porta do localhost do  Windows. Logo no Windows é possível acessar no browser:

<http://localhost:9000/>



### WSL não conecta na VPN privada 
Para se conectar a VPN de uma corporação instalamos um aplicativo VPN client no Windows e nos conectamos com credenciais da empresa.  

Se o nosso código fonte ou qualquer outro arquivo de nossos projetos dependam de um servidor que só é acessível na VPN corporativa, teremos um problema: o WSL não conseguirá se conectar nessa rede. Segue solução:

No terminal do WSL (distro Linux):
```
pconfig.exe /all
```
Após o comando acima, identifique o DNS da VPN.

Abra o seguinte arquivo:
```
sudo vi /etc/resolv.conf
```

Adicione o endereço DNS encontrado anteriormente ao **nameserver**:
```
nameserver 192.168.0.1 (algo do tipo)
```

Execute:
```
sudo ln -s ../run/resolvconf/resolv.conf resolv.conf
```

<https://docs.microsoft.com/pt-br/windows/wsl/troubleshooting>  
<https://askubuntu.com/questions/134121/how-to-restore-recreate-etc-resolv-conf-files>
