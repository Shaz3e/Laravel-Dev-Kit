# Laravel Dev Kit

![Code Quality Checks](https://github.com/Shaz3e/Laravel-Dev-Kit/actions/workflows/code-quality.yml/badge.svg)
![Duster Fix](https://github.com/Shaz3e/Laravel-Dev-Kit/actions/workflows/duster-fix-blame.yml/badge.svg)
![Duster Lint & Fix](https://github.com/Shaz3e/Laravel-Dev-Kit/actions/workflows/duster.yml/badge.svg)
![Laravel Pint Code Style](https://github.com/Shaz3e/Laravel-Dev-Kit/actions/workflows/pint.yml/badge.svg)
![Prettier Code Formatting](https://github.com/Shaz3e/Laravel-Dev-Kit/actions/workflows/prettier.yml/badge.svg)

Laravel Dev Kit is a starter kit for Laravel applications, designed to save time and set up your projects with a standardized environment. It includes pre-configured tools for code linting, formatting, and CI/CD workflows, ensuring code quality and consistency.

---

## Features

- **CI/CD Workflows**: Pre-configured GitHub Actions workflows for:

    - PHP linting
    - Fixing common coding issues
    - Prettier integration
    - Automated testing with Laravel

- **Husky Pre-Commit Hooks**: Automatically run linting and formatting tasks before committing changes.

- **Linting and Formatting**:

    - `Pint` for PHP code formatting
    - Prettier for JavaScript, CSS, and other frontend assets

- **Custom Configuration Files**:
    - `.prettierrc` and `.prettierignore` for Prettier
    - `lint-staged.config.js` for staged file linting

---

## File Structure

```plaintext
/
|-- .gitHub
|   |-- workflows
|   |   |-- auto-merge-dependabot.yml
|   |   |-- code-quality.yml.yml
|   |   |-- duster-fix-blame.yml
|   |   |-- duster.yml
|   |   |-- pint.yml
|   |   |-- prettier.yml
|
|-- .husky
|   |-- _
|   |   |-- .gitignore
|   |   |-- husky.sh
|   |-- pre-commit
|   |-- pre-push
|
|-- .prettierrc
|-- .prettierignore
|-- lint-staged.config.js
```

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (for frontend tooling)
- [Composer](https://getcomposer.org/) (for PHP dependencies)
- A fresh [Laravel](https://laravel.com) application

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/shaz3e/laravel-dev-kit.git my-new-app
    cd my-new-app
    ```

2. Install PHP dependencies:

    ```bash
    composer install
    ```

3. Install Node.js dependencies:

    ```bash
    npm install
    ```

4. Copy `.env.example` to `.env` for your Laravel application.

5. Generate Key
    ```bash
    php artisan key:generate
    ```

### Usage

1. Run the local development server:

    ```bash
    php artisan serve
    ```

2. Watch and build frontend assets:

    ```bash
    npm run dev
    ```

3. Commit code with pre-commit checks automatically applied.

---

## Workflows

### GitHub Actions

The `.github/workflows` folder includes:

- **code-quality.yml**: Automatically fix coding standards and blame-ignore files.
- **laravel.yml**: Run tests and ensure application stability.
- **lint.yml**: Run PHP, CSS, and JS lint checks.
- **prettier-write.yml**: Enforce Prettier standards across supported files.

### Husky Hooks

Automatically lint and format files before committing changes. Customize the hook behavior in `.husky/pre-commit`.

---

## Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue for discussion.

---

## License

This repository is open-source and available under the [MIT License](LICENSE).

---

## Acknowledgments

Laravel Dev Kit simplifies the setup process for Laravel applications, integrating essential developer tools to streamline workflows and maintain code quality.

## Credit

This project utilizes and integrates various tools and resources to provide an optimized development experience. Special thanks to:

- Laravel: For providing a robust PHP framework.
- Pint: Laravel's official code formatter for PHP.
- Prettier: An opinionated code formatter for JavaScript, CSS, and more.
- Husky: For Git hooks management to automate checks and ensure quality.
- Lint-Staged: For running linters against staged Git files.
- GitHub Actions: For seamless CI/CD workflows.

We acknowledge these open-source tools, frameworks, and the global development community for their contributions.

If you'd like to be recognized as a contributor to this repository, feel free to submit a pull request or raise an issue with solution.
