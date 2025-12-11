# PHP coding standard

This repository contains rules for coding standard for PHP projects.
  
## Usage
Create `.phpcs.xml` file in your project and extend `base.phpcs.xml`. Base configuration contains base rules which can be extended in your project.

## Development

Run Composer in Docker (no local PHP/Composer needed):

```sh
docker run --rm -it \
  -u "$(id -u):$(id -g)" \
  -v "$PWD":/app \
  -w /app \
  composer:2 update
```

Notes:
- For local development only; in CI/CD prefer reproducible installs (composer install) rather than updates.
- If your local PHP version differs from the target platform, you may temporarily use `--ignore-platform-reqs`, but avoid committing such changes without verifying compatibility.
