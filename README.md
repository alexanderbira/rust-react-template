# Rust WASM with PWA-Enabled Typescript React Template

This template is configured for developing web apps that use Web Assembly compiled from Rust with Cargo alongside a React Typescript template for creating Progressive Web Apps.

# Development

## Project Structure
```bash
root
├─ build
├─ node_modules
├─ public
├─ src
├─ wasm-lib
│  ├─ pkg
│  ├─ src
│  ├─ target
```

- `build` - The compile directory of the web app. Serve this folder over https.
- `node_modules` - Where the Node modules are found.
- `public` - Where static files can be kept. Files here will generally not be modified during the build process.
- `src` - This is where you write your React code. Files here should be treated as modules.
- `wasm-lib` - The Cargo library where the raw and compiled Rust code is kept.
- `wasm-lib/pkg` - The compiled WASM code will be stored here and wrapped in a JS package.
- `wasm-lib/src` - Write your Rust code here. It is the source code of the Cargo library.
- `wam-lib/target` - Ignore this unless you know what you are doing.

## Testing & Debugging
`npm run build:wasm` - Build the Cargo library. Do this before starting the development server.<br>
`npm run start` - Start the development server.<br>
<br>
`npm run test` - Test your React code with your React tests.<br>
`npm run test:wasm` - Test your Rust code with your Rust tests.<br>

# Building
`npm run build:wasm` - Build the Cargo library. Do this before building the React scripts.<br>
`npm run build` - Build your React code.<br>
<br>
Your final web app will be in the `build` directory.