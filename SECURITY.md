# Security Guidelines

## Sensitive Data (Never Commit)

The following information must NEVER be pushed to a Git repository:

- API Keys
- Private keys (SSH, RSA, etc.)
- Database credentials (username, password)
- Environment variables (.env files)
- Tokens (OAuth, JWT, access tokens)
- Personal data (emails, phone numbers)
- Configuration files with secrets

## Why This Is Important

Committing sensitive data can lead to:

- Unauthorized access to systems
- Data breaches
- Financial loss
- Account takeover
- Service abuse

## Common Vulnerabilities

- Hardcoded secrets in code
- Public exposure of .env files
- Leaked credentials in commit history
- Misconfigured repositories

## Prevention Best Practices

- Use environment variables
- Add `.env` to `.gitignore`
- Rotate keys regularly
- Use secret management tools
- Review code before pushing