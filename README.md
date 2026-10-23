# ubuntu-server-ufw-firewall-lab
Sobre o projeto

Este projeto apresenta a implementação prática de um firewall utilizando UFW (Uncomplicated Firewall) em um servidor Ubuntu Server virtualizado com Oracle VirtualBox.

O objetivo foi compreender o funcionamento de regras de firewall, controle de conexões de entrada e exposição de serviços de rede.

Ambiente utilizado

Sistema operacional: Ubuntu Server

Virtualização: Oracle VirtualBox

Firewall: UFW

Serviço de rede: Nginx

Sistema hospedeiro: Windows

Protocolo testado: HTTP/TCP

Porta do serviço web: TCP 80

Redirecionamento no VirtualBox: porta 8080 do hospedeiro para a porta 80 do servidor

Atividades realizadas

Verificação do estado inicial do UFW.

Configuração das políticas padrão de entrada e saída.

Ativação do firewall.

Instalação e verificação do serviço Nginx.

Criação de regra para permitir conexões HTTP pela porta TCP 80.

Configuração do redirecionamento de portas no VirtualBox.

Teste de acesso ao servidor web pelo navegador do Windows.

Bloqueio do acesso HTTP e observação da interrupção da conexão.

Remoção da regra de bloqueio e restauração do acesso ao serviço.

Verificação das regras do firewall com o comando ufw status numbered.

Principais comandos

Consultar o estado do firewall:

sudo ufw status verbose

Definir política padrão para conexões de entrada:

sudo ufw default deny incoming

Permitir conexões de saída:

sudo ufw default allow outgoing

Ativar o firewall:

sudo ufw enable

Instalar o Nginx:

sudo apt update
sudo apt install nginx -y

Permitir acesso HTTP:

sudo ufw allow 80/tcp

Bloquear acesso HTTP:

sudo ufw deny 80/tcp

Consultar regras numeradas:

sudo ufw status numbered

Resultados obtidos

Foi possível acessar a página padrão do Nginx a partir do Windows por meio do redirecionamento de portas do VirtualBox.

Durante os testes, o bloqueio da porta HTTP interrompeu o acesso ao serviço. Após a remoção da regra de bloqueio e a restauração da permissão, o acesso foi restabelecido.

Conhecimentos praticados

Administração básica de servidores Linux.

Configuração de firewall no Ubuntu.

Controle de tráfego de entrada e saída.

Conceitos de portas TCP e protocolos de rede.

Virtualização e redirecionamento de portas.

Testes de conectividade e diagnóstico de serviços.

Próximos passos

Praticar regras de firewall para outros serviços.

Estudar o princípio do menor privilégio.

Explorar monitoramento de conexões e análise de logs.

Desenvolver laboratórios complementares de segurança de redes.

Projeto desenvolvido para fins educacionais, em ambiente virtualizado e controlado.
