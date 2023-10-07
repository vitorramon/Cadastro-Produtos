# Cadastro-Produtos com  React e SpringBoot


## Introdução

Este repositório visa aprofundar o entendimento sobre o React e SpringBoot.

## Objetivo

O objetivo deste repositório é:

- Desenvolver um conhecimento sólido sobre o React.
- Compreender como a implementanção de vários sistemas.

## Pré-requisitos

Antes de começar a explorar o Cadastro de Produtos com React e SpringBoot, é fundamental ter conhecimentos prévios em:

- Lógica de programação.
- JavaScript.
- Java.
- Máquinas Virtuais 
- Linux
- Banco de Dados

## Tecnologias Utilizadas

As seguintes tecnologias são utilizadas neste projeto:

- Visual Studio Code.
- Node.
- NPM.
- SpringBoot
- VirtualBox
- Ubuntu Server
- JDK

## Spring Boot

- Maven
- Lombok
- Spring Web
- JPA
- MySQL

## Visual Studio Code

- Extension Pack for Java
- Extension Pack for SprinBoot
- Lombok
- ThunderClient

## Passos 

1º Baixar e configurar plataforma de virtualização de sua preferência
2º Configurar a rede da VM para que ela tenha conectividade com a rede externa
3º Instalar o servidor
4º Instalar o sistema de Banco de Dados

`sudo apt install mysql-server`: Instala o MySQL Server.
`sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf`: Edita o arquivo de configuração do MySQL.
- bind-address = 0.0.0.0 :Esta é a linha para editar conforme a necessidade de acesso, neste exemplo está permitindo conexões realizadas com qualquer IP.

5º Configurar acesso ao banco

`sudo mysql -u root -p`: Acessa o MySQL como root.
`CREATE USER 'seu_usuario'@'%' IDENTIFIED BY 'sua_senha';` : Concede permissões ao usuário seu_usuario para acessar o MySQL de qualquer host (%). 
`GRANT ALL PRIVILEGES ON *.* TO 'seu_usuario'@'%' WITH GRANT OPTION;` : 
`FLUSH PRIVILEGES;`: Recarrega as tabelas de privilégios para aplicar as alterações.

6º Configuração de tráfego no caso de Firewall

`sudo ufw allow 3306/tcp`: Permite o tráfego na porta MySQL (padrão 3306) para acesso de conexões externas.
`sudo service mysql restart`: Reinicia o serviço MySQL para aplicar as alterações.

6º Configurar o SpringBoot

- spring.datasource.url=jdbc:mysql://ip-da-vm:porta-do-banco/nome-do-banco
- spring.datasource.username=seu-usuario
- spring.datasource.password=sua-senha


