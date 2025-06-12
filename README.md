# Task Manager API

A simple Laravel-based RESTful API for managing tasks with user authentication.

## Features

- User registration and login (API token-based authentication using Laravel Sanctum)
- CRUD operations for tasks
- Each user can manage their own tasks

## Setup

### Using Git

1. **Clone the repository from GitHub**
   ```
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. **Install dependencies**  
   ```
   composer install
   ```

3. **Copy and configure environment file**  
   ```
   cp .env.example .env
   ```
   Update database and other settings in `.env`.

4. **Generate application key**  
   ```
   php artisan key:generate
   ```

5. **Run migrations**  
   ```
   php artisan migrate
   ```

6. **Install Sanctum**  
   ```
   php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
   ```

## Running the API

Start the development server:
```
php artisan serve
```

## API Endpoints

- `POST /api/register` — Register a new user
- `POST /api/login` — Login and receive an API token
- `POST /api/logout` — Logout (requires authentication)
- `GET /api/tasks` — List tasks (requires authentication)
- `POST /api/tasks` — Create a task (requires authentication)
- `GET /api/tasks/{id}` — View a task (requires authentication)
- `PUT /api/tasks/{id}` — Update a task (requires authentication)
- `DELETE /api/tasks/{id}` — Delete a task (requires authentication)

## Postman Collection

A ready-to-import Postman collection is provided in [`TaskManagerAPI.postman_collection.json`](./TaskManagerAPI.postman_collection.json):

1. Open Postman.
2. Click "Import" and select the `TaskManagerAPI.postman_collection.json` file.
3. Use the requests to interact with your API.

## License

MIT
