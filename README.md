#  🧹 vite-plugin-yaml

Transforms a YAML file into a JS object. 

## 🚀 Install
```
npm install -D @modyfi/vite-plugin-yaml
# or
# yarn add -D @modyfi/vite-plugin-yaml
# or
# pnpm i -D @modyfi/vite-plugin-yaml
```

## 🦄 Usage

Add `ViteYAML` to `vite.config.js / vite.config.ts` and configure it:

```ts
// vite.config.js / vite.config.ts
import ViteYaml from '@modyfi/vite-plugin-yaml';

export default {
  plugins: [
    ViteYaml() // config by passing in an object with the options listed below
  ]
}
```

## 🐛 Options
```ts
/**
 * A minimatch pattern, or array of patterns, which specifies the files in the build the plugin
 * should operate on.
 * By default all files are targeted.
 */
include?: FilterPattern;
/**
 * A minimatch pattern, or array of patterns, which specifies the files in the build the plugin
 * should _ignore_.
 * By default no files are ignored.
 */
exclude?: FilterPattern;
/**
 * Schema used to parse yaml files.
 * See https://github.com/nodeca/js-yaml/blob/49baadd52af887d2991e2c39a6639baa56d6c71b/README.md#load-string---options-
 */
schema?: Schema;
/**
 * A function that will be called for error reporting.
 * Defaults to `console.warn()`.
 */
onWarning?: (warning: YAMLException) => void;
```