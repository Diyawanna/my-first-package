<!-- 🧪 Step 1: Create Your Package Project

$ mkdir my-first-package
$ cd my-first-package
$ npm init --scope=@diyawanna

Fill out the prompts (or use -y for default).
This will create a package.json with a scoped name like "name": "@diyawanna/my-first-package"
{
  "name": "@diyawanna/my-first-package",
  "version": "1.0.0",
  "description": "My first npm test package",
  "main": "index.js",
  "scripts": {
    "test": "echo \"No tests yet\""
  },
  "repository": {
    "type": "git",
    "url": "https://github.com/Diyawanna/my-first-package.git"
  },
  "keywords": [
    "Diyawanna",
    "Test",
    "first"
  ],
  "author": "@wsmr",
  "license": "MIT",
  "bugs": {
    "url": "https://github.com/Diyawanna/my-first-package/issues"
  },
  "homepage": "https://github.com/Diyawanna/my-first-package#readme"
}

✍️ Step 2: Write Your Package Code
Create a file called index.js:

// index.js
function sayHello(name) {
  return `Hello, ${name}! From @diyawanna package.`;
}
module.exports = { sayHello };

**** SEE -> https://github.com/Diyawanna/my-first-package/commits/main/





📦 Step 3: Update package.json (Optional Enhancements)
Make sure your package.json looks something like this:

{
  "name": "@diyawanna/my-first-package",
  "version": "1.0.0",
  "description": "My first npm test package",
  "main": "index.js",
  "keywords": ["hello", "diyawanna", "test"],
  "author": "Your Name",
  "license": "MIT"
}


🔍 Step 4: Test the Package Locally (Optional)
Before publishing, you can test it locally:
$ npm link

In another project:
$ npm link @diyawanna/my-first-package

Then use it like this:
const { sayHello } = require('@diyawanna/my-first-package');
console.log(sayHello("World"));


**** SEE -> https://github.com/Diyawanna/my-first-package/commits/main/

A.  $ cd /path/to/my-first-package
    $ npm link
   
B.  $ cd /path/to/my-ionic-app
    $ npm link @diyawanna/my-first-package
    $ ionic serve
    
C.  import { sayHello } from '@diyawanna/my-first-package';
    console.log(sayHello('Diyawanna'));

If it's TypeScript, make sure to build it first:

Add tsconfig.json if needed.
Build it:
$ tsc

Then link the compiled output (dist/index.js or similar).

D.  If You Update the Package
    To see changes reflected in the app:
    Rebuild your package (e.g. tsc if using TS).
    It automatically updates in the linked project — no need to reinstall.

E.  When You’re Done
    To unlink and restore the original:
    $ cd /path/to/my-ionic-app
    $ npm unlink @diyawanna/my-first-package
    $ npm install  # to restore other packages if needed



🚀 Step 5: Publish to NPM
If it's a public package:

$ npm publish --access public
🔐 Without --access public, scoped packages are private by default, which requires a paid plan.


🧪 Step 6: Install & Use It Anywhere
After publishing, try installing it from any project:

$ npm i @diyawanna/my-first-package
Use it:
const { sayHello } = require('@diyawanna/my-first-package');
console.log(sayHello("Diyawanna"));


✅ Summary
Step	Description
$ npm init --scope=@diyawanna	Initializes a scoped package
$ npm publish --access public	Publishes it under your npm profile
$ npm i @diyawanna/your-package	How others will install it
 -->


# 📦 @diyawanna/my-first-package

> My first NPM test package — a simple utility that says hello 👋  
> Published by [@diyawanna](https://www.npmjs.com/~diyawanna)

---

## ✨ Features

- 🔹 Lightweight and easy to use
- 🔹 Returns a custom greeting
- 🔹 Useful as a base template for future NPM packages

---

## 🚀 Installation

Install the package via NPM:

```bash
npm install @diyawanna/my-first-package
```

## 🔧 Usage

### In JavaScript (CommonJS)

```js
const { sayHello } = require('@diyawanna/my-first-package');

console.log(sayHello("World"));
// Output: Hello, World! From @diyawanna package.
```

### In TypeScript / ES Modules

```ts
import { sayHello } from '@diyawanna/my-first-package';

console.log(sayHello('Diyawanna'));
// Output: Hello, Diyawanna! From @diyawanna package.
```

## 🔍 Local Development & Testing

### A. Link the Package Locally

In your package directory:

```bash
npm link
```

In your consuming project (e.g., Ionic or Laravel):

```bash
npm link @diyawanna/my-first-package
```

### B. Use in Your Project

**Example for Ionic Angular:**

```ts
import { sayHello } from '@diyawanna/my-first-package';

console.log(sayHello('Ionic App'));
```

**Example for Laravel (with a frontend build):**

```js
import { sayHello } from '@diyawanna/my-first-package';

console.log(sayHello('Laravel'));
```

### C. TypeScript Support (Optional)

If using TypeScript:

1. Add a `tsconfig.json` file.

2. Compile the source with:

```bash
tsc
```

## 🛠️ Development Commands

- 🔧 **Build (if using TypeScript):** `tsc`
- 🔄 **Link to another project:** `npm link @diyawanna/my-first-package`
- ❌ **Unlink when done:** `npm unlink @diyawanna/my-first-package`

## 📦 Publishing to NPM

To publish your package publicly (required for scoped packages like `@diyawanna/*`):

```bash
npm publish --access public
```

> ℹ️ Without `--access public`, scoped packages are private by default.

## 📁 Repository Structure

```
my-first-package/
├── index.js            # Entry point
├── package.json        # Package metadata
└── README.md           # This file
```

## 🧪 Example Function

**index.js**

```js
function sayHello(name) {
  return `Hello, ${name}! From @diyawanna package.`;
}

module.exports = { sayHello };
```

## 🐛 Issues & Feedback

Have a suggestion, question, or bug report?

👉 Open an issue on GitHub

## 📄 License

MIT License

## 🙌 Author

Made with ❤️ by @wsmr  
Published under the @diyawanna namespace.

## 🔗 Useful Links

- 📦 **NPM Package:** [@diyawanna/my-first-package](https://www.npmjs.com/package/@diyawanna/my-first-package)
- 💻 **GitHub Repository:** [github.com/Diyawanna/my-first-package](https://github.com/Diyawanna/my-first-package)

---

### ✅ After Saving It

1. Place this in your project root as `README.md`.
2. Run:
   ```bash
   npm publish --access public
   ```



