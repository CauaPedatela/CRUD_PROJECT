# CRUD PROJECT - Full Stack (Java & Angular)

Este é um projeto de estudo de um sistema CRUD completo, utilizando uma arquitetura de 3 camadas. O sistema integra um backend robusto em Java com persistência via Hibernate e relatórios Jasper, além de um frontend moderno em Angular.

## 🚀 Tecnologias Utilizadas

* **Backend:** Java 17, Maven, Hibernate 5, Wicket 7.
* **Frontend:** Angular 14, Bootstrap, Angular Material.
* **Banco de Dados:** MySQL 8.x.
* **Relatórios:** JasperReports.
* **Arquitetura:** MVC (Model-View-Controller) e princípios SOLID.

---

## 🛠️ Pré-requisitos (O que baixar por fora)

Para rodar este projeto localmente, você precisa instalar as seguintes ferramentas que não são gerenciadas automaticamente pelo código:

### 1. Java Development Kit (JDK) 17
O "motor" do backend.
* **Recomendado:** [Eclipse Temurin (Adoptium)](https://adoptium.net/temurin/releases/?version=17).

### 2. MySQL Server 8.x
O sistema gerenciador de banco de dados.
* **Download:** [MySQL Installer para Windows](https://dev.mysql.com/downloads/installer/).
* **Configuração:** Porta padrão `3306`.

### 3. Apache Tomcat 9.x
O servidor de aplicação web para rodar o backend Java.
* **Download:** [Tomcat 9 Software Downloads](https://tomcat.apache.org/download-90.cgi) (Versão "64-bit Windows zip").
* **Nota:** Não utilize o Tomcat 10+ devido à mudança de namespace para `jakarta.*`.

### 4. Node.js (v16 ou v18)
Necessário para gerenciar as dependências do Angular.
* **Download:** [Node.js Official Site](https://nodejs.org/).

### 5. DBeaver Community (Opcional)
Interface visual para gerenciar o banco de dados.
* **Download:** [DBeaver.io](https://dbeaver.io/download/).

---

## ⚙️ Configuração do Ambiente

### Passo 1: Banco de Dados
1. Abra o seu MySQL (via DBeaver ou Terminal).
2. Execute o comando para criar o banco de dados:
   ```sql
   CREATE DATABASE crud_project_db;
   ```

### Passo 2: Backend (IntelliJ IDEA)
1. Importe a pasta do backend como um projeto **Maven**.
2. Aguarde o download das dependências (Hibernate, Wicket, Jasper, etc.).
3. Vá em `Settings > Build, Execution, Deployment > Application Servers`.
4. Adicione o **Tomcat 9** apontando para a pasta onde você o extraiu.
5. Crie uma configuração de "Run" do tipo **Tomcat Server (Local)** e adicione o artefato `.war` na aba Deployment.

### Passo 3: Frontend (Angular)
1. No terminal, acesse a pasta do frontend.
2. Instale as dependências:
   ```bash
   npm install
   ```
3. Inicie o servidor de desenvolvimento:
   ```bash
   ng serve
   ```
4. O frontend estará disponível em `http://localhost:4200`.

---

## 📂 Estrutura do Monorepo

* `/backend-java`: Código fonte Java, configurações do Hibernate e arquivos do Wicket.
* `/frontend-angular`: Projeto Angular 14 com componentes e serviços.
* `/docs`: Documentações adicionais ou scripts SQL de carga inicial.

---

## 📄 Licença

Este projeto é para fins de estudo e desenvolvimento pessoal.

---

### Dicas para adicionar no GitHub:
1. No IntelliJ, clique com o botão direito na pasta raiz do projeto.
2. Escolha **New > File** e nomeie como `README.md`.
3. Cole o conteúdo acima.
4. Use o comando `git add README.md`, depois `git commit -m "docs: adiciona readme com instruções de setup"` e finalize com `git push`.

**Gostou dessa estrutura?** Se você quiser, podemos agora criar o script SQL para a sua primeira tabela de "Produtos" e já colocar esse script dentro de uma pasta no seu GitHub também!