# Pi Extension template
Has sane `package.json` and example of basic example at `src/index.ts`

## Export the rendered system prompt

To inspect the complete system prompt produced by `src/build-system-prompt.ts`, run:

```bash
pnpm prompt:emit
```

This writes `.test-output/system-prompt.txt`, which is gitignored. The standalone export uses Pi's standard `read`, `bash`, `edit`, and `write` tool definitions. Session-specific inputs (skills, context files, `SYSTEM.md`, and `APPEND_SYSTEM.md`) are not included.

To export somewhere else for review, pass `--output`:

```bash
pnpm prompt:emit -- --output system-prompt.txt
```