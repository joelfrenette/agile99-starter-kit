# DESIGN.md — Living Design Document
# The Architect maintains this. Updated at end of every DESIGN and BUILD session.
# Read this before writing any code. Design decisions made here are law.

## Architecture Overview
[The Architect fills this in during the DESIGN phase]

## Tech Stack
Frontend:  [e.g. Next.js App Router, TypeScript, Tailwind, shadcn/ui]
Backend:   [e.g. Next.js API routes, Supabase Edge Functions]
Database:  [e.g. Supabase PostgreSQL with Row Level Security]
Auth:      [e.g. Supabase Auth, OAuth providers]
Deploy:    [e.g. Vercel -- dev branch = staging, main = production]
Storage:   [e.g. Supabase Storage]

## Database Schema
[The Architect documents tables, columns, relationships, and RLS policies here]

## API Routes
[The Architect documents all API routes with method, path, auth, request/response]

## Component Architecture
[The Architect documents key components, their props, and data flow]

## Environment Variables Required
[List all env vars needed -- never actual values, just the key names]

## Architecture Decision Records (ADRs)
[The Architect logs every significant decision with rationale and tradeoffs]

### ADR-001: [Decision Title]
Date: [DATE]
Status: Accepted
Decision: [what was decided]
Rationale: [why this was chosen over alternatives]
Tradeoffs: [what we gave up to get this]

## Security Boundaries
[Document what is public vs authenticated vs admin-only]

## Performance Constraints
[Document any known performance requirements or bottlenecks]

## Third-Party Dependencies
[List all external APIs, libraries, and services with purpose]
