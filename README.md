# wsl-subsistemas-linux

### Habilitar WSL:
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
Reinicie a máquina.
<br>


### Atualizar WSL
aso já possua o WSL 1 instalado, após a reinicialização, abra um terminal (Power Shell ou Windows Terminal) e execute o comando abaixo.
```
wsl --set-default-version 2
```
<br>


## Instalar Ubuntu
Basta abrir o Microsoft Store (Loja) pelo menu iniciar e procurar por Ubuntu e baixar.

### Executar o Ubuntu
No menu do Windows um ícono do Ubuntu ficará disponível, clique nele e informe os dados pedidos (usuario e senha do sistema).
<br>


## Instalar .NET
```
sudo wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb

sudo apt-get update
sudo apt-get install apt-transport-https
sudo apt-get update
sudo apt-get install dotnet-sdk-3.1
```
<br>

Fontes:
<https://balta.io/artigos/wsl>
<https://docs.microsoft.com/pt-br/windows/wsl/>


