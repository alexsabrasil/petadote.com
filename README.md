# PetAdote 🐶🐱

![Status do Projeto](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow)
![Licença](https://img.shields.io/badge/Licença-MIT-green)
![Versão](https://img.shields.io/badge/Versão-1.0.0-blue)

## 📋 Índice

- [Sobre o Projeto](#sobre-o-projeto)
- [Missão e Visão](#missão-e-visão)
- [Funcionalidades](#funcionalidades)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Diagrama de Classes](#diagrama-de-classes)
- [Requisitos](#requisitos)
- [Instalação e Configuração](#instalação-e-configuração)
- [Como Usar](#como-usar)
- [Metodologia Ágil](#metodologia-ágil)
- [Equipe](#equipe)
- [Próximos Passos](#próximos-passos)
- [Licença](#licença)
- [Contato](#contato)

## 📝 Sobre o Projeto

O **PetAdote** é uma plataforma digital desenvolvida para conectar tutores que precisam doar seus pets com pessoas interessadas em adotar, oferecendo um ambiente seguro e responsável para o processo de adoção. O projeto surgiu como resposta a diversos problemas identificados:

- **Superlotação de abrigos**: Abrigos de animais enfrentam dificuldades com o número crescente de pets abandonados.
- **Tutores que não conseguem manter animais**: Situações como filhotes não planejados, mudanças de residência ou viagens prolongadas.
- **Abandono por falta de orientação**: Muitos tutores abandonam seus pets por não conhecerem alternativas.
- **Animais com necessidades especiais**: Pets que ficam deficientes após acidentes ou que precisam de cadeiras de rodas adaptadas.

A plataforma PetAdote oferece:

- Conexão direta entre tutor e adotante
- Orientação e informações práticas para tutores
- Opção de transporte e apoio logístico
- Controle de dados para evitar superlotação de abrigos

## 🎯 Missão e Visão

### Missão (Nosso Propósito Diário)
Conectar pets que precisam de um novo lar a famílias amorosas de forma rápida, segura e responsável, combatendo o abandono animal.

> "Somos o elo de confiança entre quem precisa doar e quem quer adotar."

### Visão (Onde Queremos Chegar)
Ser a plataforma mais conhecida e confiável do Brasil em adoção de animais, onde nenhum pet precise ser abandonado.

> "Queremos ser a primeira escolha de qualquer pessoa que pense em adoção, criando um impacto real no país."

## ⚙️ Funcionalidades

O Product Backlog do PetAdote inclui:

| Funcionalidade | Descrição | Prioridade |
|----------------|-----------|------------|
| Ficha cadastral e técnica do pet | Formulários detalhados para registro de informações dos pets e seus tutores | Alta |
| Facilitador para adoção | Fluxo rápido e seguro para conectar tutores e adotantes interessados | Alta |
| Rede de apoio | Integração entre tutores, veterinários, ONGs e parceiros para suporte completo | Média |
| Conectar pessoas com o mesmo interesse | Funcionalidades de rede social para criar comunidade entre amantes de pets | Baixa |
| Otimizar o tempo | Filtros inteligentes de busca para encontrar o pet ideal com base em preferências | Média |

### Estimativa de Esforço

| Funcionalidade | Pontos | Complexidade |
|----------------|--------|-------------|
| Login com senha | 2 | Baixa |
| Notificação por e-mail | 3 | Média |
| Chat entre usuários | 4 | Alta |

## 🚀 Tecnologias Utilizadas

- **Frontend**: HTML5, CSS3, JavaScript, React
- **Backend**: Node.js, Express
- **Banco de Dados**: MongoDB
- **Autenticação**: JWT, OAuth 2.0
- **Hospedagem**: AWS/Heroku
- **CI/CD**: GitHub Actions
- **Outras ferramentas**: Trello (Kanban), Figma (Design)

## 📁 Estrutura do Projeto

```
petadote/
├── client/                  # Frontend React
│   ├── public/              # Arquivos públicos
│   ├── src/                 # Código fonte React
│   │   ├── components/      # Componentes reutilizáveis
│   │   ├── pages/           # Páginas da aplicação
│   │   ├── services/        # Serviços e APIs
│   │   └── assets/          # Imagens e recursos
│   └── package.json         # Dependências do frontend
├── server/                  # Backend Node.js/Express
│   ├── controllers/         # Controladores da API
│   ├── models/              # Modelos do banco de dados
│   ├── routes/              # Rotas da API
│   ├── middleware/          # Middlewares
│   ├── config/              # Configurações
│   └── package.json         # Dependências do backend
├── docs/                    # Documentação
├── .gitignore               # Arquivos ignorados pelo Git
├── package.json             # Dependências do projeto
└── README.md                # Este arquivo
```

## 📊 Diagrama de Classes

O sistema PetAdote é estruturado com as seguintes classes principais:

- **Pet**: Armazena informações do animal (id, nome, idade, porte, raça, status)
- **Tutor**: Representa o dono atual do pet (id, nome, contato, endereço)
- **Adotante**: Pessoa interessada em adotar (id, nome, contato, preferências)
- **Adoção**: Registra o processo de adoção (id, data, status)
- **Plataforma**: Gerencia todas as entidades do sistema

### Relacionamentos:
- Tutor 1..* → Pet (um tutor pode ter vários pets)
- Adotante 1..* → Adoção (um adotante pode realizar várias adoções)
- Pet 1 → Adoção (um pet está vinculado a uma adoção)
- Plataforma gerencia todas as entidades

## 📋 Requisitos

### Requisitos Funcionais

| ID | Descrição |
|----|-----------|
| RF001 | Cadastro de pets e ficha técnica detalhada com informações sobre saúde, comportamento e necessidades específicas |
| RF002 | Fluxo de adoção seguro com verificação de informações e acompanhamento pós-adoção para garantir o bem-estar do animal |
| RF003 | Rede de apoio e comunidade para conectar tutores, veterinários, ONGs e outros parceiros que possam auxiliar no processo |

### Requisitos Não-Funcionais

| ID | Descrição |
|----|-----------|
| RNF001 | Usabilidade: interface amigável e responsiva, adaptável a diferentes dispositivos e acessível a todos os tipos de usuários |
| RNF002 | Segurança: criptografia de dados, autenticação em duas etapas (2FA), controle de acesso baseado em papéis (RBAC), conformidade com LGPD e PCI DSS, e backups regulares |
| RNF003 | Desempenho: capacidade de suportar muitos acessos simultâneos, com tempo de resposta rápido e escalabilidade para crescimento futuro |

## 🔧 Instalação e Configuração

### Pré-requisitos

- Node.js (v14.x ou superior)
- npm ou yarn
- MongoDB (local ou Atlas)
- Git

### Passos para instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/petadote.git
   cd petadote
   ```

2. Instale as dependências do backend:
   ```bash
   cd server
   npm install
   ```

3. Configure as variáveis de ambiente:
   ```bash
   cp .env.example .env
   # Edite o arquivo .env com suas configurações
   ```

4. Instale as dependências do frontend:
   ```bash
   cd ../client
   npm install
   ```

5. Inicie o servidor de desenvolvimento:
   ```bash
   # No diretório server
   npm run dev
   
   # Em outro terminal, no diretório client
   npm start
   ```

6. Acesse a aplicação em `http://localhost:3000`

## 🖥️ Como Usar

### Para Tutores

1. Crie uma conta na plataforma
2. Cadastre seu pet com informações detalhadas
3. Adicione fotos e descrição do comportamento
4. Aguarde contato de possíveis adotantes
5. Realize o processo de adoção com segurança

### Para Adotantes

1. Crie uma conta na plataforma
2. Utilize os filtros para encontrar pets compatíveis
3. Entre em contato com o tutor
4. Agende uma visita para conhecer o pet
5. Finalize o processo de adoção

## 📈 Metodologia Ágil

O projeto PetAdote utiliza a metodologia Scrum para desenvolvimento, com os seguintes papéis:

- **Product Owner (Adriana)**: Define prioridades e gerencia o backlog do produto
- **Scrum Master (Marília)**: Garante a aplicação da metodologia ágil e remove impedimentos
- **Time de Desenvolvimento (Pedro e Renato)**: Responsáveis por criar as telas e protótipos
- **Teste (Alê)**: Verifica a segurança e experiência do usuário

### Kanban (Trello)

O fluxo de trabalho é organizado em um quadro Kanban com as colunas:
- **A Fazer**: Tarefas planejadas
- **Em Progresso**: Tarefas em andamento
- **Concluído**: Tarefas finalizadas

## 👥 Equipe

- **Adriana** - Product Owner
- **Marília** - Scrum Master
- **Pedro** - Desenvolvedor
- **Renato** - Desenvolvedor
- **Alê** - Tester

## 🔜 Próximos Passos

- Evoluir funcionalidades (rede de apoio, filtros avançados)
- Criar versão protótipo navegável
- Mostrar fluxo completo: quem doa → plataforma → quem adota
- Implementar sistema de avaliação e feedback
- Desenvolver aplicativo móvel

## 📊 Benefícios do Projeto

- **Redução do abandono**: Oferece alternativas seguras para tutores que não podem mais cuidar de seus pets
- **Adoções responsáveis**: Facilita o processo de adoção com informações completas e verificação de compatibilidade
- **Suporte prático e emocional**: Fornece orientação e apoio aos tutores em momentos de decisão difícil
- **Rede de apoio centralizada**: Conecta tutores, adotantes, veterinários e ONGs em uma única plataforma

## 📄 Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE.md](LICENSE.md) para detalhes.

## 📞 Contato

Para mais informações sobre o projeto, entre em contato:

- Email: contato@petadote.com.br
- Website: www.petadote.com.br
- GitHub: [github.com/petadote](https://github.com/petadote.com)

---

Desenvolvido com ❤️ para ajudar pets a encontrarem lares amorosos.
