# <img alt=logo src=candiddev.png width=40px> Candid Development

> Feedback driven development

[![Integration](https://github.com/candiddev/.github/actions/workflows/integration.yaml/badge.svg?branch=main)](https://github.com/candiddev/.github/actions/workflows/integration.yaml)

## License

The code in this repository is unlicensed.  It's our website, why would you want this?

## Development

Our development process is mostly trunk-based with a `main` branch that folks can contribute to using pull requests.  We tag releases as necessary using CalVer.

### Repository Layout

- `./github:` Reusable GitHub Actions
- `./hugo:` Candid Development website
- `./shell:` Development tooling
- `./shared:` Shared libraries from https://github.com/candiddev/shared

Make sure you initialize the shared submodule:

```bash
git submodule update --init
```

### CI/CD

We use GitHub Actions to lint, test, build, release, and deploy the code.  You can view the pipelines in the `.github/workflows` directory.  You should be able to run most workflows locally and validate your code before opening a pull request.

### Tooling

Visit [shared/README.md](shared/README.md) for more information.
