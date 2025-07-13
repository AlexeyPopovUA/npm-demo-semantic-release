# npm-demo-semantic-release

Demo library showcasing **semantic-release** automation for NPM package publishing.

## Features

- ✅ Fully automated version management based on conventional commits
- ✅ Automatic changelog generation
- ✅ Multi-branch support (main, beta, alpha)
- ✅ Feature branch publishing with custom NPM dist-tags
- ✅ Automatic cleanup of feature branch aliases

## Usage

```javascript
import { hello } from 'npm-demo-semantic-release';

console.log(hello('World')); // "Hello, World!"
```

## Commit Message Format

This project follows [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` - New features (minor version bump)
- `fix:` - Bug fixes (patch version bump)
- `feat!:` or `BREAKING CHANGE:` - Breaking changes (major version bump)

## Release Workflow

### Main Branch
Pushes to `main` trigger automatic releases based on commit messages.

### Feature Branches
Pushes to `feature/**` or `feat/**` branches publish pre-release versions with branch-specific NPM tags.

### Pre-release Branches
- `beta` branch: Publishes beta versions
- `alpha` branch: Publishes alpha versions

## Example Scenarios

1. **Feature Release**: `feat: add new greeting function`
2. **Bug Fix**: `fix: handle empty name parameter`
3. **Breaking Change**: `feat!: change function signature`
4. **Feature Branch**: Push to `feature/awesome-feature` → Published as `npm-demo-semantic-release@1.0.0-feature-awesome-feature-1`