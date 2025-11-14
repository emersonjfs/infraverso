+++
date = '2025-11-12T02:39:04-03:00'
draft = false
title = 'Vagrant'
Image = "vagrant-hashicorp.png"
+++

## Desenvolvimento de ambientes virtuais com HashiCorp Vagrant

## Conceitos de Virtualização

### O que é Virtualização ?

![Arquiteturas](arquiteturas.png)

Virtualização é o processo de criar uma versão virtual de algum recurso, por exemplo uma rede de servidores, sistemas
operacionais, dispositivos de armazenamento, etc...

## Benefícios da virtualização

### Gerenciamento de recurso

Agora podemos gerenciar o quanto de recurso computacional cada serviço irá consumir, considerando que cada máquina
virtual manterá um serviço rodando.

### Segurança

Máquinas virtuais proporcionam maior segurança devido a isolação entre elas, sua conversa com a máquina hospedeira é
apenas para operação do hardware virtual

### Automação

Atualmente existem diversas ferramentas que permitem criar infraestruturas virtualizadas em questão de segundos

## O que é o Vagrant

![Vagrant Hashicorp](vagrant-1.png)

Vagrant é uma ferramenta de automação escrita em Ruby e mantida pela HashiCorp, a mesma empresa responsável por
outras ferramentas como o Terraform, Vault e o Nomad. Através de um script é possível subir uma infraestrutura inteira e
até mesmo configurar suas máquinas.

O Vagrant possui uma linguagem própria para os scripts baseada em Ruby e permite descrever todos os aspectos de uma
máquina virtual, como hostname, ip, cpu, memoria, disco, sistema operacional, quantidades de máquinas que serão criadas,
scripts que devem ser executados para o provisionamento, entre outros aspectos. Toda máquina criada pelo Vagrant é feita
através de uma Vagrantbox, que é uma imagem base com todos os pacotes que uma máquina virtual deve possuir quando
for criada.

## Provedor x Provisionador

O Vagrant trabalha com dois papéis distintos:

## Provedor

O provedor (provider) é o responsável pela criação da instância dos ambientes, geralmente uma máquina virtual, podendo
também ser uma instância em alguma Cloud.

## Provisionador

O provisionador (provisioner) é o responsável pelas tarefas a serem executadas de forma automatizada, como por exemplo
a instalação de pacotes e configuração do sistema.

## Fluxo de Criação de uma máquina virtual:

![Fluxo Vagrant](fluxo_vagrant.png)

A construção de uma máquina virtual pelo Vagrant se inicia com o download de uma imagem base através da Vagrant Cloud,
após o download é iniciado o processo de criação e parametrização da máquina no virtualizador (hypervisor) escolhido.
Por padrão o Vagrant possúi suporte a diversos providers como Virtualbox, Docker, Hyper-V, podendo ser expansível através
de plugins a outras soluções como VMWare e AWS.

É importante que seja verificado se a imagem em questão fornece suporte ao Hypervisor escolhido. Após a criação da
máquina no Hypervisor, o processo de execução do provisionador é executado.

## Instalação do Vagrant

Antes de começar, gostaria de salientar que estarei utilizando nesse exmplo de instalação a versão do ubuntu 24.04, mas,  o processo de instalação para as demais distro é similar, de qualquer forma estarei disponibilizando a baixo o link para o site do projeto "vagrant" para que vocês possam acessar e conhecer um pouco melhor dessa ferramenta que ao meu ver é execelente para construção de pequenos e projetos e projetos pessoais. Eu utilizo muito ela na construção de meus labs, por ser uma ferramenta com curva de aprendizado relativamente simples e está alinhada com conceito de Devops.

 ~~**Site:**~~ [hashicorp vagrant](https://developer.hashicorp.com/vagrant)

O Processo de instalação do Vagrant é bem simples, basta baixar o instalador correspondente ao seu sistema operacional,
instalar com seu gerenciador de pacotes e então validar a Instalação.

