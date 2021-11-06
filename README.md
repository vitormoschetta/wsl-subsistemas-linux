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







