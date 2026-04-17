# SECURITY_RULES.md — Security Non-Negotiables
# Read by AI agent before every session. These rules are NEVER violated.
# Also used by Smith the Scrutinizer during security audits.

## Authentication & Authorization
- All protected routes MUST use requireAuth() middleware
- Never expose user data without checking RLS policies first
- Never trust client-side auth checks alone -- always verify server-side
- JWT tokens must be validated on every protected API call
- Admin routes must have separate admin role check beyond auth

## Database
- Never write to the database from client-side code (browser)
- All database access goes through server-side API routes
- Row Level Security (RLS) must be enabled on all Supabase tables
- Never use the service_role key in client-side code
- All schema changes must be backwards-compatible migrations

## API Security
- All API routes must use withErrorHandler() wrapper
- Never return stack traces or internal errors to the client
- Validate and sanitize all user input before processing
- Use parameterized queries -- never string-concatenate SQL
- Rate limit all public endpoints

## Secrets
- Never hardcode API keys, passwords, or secrets in code
- Never commit .env files to the repository
- Use environment variables for all secrets
- NEXT_PUBLIC_ prefix only for values safe to expose to browser

## Code Quality Security
- No console.log in production code (may leak sensitive data)
- No TODO comments referencing security issues in production code
- All dependencies must be from reputable sources

## Audit Triggers (Smith runs these automatically)
- Every 3 features: security audit
- Every schema migration: SQL injection check
- Any auth change: full auth flow review
- Before every merge to main: dependency vulnerability scan

## Smith's Security Checklist (runs before UAT promotion)
[ ] No hardcoded secrets in diff
[ ] All new API routes have auth middleware
[ ] All new DB queries use parameterized inputs
[ ] No new console.log statements
[ ] RLS policies exist for any new tables
[ ] No service_role key used in client-side code
