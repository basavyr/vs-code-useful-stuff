# Latex-workshop fix
## Extenstion for compiling latex files inside Visual Studio Code 

* Changes to the VS Code settings for the extension `latex-workshop`. 
* It successfully compiles `.tex` files for paths with special characters (e.g. `~`). 
* **Works for files within iCloud**.

### How to fix

> Just copy the command from `settings.json` into the VS Code general settings. 
Everything should work fine after the settings update.  
`.tex` should compile without issues.  

```
"latex-workshop.latex.tools": [ {
"name": "latexmk", "command": "latexmk", "args": [
"-synctex=1", "-interaction=nonstopmode", "-file-line-error",
"-pdf",
"-outdir=./",
"%DOCFILE%"
],
"env": {}
} ]
```


