# Contributing to GitHub Slideshow

Thank you for your interest in contributing to GitHub Slideshow! We welcome contributions from the community.

## How to Contribute

### Reporting Issues

Before creating an issue, please check if a similar issue already exists. When reporting issues, please include:

- A clear and descriptive title
- A detailed description of the issue
- Steps to reproduce the problem
- Expected behavior vs actual behavior
- Screenshots if applicable
- Your environment details (browser, OS, etc.)

### Suggesting Enhancements

We welcome feature requests! Please use the feature request issue template and provide:

- A clear description of the enhancement
- Use cases and benefits
- Any implementation ideas you may have

### Pull Requests

1. Fork the repository
2. Create a new branch from `master` for your changes
3. Make your changes following our coding standards
4. Test your changes thoroughly
5. Commit your changes with clear, descriptive commit messages
6. Push your branch to your fork
7. Open a pull request with a clear description of your changes

#### Pull Request Guidelines

- Fill out the pull request template completely
- Reference any related issues
- Include tests if applicable
- Update documentation as needed
- Keep pull requests focused on a single concern
- Follow the existing code style and conventions

### Development Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/iwantaljaard/github-slideshow.git
   cd github-slideshow
   ```

2. Install dependencies:
   ```bash
   script/setup
   ```

3. Run the local development server:
   ```bash
   script/server
   ```

4. Build and test:
   ```bash
   script/cibuild
   ```

### Code Style

- Follow the existing code style in the project
- Use meaningful variable and function names
- Comment complex logic
- Keep functions focused and concise

### Testing

- Write tests for new features
- Ensure all tests pass before submitting a pull request
- Run `script/cibuild` to verify your changes

### Commit Messages

- Use clear and meaningful commit messages
- Start with a verb in the present tense (e.g., "Add", "Fix", "Update")
- Keep the first line under 50 characters
- Provide additional context in the body if needed

## Getting Help

If you need help or have questions:

- Check the [README](README.md) for basic information
- Review existing issues and pull requests
- Open a new issue with the question label

## Code of Conduct

This project adheres to a Code of Conduct. By participating, you are expected to uphold this code. Please report unacceptable behavior to the project maintainers.

Thank you for contributing!
