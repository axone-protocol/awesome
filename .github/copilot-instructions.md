# Copilot Instructions for AXONE Awesome List

## Project Overview

This is a curated "Awesome" list repository for the AXONE blockchain protocol ecosystem. It maintains a comprehensive directory of community-contributed resources including node operators, explorers, APIs, tools, and services. The project emphasizes automation, quality control, and community collaboration.

## Key Architecture

### Automated Status Monitoring

- **Status Badge System**: The core feature automatically checks service availability and updates status badges (✅/❌) in README tables
- **Link Checker**: `.github/scripts/markdown-table-link-check.js` validates all URLs in tables, with special handling for gRPC endpoints and large files (snapshots)
- **Daily Automation**: GitHub Actions run status checks on schedule and auto-commit updates

### Content Structure

The README.md follows a strict tabular format organized by service categories:

- **Networks**: Mainnet and testnet information with dynamic height badges
- **Documentation/Guides**: Community-contributed setup guides
- **Block Explorers**: Various blockchain explorers with status tracking
- **Services**: RPC, API, gRPC endpoints organized by provider
- **Applications**: Wallet integrations and third-party tools

## Development Workflows

### Contributing New Resources - Fork → Add → PR

The contribution process follows a strict community-driven workflow:

1. **Fork the repository** to your GitHub account
2. **Create a feature branch** following naming conventions:
   - `feat/add-new-service` - For adding new services/resources
   - `docs/update-guide` - For documentation improvements
   - `fix/correct-url` - For fixing broken links or data
   - Branch patterns enforced: `feat|fix|build|ci|docs|style|refactor|perf|test|chore`
3. **Edit README.md directly** - this is the single source of truth
4. **Follow table format exactly**:
   - Add new entries to appropriate service category (RPC, API, Explorer, etc.)
   - **Add new resources at the end of tables** - follows chronological contribution order
   - Include "Thanks To" provider name with link when possible
   - Set initial Status to ✅ (automation will validate and update)
   - Ensure proper markdown table alignment
5. **Submit Pull Request** with descriptive title and description
6. **Automated validation runs**:
   - Branch name validation (enforced, PR will be closed if non-compliant)
   - Markdown linting checks
   - YAML linting for any workflow changes
   - Link validation (runs after merge)

### PR Review Process

- **Community-driven curation**: Focus on editorial quality and resource value
- **CodeRabbit integration**: Automated reviews with "chill" profile for constructive feedback
- **Manual review**: Maintainers ensure alignment with awesome list standards
- **Maintainer approval required**: No auto-merge - maintainers must approve all PRs
- **Squash and merge**: Community contributions are systematically squashed and merged to maintain clean history

### Quality Control Pipeline

- **Markdown Linting**: `.markdownlint.yaml` with relaxed rules for this content type
- **YAML Linting**: `.yamllint.yaml` for workflow files
- **Commit Linting**: Conventional commits enforced via commitlint
- **Branch Naming**: Enforced via GitHub Actions for PRs

### Automation Scripts

Key script: `.github/scripts/markdown-table-link-check.js`

- Parses markdown tables to extract URLs
- Skips gRPC endpoints (can't validate with HTTP)
- Uses custom timeouts for large files (snapshots)
- Updates status symbols automatically
- Handles edge cases for different service types

## Project-Specific Conventions

### Service Provider Format

Each service entry includes:

- **Thanks To**: Provider name with optional link
- **URL**: Service endpoint
- **Status**: ✅ (alive) or ❌ (dead) - auto-updated

### Network Information

- Dynamic badges show current block height via API calls
- Badge format: `![network-name](https://img.shields.io/badge/dynamic/json...)`
- Separate entries for mainnet (`axone-1`) and testnet (`axone-dentrite-1`)

### Asset Management

- Icons stored in `/assets/` as WebP format
- Inline styling used for consistent icon sizing (15px)
- Icons reference social platforms, not technical services

## Integration Points

### GitHub Actions Dependencies

- **Link Checking**: Uses `link-check` npm package with custom configuration
- **Markdown Processing**: Custom parser in `helper/index.js` handles table extraction

### External APIs

- Blockchain height badges pull from various API endpoints
- Status checking validates HTTP/HTTPS endpoints only
- Special handling for snapshot files (large downloads)

## Critical Files

- `README.md`: Single source of truth for all content
- `.github/scripts/markdown-table-link-check.js`: Core automation logic
- `.github/workflows/update-service-status-badges.yml`: Status update automation
- `.markdownlint.yaml`: Content quality rules

## Common Patterns

- **Direct README editing**: All contributions modify README.md directly - no separate documentation files
- **Chronological table ordering**: New resources are added at the end of tables, preserving contribution order
- **Automated status validation**: All URLs in tables get automatic status validation
- **Provider attribution**: Provider names should link to their main service page when possible
- **Consistent table structure**: New categories follow the established table structure with consistent column headers
- **Community curation**: Community-driven content with maintainer oversight for quality
- **Fork-first workflow**: No direct commits to main - all changes via fork → branch → PR
- **Branch naming enforcement**: PRs with non-compliant branch names are automatically closed
- **Status badge automation**: Never manually change ✅/❌ symbols - let automation handle updates
