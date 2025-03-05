# tree2files 🏗️

**Convert an AI-generated tree structure into real files & directories.**

## 🚀 Features
✅ Parses tree format from AI output (e.g., ChatGPT, Copilot).
✅ Creates files & folders **without overwriting existing files**.
✅ Optionally **skips the root folder** (perfect for pre-existing repos).

## 📦 Installation
Clone this repo and move the script somewhere in your `$PATH`:
```sh
git clone https://github.com/bline/tree2files.git
cd tree2files
chmod +x tree2files
mv tree2files ~/.local/bin/  # Or /usr/local/bin/ for global usage
```

## 🔧 Usage
1. Save your AI-generated project structure in `structure.txt`:
   ```
   myproject/
   ├── Cargo.toml
   ├── package.json
   ├── src/
   │   ├── lib.rs
   │   └── ts/
   │       ├── index.ts
   │       ├── validator.ts
   │       └── types.ts
   ├── examples/
   │   ├── browser.html
   │   └── node.js
   └── tests/
       ├── validator.test.ts
       └── schemas/
   ```

2. Run:
   ```sh
   tree2files structure.txt
   ```
   This creates the full directory structure.

3. **If you already cloned a Git repo** and want files inside it:
   ```sh
   tree2files structure.txt --strip-root
   ```

4. Open in VS Code:
   ```sh
   code .
   ```

## 🎯 Why Use This?
- **Saves time**: No need to manually create files after AI-generated output.
- **Safe**: Doesn't overwrite existing files.
- **Lightweight**: No dependencies, just a single script!

## 📄 License
MIT License. Contributions welcome!
