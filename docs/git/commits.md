


> Commits are snapshots of your entire repository at specific times…based around logical units of change. 
> Over time, commits should tell a story of the history of your repository and how it came to be the way that it currently is.


We use the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification for commit messages because it works well with the automated versioning and changelog generation as well as semantically versioning.

The commit contains the following structural elements, to communicate intent to the consumers of your library:

- **fix:** a commit of the type fix patches a bug in your codebase (this correlates with PATCH in Semantic Versioning).
- **feat:**  a commit of the type feat introduces a new feature to the codebase (this correlates with MINOR in Semantic Versioning).
- **BREAKING CHANGE:**  a commit that has a footer BREAKING CHANGE:, or appends a ! after the type/scope, introduces a breaking API change (correlating with MAJOR in Semantic Versioning). A BREAKING CHANGE can be part of commits of any type.
- **build:** anything related to the build process. Configs, scripts, package.json etc.
- **chore:** updating packages, updating configs, etc. 
- **ci:** pipeline changes (e.g. travis, circle, etc)
- **docs:** markdown, jsdoc, etc 
- **style:** ui/ux changes (e.g. css, html, etc) 
- **refactor:** improvements to code readability, removal of duplication, restructuring of code, etc
- **perf:** performance improvements
- **test:** jest / puppeteer / cypress / etc

## BREAKING CHANGES use a ! suffix, eg. chore!: drop Node 6 from testing matrix

when commiting, use the following format:

```bash
    <type>(<scope>): <subject>
    <BLANK LINE>
    <body> // why was the change made?
    <BLANK LINE>
    <footer> // mandatory if BREAKING CHANGE
```