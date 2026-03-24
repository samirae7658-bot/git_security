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
## Environment Variables Best Practices

- Store sensitive data in `.env` files
- Never commit `.env` files to Git
- Always add `.env` to `.gitignore`
- Use different `.env` files for development and production
- Rotate keys regularly
- Use secure secret management tools when possible

### Example

.env file:
API_KEY=your_api_key_here
DB_PASSWORD=your_password

In code (Python example):
import os
api_key = os.getenv("API_KEY")