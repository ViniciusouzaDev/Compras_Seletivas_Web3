# Sistema de Gerenciamento de Compras Coletivas

Projeto desenvolvido para a disciplina de **Web III** utilizando o framework **Laravel**.  
O objetivo é organizar compras coletivas realizadas por moradores de um grupo, gerenciando pedidos, produtos e pagamentos.

## 📚 Descrição do Projeto

Este sistema permite:

- Cadastro de moradores (`residents`)
- Cadastro de produtos disponíveis (`products`)
- Registro de compras coletivas feitas pelo grupo (`collective_purchases`)
- Associação entre pedidos de moradores e produtos (`orders`)
- Controle de pagamentos por pedido (`payments`)

## 🧱 Estrutura do Banco de Dados

O sistema possui 5 tabelas principais com relacionamentos:

- **residents**: moradores cadastrados
- **products**: produtos comprados em atacado
- **collective_purchases**: compras feitas em grupo
- **orders**: pedidos individuais vinculados às compras coletivas
- **payments**: status e dados de pagamento de cada pedido

Todos os relacionamentos estão definidos nas migrations usando `foreignId()->constrained()->onDelete('cascade')`.  
Os Models possuem os métodos de relacionamento apropriados: `hasOne`, `hasMany`, `belongsTo`, `belongsToMany`.

## 🛠️ Como Executar o Projeto

### 1. Clonar o repositório

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
```

### 2. Subir com Laravel Sail (Docker)

```bash
./vendor/bin/sail up -d
```

### 3. Instalar dependências

```bash
./vendor/bin/sail composer install
```

### 4. Rodar as migrations

```bash
./vendor/bin/sail artisan migrate
```

## 🗺️ Diagrama do Banco de Dados

O diagrama foi enviado separadamente como imagem `.jpg`.

## ✅ Requisitos Atendidos

- [x] Mínimo de 5 tabelas com relacionamentos
- [x] Relacionamentos definidos nas migrations com `foreignId` e `onDelete('cascade')`
- [x] Models com relacionamentos (`hasMany`, `belongsTo`, etc.)
- [x] Uso de `$fillable` e `$casts`
- [x] Código funcionando ao rodar `php artisan migrate`
- [x] Diagrama entregue

## 👥 Desenvolvedores

- Vinicius
- Nara
- Iuri

