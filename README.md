## 👋 Welcome to code-server 🚀

VS Code in the browser - run Visual Studio Code on any machine

## 📋 Description

VS Code in the browser - run Visual Studio Code on any machine

## 🚀 Services

- **app**: lscr.io/linuxserver/code-server:latest

## 📦 Installation

### Option 1: Quick Install
```bash
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/code-server/main/docker-compose.yaml" -o compose.yml
```

### Option 2: Git Clone
```bash
git clone "https://github.com/composemgr/code-server" ~/.local/srv/docker/code-server
cd ~/.local/srv/docker/code-server
docker compose up -d
```

### Option 3: Using composemgr
```bash
composemgr install code-server
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
SERVICE_USER=1000
SERVICE_GROUP=1000
APP_USER_PASS=changeme_user_password
APP_ADMIN_PASS=changeme_admin_password
```

See `docker-compose.yaml` for complete list of configurable options.

## 🌐 Access

- **Web Interface**: http://172.17.0.1:8080

## 📂 Volumes

- `./volumes/config/ssh` - Data storage
- `./volumes/config/gnupg` - Data storage
- `./volumes/data/workspace` - Data storage
- `./volumes/data/code-server` - Data storage
- `./volumes/config/code-server` - Data storage

## 🔐 Security

- Change all default passwords before deploying to production
- Use strong secrets for all authentication tokens
- Configure HTTPS using a reverse proxy (nginx, traefik, caddy)
- Regularly update Docker images for security patches
- Backup your data regularly

## 🔍 Logging

```shell
docker compose logs -f app
```

## 🛠️ Management

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# Update to latest images
docker compose pull && docker compose up -d

# View logs
docker compose logs -f

# Restart services
docker compose restart
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
