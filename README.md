# VS Code Settings

## Settings

```json
{
  "accessibility.signals.chatEditModifiedFile": {
    "sound": "off"
  },
  "editor.accessibilitySupport": "off",
  "editor.fontFamily": "JetBrains Mono",
  "editor.fontLigatures": true,
  "editor.fontSize": 14,
  "editor.lineHeight": 22,
  "editor.tabSize": 2,
  "editor.insertSpaces": true,
  "editor.detectIndentation": false,
  "editor.wordWrap": "on",
  "editor.linkedEditing": true,
  "editor.snippetSuggestions": "top",
  "editor.suggestSelection": "first",
  "editor.renderWhitespace": "all",
  "editor.cursorSmoothCaretAnimation": "on",
  "editor.codeLens": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnPaste": true,
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit",
    "source.organizeImports": "explicit",
    "source.sortImports": "explicit",
    "source.removeUnusedImports": "explicit"
  },
  "[css]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[go]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "golang.go"
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
    "diffEditor.ignoreTrimWhitespace": false,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.quickSuggestions": {
      "other": "off",
      "comments": "off",
      "strings": "off"
    }
  },
  "[prisma]": {
    "editor.defaultFormatter": "Prisma.prisma"
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
  "[vue]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "javascript.updateImportsOnFileMove.enabled": "always",
  "javascript.preferences.organizeImports": {
    "enabled": true
  },
  "typescript.updateImportsOnFileMove.enabled": "always",
  "files.autoSave": "onWindowChange",
  "files.defaultLanguage": "markdown",
  "files.insertFinalNewline": true,
  "files.trimTrailingWhitespace": true,
  "explorer.confirmDelete": false,
  "explorer.confirmDragAndDrop": false,
  "explorer.confirmPasteNative": false,
  "search.exclude": {
    "**/node_modules/**": true
  },
  "search.useIgnoreFiles": false,
  "terminal.integrated.cursorBlinking": true,
  "terminal.integrated.fontFamily": "monospace",
  "terminal.integrated.fontSize": 13,
  "workbench.activityBar.location": "top",
  "workbench.colorTheme": "Catppuccin Mocha",
  "workbench.editor.enablePreview": false,
  "workbench.editor.limit.enabled": true,
  "workbench.editor.limit.value": 6,
  "workbench.editor.preferHistoryBasedLanguageDetection": true,
  "workbench.editor.revealIfOpen": true,
  "workbench.iconTheme": "catppuccin-mocha",
  "workbench.startupEditor": "none",
  "window.confirmSaveUntitledWorkspace": false,
  "window.newWindowProfile": "Default",
  "catppuccin.accentColor": "rosewater",
  "catppuccin.extraBordersEnabled": true,
  "catppuccin.italicComments": false,
  "catppuccin.italicKeywords": false,
  "catppuccin-icons.hidesExplorerArrows": true,
  "containers.containerClient": "com.microsoft.visualstudio.containers.docker",
  "containers.orchestratorClient": "com.microsoft.visualstudio.orchestrators.dockercompose",
  "git.confirmSync": false,
  "git.enableSmartCommit": true,
  "github.copilot.nextEditSuggestions.enabled": true,
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
  "prettier.trailingComma": "all",
  "indentRainbow.colors": [
    "#f38ba8",
    "#fab387",
    "#f9e2af",
    "#a6e3a1",
    "#89dceb",
    "#cba6f7"
  ],
  "indentRainbow.indicatorStyle": "light",
  "go.toolsManagement.autoUpdate": true,
  "gopls": {
    "ui.semanticTokens": true
  }
}
```

## Snippets

```json
{
  "Wrap with div": {
    "scope": "html,javascript,typescript,javascriptreact,typescriptreact,vue",
    "prefix": "wwd",
    "body": ["<div>", "\t$TM_SELECTED_TEXT$0", "</div>"],
    "description": "Wrap selected HTML with a div"
  },
  "Wrap with react fragment": {
    "scope": "html,javascript,typescript,javascriptreact,typescriptreact,vue",
    "prefix": "wwr",
    "body": ["<>", "\t$TM_SELECTED_TEXT$0", "</>"],
    "description": "Wrap selected code with a React fragment"
  },
  "Wrap with Custom Component": {
    "scope": "html,javascript,typescript,javascriptreact,typescriptreact,vue",
    "prefix": "wwcc",
    "body": [
      "<${1:MyComponent}>$0",
      "  ${TM_SELECTED_TEXT}",
      "</${1:MyComponent}>"
    ],
    "description": "Wrap selected JSX with a custom component and allow renaming"
  },
  "Wrap with HTML tag": {
    "scope": "html,javascript,typescript,javascriptreact,typescriptreact,vue",
    "prefix": "wwt",
    "body": ["<${1:div}>$0", "\t${TM_SELECTED_TEXT}", "</${1:div}>"],
    "description": "Wrap selected HTML with a specified tag"
  },
  "React Component (JS)": {
    "scope": "javascriptreact,typescriptreact",
    "prefix": "rfc",
    "body": [
      "export const ${1:${TM_FILENAME_BASE/([\\w]+)([-_])([\\w])/${1:/capitalize}${3:/capitalize}/g}} = () => {",
      "  return (",
      "    <div>",
      "      <p>${1:${TM_FILENAME_BASE/([\\w]+)([-_])([\\w])/${1:/capitalize}${3:/capitalize}/g}}</p>",
      "      $0",
      "    </div>",
      "  );",
      "}"
    ],
    "description": "Create a React component in JavaScript with filename as component name"
  },
  "React Component with TypeScript": {
    "scope": "typescriptreact",
    "prefix": "rfct",
    "body": [
      "type ${1:${TM_FILENAME_BASE/([\\w]+)([-_])([\\w])/${1:/capitalize}${3:/capitalize}/g}}Props = {",
      "  ",
      "};",
      "",
      "export const ${1:${TM_FILENAME_BASE/([\\w]+)([-_])([\\w])/${1:/capitalize}${3:/capitalize}/g}} = ({}: ${1:${TM_FILENAME_BASE/([\\w]+)([-_])([\\w])/${1:/capitalize}${3:/capitalize}/g}}Props) => {",
      "  return (",
      "    <div>",
      "      <p>${1:${TM_FILENAME_BASE/([\\w]+)([-_])([\\w])/${1:/capitalize}${3:/capitalize}/g}}</p>",
      "      $0",
      "    </div>",
      "  );",
      "}"
    ],
    "description": "Create a React component with TypeScript and typed props, using filename as component name"
  },
  "React useState": {
    "scope": "javascriptreact,typescriptreact",
    "prefix": "us",
    "body": [
      "const [${1:state}, set${2/(.*)/${1:/capitalize}/}] = useState${3:}(${4});$0"
    ],
    "description": "Declare a React useState hook with auto-capitalized setter"
  },
  "React useEffect": {
    "scope": "javascriptreact,typescriptreact",
    "prefix": "ue",
    "body": ["useEffect(() => {", "\t$0", "}, []);"],
    "description": "Create a React useEffect hook with dependencies"
  },
  "Wrap with try-catch": {
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "prefix": "wwtc",
    "body": [
      "try {",
      "\t${TM_SELECTED_TEXT}$0",
      "} catch (${1:error}) {",
      "\tif (process.NODE_ENV === 'development') {",
      "\t\tconsole.error(${1:error});",
      "\t}",
      "}"
    ],
    "description": "Wrap selected code with a try-catch block"
  },
  "Console log with label": {
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "prefix": "slog",
    "body": ["console.log('${1}:', ${1});$0"],
    "description": "Console log with a custom label and variable"
  }
}
```
