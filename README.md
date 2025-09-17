# Users API Automation

Este repositório contém testes automatizados para a API de usuários do [Serverest](https://serverest.dev/).

## 🚀 Objetivo
Demonstrar habilidades de automação de testes de API, incluindo:

- Criação de collection no Postman
- Uso de variáveis de ambiente (`token`, `userId`, `baseUrl`)
- Testes de endpoints CRUD de usuários
- Integração com Newman para execução em CLI
- Geração de relatórios HTML detalhados
- CI/CD com GitHub Actions para execução automática

## 🧪 Testes incluídos
1. Login (POST) → gera token
2. ListaUsuarios (GET)
3. CriaUsuarios (POST) → gera userId
4. BuscaUsuariosId (GET)
5. AtualizaUsuarios (PUT)
6. DeletaUsuarioId (DELETE)

## ⚙️ Como rodar localmente
```bash
npm install -g newman newman-reporter-htmlextra
newman run "Users API Tests.postman_collection.json" \
  -e "baseUrl.postman_environment.json" \
  -r cli,htmlextra \
  --reporter-htmlextra-export reports/index.html
