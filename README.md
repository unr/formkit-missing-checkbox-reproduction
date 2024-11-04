# Nuxt x Formkit Broken Checkbox Example

Bare minimum setup to showcase broken checkbox.

## THE FIX

You need to ensure the regenesis icons are added.

```js
import { defineFormKitConfig } from '@formkit/vue'
import { rootClasses } from './formkit.theme'
import { genesisIcons } from "@formkit/icons"
export default defineFormKitConfig({
    config: {
        rootClasses,
    },
    icons: genesisIcons
})
```

![image](https://github.com/user-attachments/assets/4b165bd1-2ea4-4262-a8bc-777e43af6501)


## How to Use

```bash
# pnpm
pnpm install
pnpm dev
```

## Example of Original Issue

![image](https://github.com/user-attachments/assets/957b4f12-c901-478f-81b9-85c73583afd2)
