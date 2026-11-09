# Module 04: Docker & Containerization

## 1. Architecture Overview
- **Application:** Node.js Express portfolio.
- **Containerization:** Docker multi-stage build for a minimal production image.
- **Orchestration:** Docker Compose for single-service deployment.
- **Networking:** Port 8080 exposed to the host.

## 2. Dockerfile Optimization
- Multi-stage build to exclude build dependencies.
- `node:20-alpine` base image for a small footprint.
- Non-root `USER node` for security.
- Layer caching for `package.json` before copying the rest of the code.

## 3. Deployment Steps
1. Created a `.dockerignore` to exclude `node_modules` and `.git`.
2. Built the image manually: `sudo docker build -t my-portfolio .`
3. Ran the container manually: `sudo docker run -d -p 8080:8080 --name my-app my-portfolio`
4. Verified the app at `http://localhost:8080`.
5. Tested Docker Compose by running: `sudo docker compose up -d --build`

## 4. Proof of Work
<img width="2286" height="1113" alt="Screenshot From 2026-11-08 18-28-56" src="https://github.com/user-attachments/assets/ff5a46e1-85ae-4045-8661-8c3d5464fd2f" />
<img width="1681" height="147" alt="Screenshot From 2026-11-08 18-29-28" src="https://github.com/user-attachments/assets/0e1be8b4-18f0-49e5-9905-4ea2e17c0b62" />
<img width="1920" height="180" alt="Screenshot From 2026-11-08 18-29-40" src="https://github.com/user-attachments/assets/13078b3e-9c5f-4502-97d9-1b242905d869" />
<img width="1908" height="1042" alt="Screenshot From 2026-11-08 18-32-04" src="https://github.com/user-attachments/assets/f5d95e25-a728-4b67-93ca-8394fae51be9" />
<img width="1917" height="384" alt="Screenshot From 2026-11-08 18-40-04" src="https://github.com/user-attachments/assets/8b31f843-5515-4018-b524-ed7c3e44b2d5" />
