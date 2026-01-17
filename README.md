---

# LazyVim Go IDE Configuration

This repository provides a **Neovim + LazyVim configuration for Go development**, offering an IDE-like experience with LSP, formatting, linting, debugging, and Go-specific tooling.

---

## ✨ Features

* Go LSP support via **gopls**
* Auto-formatting with **gofumpt** and **goimports**
* Linting using **golangci-lint**
* Debugging with **Delve (DAP)**
* Treesitter syntax highlighting
* Go utilities (tests, struct tags, implementations, etc.)
* Fully integrated with **LazyVim**

---

## 📦 Prerequisites

Make sure the following are installed:

* **Go** (latest stable)
* **Neovim** (v0.9+ recommended)
* **Git**
* **LazyVim**

---

## 🔧 Install Required Go Tools

Run the following commands to install Go tooling:

### LSP

```bash
go install golang.org/x/tools/gopls@latest
```

### Formatting

```bash
go install golang.org/x/tools/cmd/goimports@latest
go install mvdan.cc/gofumpt@latest
```

### Debugging

```bash
go install github.com/go-delve/delve/cmd/dlv@latest
```

### Linting

```bash
go install github.com/golangci/golangci-lint/cmd/golangci-lint@latest
```

---

## 🧭 Update PATH

Add Go binaries to your `PATH`.

### For Bash (`~/.bashrc`)

```bash
export PATH="$PATH:$(go env GOPATH)/bin"
```

Reload your shell:

```bash
source ~/.bashrc
```

---

## 🚀 Installation

### 1️⃣ Install LazyVim

Follow the official LazyVim installation guide:
👉 [https://github.com/LazyVim/LazyVim](https://github.com/LazyVim/LazyVim)

---

### 2️⃣ Backup Existing Neovim Config (Optional but Recommended)

```bash
mv ~/.config/nvim ~/.config/nvim.bak
```

---

### 3️⃣ Clone This Repository

```bash
git clone https://github.com/mehedi-imam241/lazyvim-go-ide.git ~/.config/nvim
```

---

### 4️⃣ Start Neovim

```bash
nvim
```

Lazy.nvim will automatically install all required plugins.

---

## 🧪 Verify Installation

Inside Neovim, run:

```vim
:LspInfo
```

You should see:

* `gopls` attached to Go buffers

Check formatting:

```vim
<leader>cf
```

---

## ⌨️ Common Keybindings

| Action              | Key          |
| ------------------- | ------------ |
| Go to definition    | `gd`         |
| Hover documentation | `K`          |
| Rename              | `<leader>cr` |
| Code actions        | `<leader>ca` |
| Format file         | `<leader>cf` |
| Debug start         | `<leader>dd` |
| Toggle breakpoint   | `<leader>db` |
| Run nearest test    | `<leader>tn` |

---

## 🛠 Troubleshooting

* Ensure `$GOPATH/bin` is in your `PATH`
* Run `:checkhealth` inside Neovim
* Make sure Go tools are installed correctly:

  ```bash
  which gopls gofumpt dlv golangci-lint
  ```

---

## 📜 License

MIT License

---

## 🙌 Acknowledgements

* [LazyVim](https://github.com/LazyVim/LazyVim)
* [Go.nvim](https://github.com/ray-x/go.nvim)
* [Neovim](https://neovim.io)

---




