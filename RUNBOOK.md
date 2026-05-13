# RUNBOOK: Информационный стенд на Docker Compose

## 📋 Общая информация

| Параметр | Значение |
|----------|----------|
| **Сервер** | admin123-VirtualBox |
| **Пользователь** | deployer |
| **Каталог деплоя** | `/home/deployer/deploy/is-stack` |
| **URL приложения** | `http://127.0.0.1:8080` (или `http://<IP>:8080`) |
| **Версия** | 0.1.0-labs |

### Компоненты системы

| Сервис | Контейнер | Порт | Образ |
|--------|-----------|------|-------|
| **Web App** | web_app | 8080→5000 | `ghcr.io/hrs-void/is-lab-app:latest` |
| **SQL Server** | mssql_db | 1433 | `mcr.microsoft.com/mssql/server:2022-latest` |

---

## 1️⃣ Проверка статуса сервисов

### Основная команда
```bash
cd ~/deploy/is-stack
docker compose ps
