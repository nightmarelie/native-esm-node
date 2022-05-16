# native-esm-node

Visual Studio Code  
By default, VS Code does not add filename extensions when it adds imports for us. That can be changed via the following two settings:

"javascript.preferences.importModuleSpecifierEnding": "js"
"typescript.preferences.importModuleSpecifierEnding": "js"
This is how we can add filename extensions to existing local imports (within a package):

Search: ^(import [^';]_ from '(\./|(\.\./)+)[^';.]_)';
Replace: $1.js';
