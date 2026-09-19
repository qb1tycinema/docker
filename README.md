# Infrastructure Environment Configuration

To run the infrastructure services successfully via Docker Compose, you must create an `.env` file in the root directory. This file stores the credentials needed for PostgreSQL, Redis, and RabbitMQ. 

> **⚠️ Security Warning:** 
> Never commit the actual `.env` file to version control. It is already added to `.gitignore`.

## Example `.env` Structure

Create a file named `.env` and populate it with your own secure values:

```env
# Postgres
POSTGRES_USER="your_database_user"
POSTGRES_PASSWORD="your_secure_password"

# Redis
REDIS_PASSWORD="your_redis_password"

# Rabbitmq
RABBITMQ_DEFAULT_USER="your_rabbitmq_user"
RABBITMQ_DEFAULT_PASS="your_rabbitmq_password"
```

## Variable Descriptions

### PostgreSQL
* **`POSTGRES_USER`**: The default username for the database superuser (e.g., `postgres` or `admin`).
* **`POSTGRES_PASSWORD`**: A strong password used to secure the database.

### Redis
* **`REDIS_PASSWORD`**: The password required for clients and other services to authenticate with the Redis instance.

### RabbitMQ
* **`RABBITMQ_DEFAULT_USER`**: The administrator username used for the RabbitMQ management dashboard and for microservices to establish connections.
* **`RABBITMQ_DEFAULT_PASS`**: The password for the RabbitMQ administrator account.