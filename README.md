# Sistema de Chamados - Como Rodar

## Pré-requisitos

- PHP 8.2+
- Composer 2+
- Node.js 18+
- NPM

## Instalação rápida

1. Clone o repositório:
   ```bash
   git clone <url-do-repositorio>
   cd SistemaDeChamados-PHP-elan
   ```

2. Instale as dependências do Laravel:
   ```bash
   composer install
   ```

3. Crie o arquivo de ambiente:
   ```powershell
   # Windows PowerShell
   copy .env.example .env
   
   # Linux/Mac
   cp .env.example .env
   ```

4. Gere a chave da aplicação:
   ```bash
   php artisan key:generate
   ```

5. Crie o banco de dados SQLite:
   ```powershell
   # Windows PowerShell
   New-Item database\database.sqlite
   
   # Linux/Mac
   touch database/database.sqlite
   ```

6. Execute as migrations e seeders:
   ```bash
   php artisan migrate --seed
   ```

7. Instale as dependências do frontend:
   ```bash
   npm install
   ```

## Rodando o projeto

Em um terminal (backend Laravel):

```bash
php artisan serve
```

Em outro terminal (Vite/frontend):

```bash
npm run dev
```

Acesse: `http://127.0.0.1:8000`

## Credenciais de acesso

O comando `php artisan migrate --seed` já cria automaticamente um usuário administrador.

**Credenciais padrão:**

- Email: `admin@admin.com`
- Senha: `Admin@1234`

## Tecnologias utilizadas

### Backend

- PHP 8.2
- Laravel 12
- Laravel Sanctum
- Laravel Breeze
- Inertia.js (Laravel adapter)
- SQLite (padrão do projeto)

### Frontend

- React 19
- Inertia.js React
- Vite 7
- Tailwind CSS
- Axios
- Recharts

### Qualidade e testes

- PHPUnit 11
- Laravel Pint