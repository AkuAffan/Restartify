# Contributing

Thanks for contributing to Restartify.

## Prerequisites
- Java 8+
- Maven (or use bundled Maven in this repo)

## Local Build
```powershell
cd plugins
.\apache-maven-3.9.6\bin\mvn.cmd -q clean package
```

## Development Guidelines
- Keep behavior backward compatible when possible.
- Add config defaults for every new feature.
- Avoid breaking command syntax.
- Update:
  - `plugin.yml` (if command/metadata changed)
  - `config.yml` / `messages.yml` / `permissions.yml`
  - changelog and release notes

## Pull Request Checklist
- [ ] Plugin builds successfully.
- [ ] New commands are documented.
- [ ] New config keys have safe defaults.
- [ ] Release notes/changelog updated.
