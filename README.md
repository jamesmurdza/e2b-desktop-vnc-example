# E2B Desktop + VNC Example

This example shows how you can run use E2B Desktop with VNC. It's as easy as:

```typescript
import { Desktop } from "./sandbox.ts";

const desktop = await Desktop.create("desktop-dev-v2");
console.log("Desktop Sandbox started, ID:", desktop.sandboxId);
await desktop.vncServer.start();
console.log("VNC URL:", desktop.vncServer.getUrl(true));
```

## Running the example

Set the E2B API KEY in `.env`:

```
E2B_API_KEY = ...
```

Install dependencies:

```
npm install
```

Run the example script:

```
npm run dev
```
