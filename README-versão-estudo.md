# 🐳 Conversão de Temperatura – Projeto Docker

Este projeto foi desenvolvido durante uma das minhas aulas práticas de **Docker**, com o objetivo de compreender o **ciclo completo de containerização** de uma aplicação **Node.js**.

O repositório original foi clonado a partir de:  
👉 [github.com/lbsantana/conversao-temperatura-auladocker](https://github.com/lbsantana/conversao-temperatura-auladocker)

---

## 🚀 Objetivo

Containerizar uma aplicação Node.js simples de conversão de temperatura, praticando desde a criação do container até a execução da aplicação dentro dele.

---

## 🧩 Etapas Realizadas

1. **Criação do Container Interativo**  
   - Baseado na imagem oficial do **Ubuntu**.  
   - Container criado com o comando:
     ```bash
     docker run -it ubuntu /bin/bash
     ```

2. **Instalação Manual das Dependências**  
   Dentro do container, foram instaladas as ferramentas necessárias:
   ```bash
   apt update && apt install -y nodejs npm
   ```

3. **Cópia dos Arquivos do Projeto para o Container**
   - Utilizei o comando `docker cp` para transferir o conteúdo do projeto local para dentro do container:
     ```bash
     docker cp ./conversao-temperatura <container_id>:/app
     ```

4. **Execução da Aplicação Dentro do Container**
   - A aplicação foi iniciada manualmente dentro do container:
     ```bash
     cd /app
     npm install
     node app.js
     ```

5. **Acesso via Navegador**
   - O container foi configurado para expor a aplicação na porta:
     ```
     localhost:8080
     ```

---

## 🧠 Conceitos Praticados

- Isolamento de ambientes com containers  
- Manipulação de imagens e containers  
- Instalação manual de dependências dentro do ambiente Docker  
- Transferência de arquivos entre o host e o container  
- Execução e monitoramento de aplicações em ambiente isolado  
- Entendimento do fluxo de desenvolvimento → build → execução  

---

## 🔍 Resultado

A aplicação foi executada com sucesso dentro do container, respondendo corretamente às requisições na porta **8080**, demonstrando na prática:
- A importância da **reprodutibilidade de ambientes**  
- Como o **Docker simplifica a entrega de aplicações Node.js**  
- O ganho de **consistência entre os ambientes de desenvolvimento e produção**

---

## 🧑‍💻 Tecnologias Utilizadas

- **Docker**
- **Ubuntu**
- **Node.js**
- **npm**

---

## 📘 Próximos Passos

- Criar um **Dockerfile** para automatizar todo o processo manual.  
- Publicar a imagem no **Docker Hub**.  
- Integrar com **Docker Compose** para gerenciar múltiplos serviços.

---

### ✍️ Autor

Lucas Barbosa Santana
🧑‍💻 Cloud & DevOps Engineer | AWS Certified Solutions Architect
🔗 linkedin.com/in/lbsantana
