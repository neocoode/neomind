# NeoMind

NeoMind é um projeto modular que combina **inteligência artificial** com micro serviços, proporcionando uma arquitetura escalável para interações avançadas com usuários, análise de dados e gerenciamento de autenticação. Utiliza o modelo LLaMA para processamento de linguagem natural e outras tecnologias modernas.

---

## **Estrutura do Projeto**

```
NeoMind/
├── frontend/                 # Aplicação Frontend em Next.js
├── services/                 # Micro serviços para funcionalidades específicas
│   ├── cortex/               # Backend para IA e treinamento do modelo
│   ├── communicator/         # Intermediário entre serviços e o Cortex
│   ├── authenticator/        # Serviço para autenticação e gerenciamento de usuários
│   └── analytics/            # Serviço para análises e geração de relatórios
├── data/                     # Dados de treinamento
├── docs/                     # Documentação técnica
├── scripts/                  # Scripts de automação e deploy
└── docker-compose.yml        # Orquestração de containers
```

---

## **Principais Funcionalidades**

### **Frontend**
- Desenvolvido em **Next.js**.
- Fornece uma interface interativa para o usuário final interagir com o sistema.
- Comunicação com os serviços via API REST.

### **Micro Serviços**
- **Cortex**:
  - Processamento de mensagens usando o modelo LLaMA.
  - Treinamento incremental do modelo com novos dados.
- **Communicator**:
  - Roteia solicitações entre os serviços, garantindo escalabilidade e controle centralizado.
- **Authenticator**:
  - Gerencia autenticação (login, registro) e permissões de usuários.
- **Analytics**:
  - Coleta e analisa dados para monitoramento de performance e relatórios.

---

## **Tecnologias Utilizadas**

- **Frontend**: 
  - Next.js (React), Axios para comunicação com APIs.
- **Backend (Micro Serviços)**:
  - Python (Flask, Transformers) para o Cortex e Analytics.
  - Node.js (Express) para Authenticator e Communicator.
- **Orquestração**:
  - Docker e Docker Compose.
- **Dados e Treinamento**:
  - Hugging Face Transformers, PEFT (LoRA).

---

## **Como Executar**

### **Pré-requisitos**
- **Node.js** (para frontend e serviços baseados em Node.js).
- **Python** e **pip** (para serviços baseados em Python).
- **Docker** e **Docker Compose** (para orquestração).

### **Passos**
1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/neomind.git
   cd neomind
   ```

2. Configure as dependências:
   - **Frontend**:
     ```bash
     cd frontend
     npm install
     ```
   - **Serviços em Python**:
     ```bash
     cd services/cortex
     pip install -r requirements.txt
     ```

3. Execute os serviços com Docker Compose:
   ```bash
   docker-compose up
   ```

4. Acesse o frontend em:
   ```
   http://localhost:3000
   ```

---

## **Próximos Passos**

- Implementar novos endpoints no Communicator.
- Adicionar dashboards no Analytics para visualização de dados em tempo real.
- Otimizar o treinamento do modelo no Cortex.

---

## **Contribuição**

Contribuições são bem-vindas! Para contribuir:
1. Crie um fork do repositório.
2. Crie uma branch para sua funcionalidade:
   ```bash
   git checkout -b feature/nova-funcionalidade
   ```
3. Faça um pull request.

---

## **Licença**

Este projeto está sob a licença [MIT](LICENSE).