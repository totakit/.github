# Contributing to totakit

Thanks for your interest in contributing. Here's how to get started.

## Quick Start

1. Fork the repo
2. Clone your fork
3. Create a branch: `git checkout -b feat/your-feature`
4. Install dependencies: `npm install`
5. Start dev server: `npm run dev`
6. Make your changes
7. Run checks: `npm run lint && npm run typecheck && npm run build`
8. Commit: `git commit -m "feat: your feature"`
9. Push: `git push origin feat/your-feature`
10. Open a Pull Request

## What We're Looking For

| Type | Impact | Example |
|------|--------|---------|
| New tool | HIGH | Add SVG-to-PNG converter |
| Bug fix | HIGH | Fix PDF merge failing on large files |
| Performance | MEDIUM | Reduce image resizer memory usage |
| Accessibility | MEDIUM | Add keyboard navigation to cropper |
| Documentation | LOW | Improve tool descriptions |
| Typo fix | LOW | Fix spelling in README |

## Commit Convention

We use [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: add image rotation support
fix: handle empty file input gracefully
perf: reduce memory usage in PDF merge
a11y: add ARIA labels to file dropzone
docs: update README examples
chore: update dependencies
```

## Code Standards

### Non-Negotiable

- TypeScript strict mode — no `any`, no implicit types
- All processing must be client-side only
- No network calls during file processing
- No `eval()`, `Function()`, or dynamic script injection
- Input validation before processing (type, size, format)
- Memory management: revoke blob URLs, null references after use
- Accessible: ARIA labels, keyboard navigation, sufficient contrast

### Quality Bar

- Mobile responsive
- Works offline (service worker compatible)
- Error messages are user-friendly, not stack traces
- Loading states for any operation > 100ms
- Fallback strategy if WASM fails (JS fallback)

## Adding a New Tool

1. Create the processing logic in `src/lib/tools/[category]/`
2. Create the page in `src/app/tools/[tool-name]/page.tsx`
3. Use the shared `ToolLayout` component for consistent UI
4. Add SEO metadata (title, description, JSON-LD)
5. Add the tool to the sitemap
6. Test on Chrome, Firefox, Safari, and mobile

## CLA

By submitting a pull request, you agree to the [Contributor License Agreement](https://totakit.com/cla). This ensures we can distribute your contribution under the project's license.

## AI-Assisted Contributions

We welcome AI-assisted contributions. Here's our policy:

### Allowed

- Using AI for research, drafting, and formatting
- Using AI to generate boilerplate code
- Using AI to write tests
- Using AI to improve documentation

### Required

- Human verification of all code — AI hallucinates. You must test.
- Human verification of all claims — check that docs are accurate.
- Security review — AI-generated code must pass the same security bar.
- Disclosure if asked — if someone asks "did you use AI?", be honest.

### Not Allowed

- Submitting AI output without review or testing
- AI-generated code that makes network calls during processing
- AI-generated code that uses `eval()` or dynamic script injection

### Why This Policy

The value of totakit is tool quality and user trust, not production method. A well-tested, AI-assisted tool is better than a poorly-tested, human-only tool. We care about the output, not the process.

## Questions?

- [Discussions](https://github.com/totakit/totakit.github.io/discussions) for general questions
- [Issues](https://github.com/totakit/totakit.github.io/issues) for bugs and feature requests
- [hello@totakit.com](mailto:hello@totakit.com) for private inquiries
