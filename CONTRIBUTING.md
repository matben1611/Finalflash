# Contributing

Thank you for your interest in contributing to this project!

## Getting Started

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Write or update tests as needed
5. Run tests: `Invoke-Pester -Path ./tests -PassThru`
6. Run code analysis: `Invoke-ScriptAnalyzer -Path ./scripts -Recurse`
7. Commit with descriptive messages (`git commit -am 'Add feature...'`)
8. Push to your fork
9. Create a Pull Request

## Code Standards

- Follow PowerShell best practices
- Use explicit parameter names in function definitions
- Add comment-based help for functions
- Ensure all tests pass before submitting PR
- Use proper error handling with try/catch blocks
- Follow the existing code style and formatting

## Commit Messages

Use conventional commits:
- `feat:` for new features
- `fix:` for bug fixes
- `docs:` for documentation
- `test:` for test changes
- `ci:` for CI/CD changes
- `refactor:` for code refactoring

Example: `feat: add new BIOS recommendation category`

## Testing

- Add tests for new functionality in `/tests`
- Tests use Pester 5.x framework
- All tests must pass: `Invoke-Pester -Path ./tests -PassThru`
- Test file naming convention: `scriptname.tests.ps1`

## Questions?

Feel free to open an issue to discuss improvements or ask questions.
