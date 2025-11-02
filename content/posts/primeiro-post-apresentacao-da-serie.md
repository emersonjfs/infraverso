---
title: "Infraverso: o início de um laboratório DevOps aberto"
description: "Apresentação do blog e do plano da série: Vagrant, Git, Hugo e deploy no OCI — do zero ao ar, com práticas que funcionam no dia a dia."
date: 2025-11-02
draft: false
tags: ["devops", "linux", "hugo", "vagrant", "git", "oci"]
categories: ["Apresentação"]
slug: "infraverso-inicio-laboratorio"
---

Este é o post de abertura do InfraVerso: uma série prática para montar, do zero, um laboratório DevOps replicável — do ambiente local com Vagrant e Hugo ao deploy no OCI, com foco em clareza e repetibilidade.


## Olá! Eu sou Emerson Santos

SysAdmin Linux L2 e entusiasta de infraestrutura e automação. Este espaço nasce para documentar um laboratório prático que uso no dia a dia e que você pode reproduzir em casa: desenvolvimento local no Linux Mint, homologação com Vagrant/libvirt e publicação em produção no Oracle Cloud (OCI). A ideia é compartilhar caminhos testados, atalhos e os “porquês” por trás das escolhas técnicas.

## O que você encontrará aqui

- Passo a passo enxuto, com comandos que realmente funcionam.
- Fluxos de trabalho repetíveis: escrever, testar, versionar, publicar.
- Resolução de problemas reais que surgem no processo (front matter, ícones, portas, NSG).

## A série: do zero ao ar

Esta série está organizada em camadas, para aprender cada ferramenta no seu contexto e depois integrar tudo.

1. Vagrant do zero: ambiente de dev Linux com rsync-auto  
   - Instalação, Vagrantfile mínimo, rede privada e sincronização automática Host → VM. Inclui o “setup de 3 terminais” (rsync-auto, Hugo, VSCode).

2. Git na prática: homolog → main → produção  
   - Fluxo que uso no projeto: commit em homolog, merge em main, push e pull-to-deploy. Inclui um “cartão de bolso” com a ordem dos comandos.

3. Hugo sem armadilhas: estrutura, front matter e tema  
   - Como organizar conteúdo, evitar conflitos de front matter, e usar ícones do tema Stack sem erros (pasta assets/icons e nomes válidos).

4. Integração local: Hugo + Vagrant + Git  
   - Do salvar no VSCode ao live reload na VM, com rsync-auto e validações úteis.

5. Deploy no OCI: pull-to-deploy simples e seguro  
   - git pull + hugo em produção, NSG com portas mínimas, e checklist de verificação pós-deploy.

6. Automação leve: webhook ou systemd  
   - Opções para disparar rebuild após push na main, mantendo controle e previsibilidade.

## Padrões e boas práticas do laboratório

- Simetria entre homolog e produção sempre que possível (mesmo layout de diretórios, mesmas versões de ferramentas).
- Segurança por padrão: portas mínimas liberadas, chaves SSH, e serviços nomeados claramente.
- Reprodutibilidade: tudo versionado em Git com mensagens de commit objetivas e ordem de execução definida.

## Como acompanhar

- A seção “Portfólio” lista os artefatos e repositórios do laboratório.
- “Archives” reúne todos os posts em ordem.
- No “Sobre”, você encontra meus contatos: LinkedIn, X/Twitter e GitHub.

Se quiser montar o laboratório junto, prepare um ambiente Linux com VSCode, Git, Vagrant/libvirt e uma conta no OCI. No próximo post, começamos pelo Vagrant do zero. Até lá!