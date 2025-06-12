# 🐳 Configuração de Ambiente de Desenvolvimento com Docker e WSL2 no Windows  
# 🐳 Development Environment Setup with Docker and WSL2 on Windows

Este repositório documenta a configuração de um ambiente de desenvolvimento isolado e performático no Windows, utilizando **Docker Desktop** com suporte a **WSL2 (Windows Subsystem for Linux 2)**.

This repository documents the setup of a performant and isolated development environment on Windows, using **Docker Desktop** with **WSL2 (Windows Subsystem for Linux 2)** support.

---

## 💡 Objetivo / Purpose

**PT-BR:** Criar um ambiente que permita executar aplicações conteinerizadas (como o **n8n**) de forma estável, portátil e segura no Windows, com suporte à virtualização via WSL2.  
**EN:** To create an environment that allows containerized applications (like **n8n**) to run in a stable, portable, and secure way on Windows, using WSL2 virtualization support.

---

## ⚙️ Desafios e Solução / Challenges and Solution

### 🔧 Desafios enfrentados / Challenges Faced

- Ativação da virtualização (VT-x) na BIOS do Dell Inspiron 15 3520.  
- Conflitos com a Plataforma de Máquina Virtual do Windows.  
- Instalação e atualização do WSL2.  
- Configuração do Docker Desktop com backend WSL2.  

---

### ✅ Solução aplicada / Solution Applied

- Enable and verify **Intel VT-x** in BIOS.  
- Fix conflicts with **Windows Virtual Machine Platform**.  
- Install and configure **WSL2** (Ubuntu).  
- Setup **Docker Desktop** to use WSL2 backend.  
- Create a persistent **n8n** environment using `docker-compose`.

---

## 🧠 Habilidades Demonstradas / Skills Demonstrated

- 🖥️ Virtualização / Hardware Virtualization  
- 🐧 WSL2: Instalação, depuração e uso como backend  
- 🐋 Docker e Docker Compose  
- 💾 Volumes persistentes para dados sensíveis  
- 🔐 Variáveis de ambiente e mapeamento de portas  
- 🧩 Automação com **n8n**  
- 🛠️ Resolução de problemas e conflitos entre camadas de virtualização  

---

## 🚀 Exemplo: n8n com Docker Compose  
## 🚀 Example: n8n with Docker Compose

Configuração do n8n como ambiente Low-Code de automação de tarefas.

Setting up n8n as a Low-Code automation platform using Docker Compose.

### 📂 Estrutura / Folder Structure

/
├── data/ # Volume persistente / Persistent volume
├── .env # Variáveis de ambiente / Environment variables
└── docker-compose.yml # Definição dos serviços / Service definitions



---

## 📦 Como usar / How to Use

### Pré-requisitos / Prerequisites

- WSL2 instalado (Ubuntu recomendado)  
- Docker Desktop instalado e configurado com WSL2  
- Git e terminal configurado (CMD/PowerShell/Bash)

---

### 1. Clone o repositório / Clone the repository

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio


2. Edite o arquivo .env / Edit the .env file
env
Copiar
Editar
N8N_HOST=localhost
N8N_PORT=5678

3. Inicie o ambiente / Start the environment
bash
Copiar
Editar
docker-compose up -d
Acesse: http://localhost:5678

4. Pare o ambiente / Stop the environment
bash
Copiar
Editar
docker-compose down
🔄 Backup & Restauração / Backup & Restore (em breve / coming soon)
📚 Referências / References
WSL2 Documentation

Docker Desktop + WSL2

n8n Documentation

📌 Autor / Author
Edson Correa
https://edcorrea.tech/
