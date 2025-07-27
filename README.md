# VS Code Settings

## Settings

```json
{
  // =============================================================================
  // EDITOR CONFIGURATION
  // =============================================================================
  "editor.fontSize": 14,
  "editor.lineHeight": 22,
  "editor.fontFamily": "Cascadia Code",
  "editor.fontLigatures": true,
  "editor.tabSize": 2,
  "editor.insertSpaces": true,
  "editor.detectIndentation": false,
  "editor.wordWrap": "on",
  "editor.minimap.enabled": false,
  "editor.linkedEditing": true,
  "editor.snippetSuggestions": "top",
  "editor.suggestSelection": "first",
  "editor.renderWhitespace": "all",
  "editor.cursorSmoothCaretAnimation": "on",
  "editor.codeLens": true,

  // =============================================================================
  // FORMATTING CONFIGURATION
  // =============================================================================
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit",
    "source.organizeImports": "explicit"
  },

  // Language-specific formatters
  "[css]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[json]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[jsonc]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[markdown]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[scss]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },

  // =============================================================================
  // WORKBENCH CONFIGURATION
  // =============================================================================
  "workbench.iconTheme": "catppuccin-mocha",
  "workbench.colorTheme": "Catppuccin Mocha",
  "workbench.editor.revealIfOpen": true,
  "window.newWindowProfile": "Default",

  // =============================================================================
  // FILES CONFIGURATION
  // =============================================================================
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1000,
  "files.trimTrailingWhitespace": true,
  "files.insertFinalNewline": true,

  // =============================================================================
  // SEARCH CONFIGURATION
  // =============================================================================
  "search.exclude": {
    "**/node_modules": true
  },
  "search.useIgnoreFiles": false,

  // =============================================================================
  // TERMINAL CONFIGURATION
  // =============================================================================
  "terminal.integrated.fontSize": 13,
  "terminal.integrated.fontFamily": "monospace",

  // =============================================================================
  // EXPLORER CONFIGURATION
  // =============================================================================
  "explorer.confirmDelete": false,

  // =============================================================================
  // LANGUAGE-SPECIFIC CONFIGURATION
  // =============================================================================
  "javascript.updateImportsOnFileMove.enabled": "always",
  "javascript.preferences.organizeImports": {
    "enabled": true
  },
  "typescript.updateImportsOnFileMove.enabled": "always",

  // =============================================================================
  // EXTENSIONS CONFIGURATION
  // =============================================================================

  // GitHub Copilot
  "github.copilot.nextEditSuggestions.enabled": true,

  // ESLint
  "eslint.enable": true,
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact",
    "react",
    "vue",
    "html"
  ],

  // Indent Rainbow
  "indentRainbow.indicatorStyle": "light",
  "indentRainbow.colors": [
    "#f5e0dc",
    "#f2cdcd",
    "#cba6f7",
    "#b4befe",
    "#a6e3a1",
    "#94e2d5",
    "#f9e2af",
    "#fab387"
  ]
}

```
