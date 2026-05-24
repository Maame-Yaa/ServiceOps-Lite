# ServiceOps Lite

ServiceOps Lite is a lightweight tool for service businesses to capture leads and manage early-stage communication in a structured way.

## Why it exists

Many businesses lose leads because inquiries are scattered across social media DMs, forms, and random notes. ServiceOps Lite provides a simple intake and inquiry workflow with admin visibility and status tracking so nothing falls through the cracks.

## MVP features

- Client intake form with admin list and detail views
- Inquiry form with admin list and detail views
- Status tracking and internal notes
- Search and filtering
- Basic admin authentication

## Architecture overview

- Next.js frontend (public pages + admin UI)
- Node.js REST API backend
- PostgreSQL database
- `infra/` reserved for AWS CDK (deployment later)

## Tech stack

- Next.js, TypeScript, Tailwind CSS
- Node.js, NestJS
- PostgreSQL, Prisma
- AWS (planned): S3 + CloudFront, ECS, RDS, Secrets Manager, CloudWatch

## Local development

### Prerequisites
- Node.js installed
- Docker installed

### Run the database (PostgreSQL)

```bash
# from repo root
docker compose up -d
```

### Run the backend API

```bash
# from repo root
cd backend
npm run start:dev
```

### Run the frontend

```bash
# from repo root
cd frontend
npm run dev
```

- Frontend: `http://localhost:3000`
- Backend: `http://localhost:3001`


## Out of scope

This project intentionally does not include booking, payments, client portals, multi-tenant support, or marketing automation.
