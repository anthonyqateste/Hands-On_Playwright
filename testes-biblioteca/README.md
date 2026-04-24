# Testes de API com Playwright

Este projeto contém um conjunto de testes automatizados de API desenvolvidos com **Playwright**, focados na validação das rotas principais do serviço de gestão de livros.  
Os testes verificam cenários reais, como obter listas, criar novos registos, atualizar dados, remover itens e validar mensagens de erro.

----------

## 📦 1. Pré‑requisitos

Antes de executar os testes, certifica‑te de que tens instalado:

- **Node.js** (versão 18 ou superior)
- **npm** (incluído com o Node)
- **Playwright** (instalado através do projeto)

Para confirmar:
node -v

----------

📥 2. Instalar dependências
Na raiz do projeto, executa: npm install

Isto instala o Playwright e todas as bibliotecas necessárias.

----------

🧪 3. Como correr apenas os testes de API
Os testes de API estão organizados na pasta: testes-biblioteca/tests/api

Se quiseres correr um ficheiro específico: npx playwright test testes-biblioteca/tests/api/nome-do-teste.spec.js

----------

🧱 4. O que estes testes validam
Os testes cobrem vários cenários importantes, incluindo:

- Obter a lista completa de livros (GET /livros)
- Obter um livro por ID
- Criar um novo livro (POST)
- Atualizar um livro existente (PUT)
- Remover um livro (DELETE)
- Validar respostas de erro quando:
      o ID não existe
      o payload é inválido
      campos obrigatórios estão em falta

Cada teste segue uma estrutura simples:

1. Enviar o pedido HTTP com request.get(), request.post(), etc.
2. Validar o código de estado (ex.: expect(response.status()).toBe(200))
3. Ler o JSON da resposta
4. Confirmar que os dados estão corretos

----------

▶️ 5. Ver o relatório dos testes
Depois de executar os testes, podes abrir o relatório HTML com: npx playwright show-report

Isto permite ver:

- Testes que passaram
- Testes que falharam
- Detalhes de cada pedido e resposta

----------

📚 6. Sobre este projeto
Este conjunto de testes foi criado para fins de aprendizagem e prática de automação de APIs com Playwright.
O objetivo é garantir que cada endpoint funciona corretamente e que os cenários principais estão cobertos de forma simples e clara.
