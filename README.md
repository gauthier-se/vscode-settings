# VS Code Settings

## Settings

```json
{
  // Editor
  "editor.fontSize": 14,
  "editor.lineHeight": 22,
  "editor.fontFamily": "JetBrains Mono",
  "editor.fontLigatures": true,
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

  // Formatting
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit",
    "source.organizeImports": "explicit",
    "source.sortImports": "explicit",
    "source.removeUnusedImports": "explicit"
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

  // JavaScript/TypeScript
  "javascript.updateImportsOnFileMove.enabled": "always",
  "javascript.preferences.organizeImports": {
    "enabled": true
  },
  "typescript.updateImportsOnFileMove.enabled": "always",
  "typescript.inlayHints.variableTypes.enabled": true,
  "typescript.inlayHints.parameterTypes.enabled": true,
  "typescript.inlayHints.parameterNames.enabled": "literals",

  // Workbench
  "workbench.iconTheme": "catppuccin-mocha",
  "workbench.colorTheme": "Catppuccin Mocha",
  "workbench.startupEditor": "none",
  "workbench.editor.revealIfOpen": true,
  "workbench.editor.preferHistoryBasedLanguageDetection": true,
  "workbench.editor.enablePreview": false,
  "workbench.editor.limit.enabled": true,
  "workbench.editor.limit.value": 6,

  // Window
  "window.newWindowProfile": "Default",
  "window.confirmSaveUntitledWorkspace": false,

  // Files
  "files.autoSave": "onWindowChange",
  "files.trimTrailingWhitespace": true,
  "files.insertFinalNewline": true,
  "files.defaultLanguage": "markdown",

  // Explorer
  "explorer.confirmDelete": false,
  "explorer.confirmDragAndDrop": false,

  // Search
  "search.exclude": {
    "**/node_modules/**": true
  },
  "search.useIgnoreFiles": false,

  // Terminal
  "terminal.integrated.fontSize": 13,
  "terminal.integrated.fontFamily": "monospace",
  "terminal.integrated.cursorBlinking": true,

  // Accessibility
  "accessibility.signals.chatEditModifiedFile": {
    "sound": "off"
  },

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

  // Prettier
  "prettier.trailingComma": "all",

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
  ],

  // Catppuccin Theme
  "catppuccin.accentColor": "rosewater",

  // Containers
  "containers.containerClient": "com.microsoft.visualstudio.containers.docker",
  "containers.orchestratorClient": "com.microsoft.visualstudio.orchestrators.dockercompose"
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
