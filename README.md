## MODUL -3 JAVASCRIPT
## LESSON -19
## REACT.JS

```javascript
- vite and react.js
- starter folders structure 
- npm install -D sass
- tailwind.css
- (npm install -D tailwindcss postcss autoprefixer) 
- (npx tailwindcss init -p)
- js.config.json
- Aliases
```

## VITE CONFIG.JS (ALIASES)

```js
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react-swc'
import { fileURLToPath } from "node:url";

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
  alias: [
    {
      find: "@",
      replacement: fileURLToPath(new URL("./src", import.meta.url)),
    },
    {
      find: "@components",
      replacement: fileURLToPath(new URL("./src/components", import.meta.url)),
    },
    {
      find: "@UIlayouts",
      replacement: fileURLToPath(new URL("./src/components/layouts", import.meta.url)),
    },
    {
      find: "@UIcontainers",
      replacement: fileURLToPath(new URL("./src/components/containers", import.meta.url)),
    },
    {
      find: "@UIform",
      replacement: fileURLToPath(new URL("./src/components/form", import.meta.url)),
    },
    {
      find: "@UIicons",
      replacement: fileURLToPath(new URL("./src/components/icons", import.meta.url)),
    },
    {
      find: "@UI",
      replacement: fileURLToPath(new URL("./src/components/ui", import.meta.url)),
    },
    {
      find: "@layouts",
      replacement: fileURLToPath(new URL("./src/layouts", import.meta.url)),
    },
    {
      find: "@mocks",
      replacement: fileURLToPath(new URL("./src/mocks", import.meta.url)),
    },
    {
      find: "@pages",
      replacement: fileURLToPath(new URL("./src/pages", import.meta.url)),
    },
    {
      find: "@router",
      replacement: fileURLToPath(new URL("./src/router", import.meta.url)),
    },
    {
      find: "@service",
      replacement: fileURLToPath(new URL("./src/service", import.meta.url)),
    },
    {
      find: "@utils",
      replacement: fileURLToPath(new URL("./src/utils", import.meta.url)),
    },

    {
      find: "@reducer",
      replacement: fileURLToPath(new URL("./src/reducer", import.meta.url)),
    },
    {
      find: "@context",
      replacement: fileURLToPath(new URL("./src/context", import.meta.url)),
    },
    {
      find: "@images",
      replacement: fileURLToPath(new URL("./src/assets/images", import.meta.url)),
    },
    {
      find: "@icons",
      replacement: fileURLToPath(new URL("./src/assets/icons", import.meta.url)),
    },
  ],
});
```

## JSCONFIG

```js 
{
    "compilerOptions": {
        "paths": {
            "@/*": ["./src/*"],
            "@components/*": ["./src/components/*"],
            "@UI/*": ["./src/components/ui/*"],
            "@UIlayouts/*": ["./src/components/layouts/*"],
            "@UIform/*": ["./src/components/form/*"],
            "@UIcontainers": ["./src/components/containers/*"],
            "@UIicons": ["./src/components/icons/*"],
            "@images/*": ["./src/assets/images/*"],
            "@icons/*": ["./src/assets/icons/*"],
            "@mocks/*": ["./src/mocks/*"],
            "@utils/*": ["./src/utils/*"],
            "@layout/*": ["./src/layouts/*"],
            "@pages/*": ["./src/pages/*"],
            "@routers/*": ["./src/router/*"],
            "@service/*": ["./src/service/*"],
            "@reducer/*": ["./src/reducer/*"]
        }
    }
}
```