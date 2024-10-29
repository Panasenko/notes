<!-- markdownlint-disable MD022 MD032 MD013 -->
markdown_linter
===============
- Category: nmap/linter
- Tags: markdown, linter
- Created: 2024-10-29T17:26:34+02:00

Configuration
=============

Text passed to markdownlint is parsed as Markdown, analyzed, and any issues reported. Two kinds of text are ignored by most rules:

- HTML comments
- Front matter (see `options.frontMatter` below)

Rules can be enabled, disabled, and configured via `options.config` (described below) to define the expected behavior for a set of inputs. To enable or disable rules at a particular location within a file, add one of these markers to the appropriate place (HTML comments don't appear in the final markup):

- Disable all rules: `<!-- markdownlint-disable -->`
- Enable all rules: `<!-- markdownlint-enable -->`
- Disable all rules for the current line: `<!-- markdownlint-disable-line -->`
- Disable all rules for the next line: `<!-- markdownlint-disable-next-line -->`
- Disable one or more rules by name: `<!-- markdownlint-disable MD001 MD005 -->`
- Enable one or more rules by name: `<!-- markdownlint-enable MD001 MD005 -->`
- Disable one or more rules by name for the current line: `<!-- markdownlint-disable-line MD001 MD005 -->`
- Disable one or more rules by name for the next line: `<!-- markdownlint-disable-next-line MD001 MD005 -->`
- Capture the current rule configuration: `<!-- markdownlint-capture -->`
- Restore the captured rule configuration: `<!-- markdownlint-restore -->`

For example:
============

```markdown
<!-- markdownlint-disable-next-line no-space-in-emphasis -->
space * in * emphasis

