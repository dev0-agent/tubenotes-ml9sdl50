# Learnings

## TypeScript
- An empty file is not considered a module. If you want to import it using `import * as schema from "./schema"`, it must have at least one export (e.g., `export {};`).