# Docker_WSL2_Windows
Neste artigo vou mostrar como fazer instalação do Docker com o WSL2 no sistema Windows Home

Resolvi escrever este tutorial depois de bater a cabeça pra conseguir instalar o WSL2 na minha máquina. Como o sistema que eu utilizo é o Windows Home, os tutoriais que eu encontrava não davam certo; por isso a iniciativa.
Sou cientista de dados e estou fazendo um curso de engenharia de dados, para isso, precisei aprender a subir um cluster no Docker para rodar algumas ferramentas como: Kafka, MongoDB e Jupyter.

Sem mais delongas...

**Atualização do Windows**

Primeira coisa a ser verificada é se o seu Windows está atualizado, para as ferramentas que queremos instalar rodem de forma correta é preciso ter o Windows 10 em sua versão atualizada ou uma versão maior que 2004. É recomendado que a  máquina tenha pelo menos 8GB de memória RAM, ele até roda com 4GB mas, de forma bem lenta.

A atualização do sistema pode ser feita através do seguinte link: https://www.microsoft.com/pt-br/software-download/windows10


**Terminal**

Parece ser apenas um detalhe, mas não é… Na primeira vez que tentei entrar pelo terminal que havia na minha máquina eu não consegui, porque ele não dava a opção de abrir o Linux nele, por isso baixem esse terminal.

Para isso, basta entrar no Store da Microsoft e digitar: Windows Terminal


![imagem_terminal](https://github.com/Kelly002/Docker_WSL2_Windows/blob/main/imagem1.png)


Ele será muito útil, pois pela seta +, você vai conseguir abrir o terminal do Linux, depois que ele já estiver instalado. Assim como outros sistemas, tudo em um único lugar.


![foto_terminal](https://github.com/Kelly002/Docker_WSL2_Windows/blob/main/imagem2.png)


**Habilitando o Windows**

Para dar continuidade será necessário habilitar algumas opções no sistema Windows. Vá até o Painel de Controle, Programas, Ativar e desativar recursos do Windows. 
Selecione: Plataforma de máquina virtual, Plataforma do Hipervisor Windows e Subsistema de Windows para Linux

![foto_subsistema](https://github.com/Kelly002/Docker_WSL2_Windows/blob/main/imagem3.png)

Desta forma, vamos conseguir trabalhar com o Linux dentro de uma máquina virtual que trabalhe dentro do sistema Windows.

**Instalação do WSL**

Agora vamos fazer o download do kernel do WSL2, que é o subsistema Linux para Windows,  pelo seguinte site:

[kernel_WSL2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)


A instalação é bem simples, basta avançar e finalizar.

Feita a instalação vamos agora definir a versão 2 do WSL, digitando o seguinte comando pelo terminal:

```
--set -default - version 2
```

**Instalação do Linux**

Agora, vamos para a instalação do Linux, no Windows Store digitamos 'Linux' e vamos pegar o Ubuntu LTS.


![imagem_docker](https://github.com/Kelly002/Docker_WSL2_Windows/blob/main/imagem4.png)


**Download do Docker**

Vamos fazer a instalação do Docker, utilizando o seguinte link: https://hub.docker.com/editions/community/docker-ce-desktop-windows/


![imagem_instalacao_docker](https://github.com/Kelly002/Docker_WSL2_Windows/blob/main/imagem6.png)


Feito a instalação do Docker é preciso fazer o logout e login da máquina.

**Configurações do Docker**

Para isso, nós vamos em Settings, Resourchs, WSL Inplantion e vamos selecionar as opções que você quer que o Docker rode de maneira integrada com o seu sistema. No meu caso eu aproveitei e instalei também o Debian, o Alpine e o Linux.


![imagem_sistema](https://github.com/Kelly002/Docker_WSL2_Windows/blob/main/imagem7.png)


Para testarmos podemos abrir o terminal do Ubuntu (basta ir na seta ao lado do sinal “+” e abrir o terminal do Ubuntu) e rodar o Docker.


![imagem_terminal1](https://github.com/Kelly002/Docker_WSL2_Windows/blob/main/imagem8.png)


Pronto, o cluster foi subido com sucesso.


![imagem_terminal2](https://github.com/Kelly002/Docker_WSL2_Windows/blob/main/imagem9.png)


Espero que este meu tutorial te ajude e que você consiga prosseguir nessa nossa jornada de novos aprendizados.








