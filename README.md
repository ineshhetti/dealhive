# DealHive MVP

DealHive is a US-focused community bargain sharing platform inspired by OzBargain. The goal is to provide a space where users can discover, share, and vote on deals, fostering a community-driven hub for saving money and finding promotions.

## Project Goals

1. Build a lean MVP with core features (browse, submit, vote, comment, search).
2. Deploy on AWS with low-cost, scalable infrastructure.
3. Ensure simple, intuitive UI optimized for speed and SEO (Next.js).
4. Maintain clear separation of concerns: frontend (Next.js), backend (Spring Boot), database (Postgres).
5. Focus on community trust: moderation tools, abuse prevention, and clear attribution of sources.

## MVP Core Features

- Browse deals anonymously.
- User accounts with email/password authentication.
- Deal submission (title, description, price, store, URL, tags, image).
- Voting (upvote/downvote) with hot ranking.
- Commenting (flat for MVP).
- Search and filtering (by store, category, tags, price).
- Basic moderation (report content, admin hide/ban).
- Responsive UI with accessibility compliance.

## Tech Stack

- **Frontend**: Next.js + TypeScript + Tailwind + shadcn/ui
- **Backend**: Spring Boot 3.x (Java 21)
- **Database**: PostgreSQL 16
- **Cache**: Redis
- **Search**: PostgreSQL full-text (OpenSearch optional later)
- **Storage**: S3 for images, CloudFront CDN
- **Auth**: Cognito (prod), in-app JWT (dev)
- **Infra-as-Code**: Terraform
- **CI/CD**: GitHub Actions → AWS ECS + Amplify/S3

## Development Plan

- Work in vertical slices: Auth → Submit Deal → List → Vote → Comment.
- Deliver end-to-end functionality incrementally.
- Use Docker Compose for local dev.
- Use GitHub Actions for CI/CD with deployments gated on live branch.

## Acceptance Criteria for MVP

- A new user can register, log in, submit a deal, and see it listed.
- Users can upvote/downvote deals; ranking updates accordingly.
- Users can comment and report inappropriate content.
- Admin can hide deals/comments from the feed.
- Search and filtering work for deals.
- Deployed infrastructure on AWS with dev/prod environments.

## Guiding Principles

- **Community first**: prioritize user experience, safety, and transparency.
- **Simplicity**: avoid over-engineering in MVP; iterate later.
- **Compliance**: respect copyright and source rules (no unauthorized scraping).
- **Scalability**: design to handle growth, but start lean.