# FilterWatchdog - Dev Docs

## Functionality

- This bot will automatically scan filter extensions each update for vulnerabilities (like webview, cookie dough, point-blank, etc...). Additionally, using various techniques ([Unpacking from bundlers](https://www.npmjs.com/package/webcrack), [prettier](https://prettier.io/), and finally AI variable name refactoring will use [Code Llama](https://ai.meta.com/blog/code-llama-large-language-model-coding). It will use a parser to only be fed snippets of code that are called, as of now, but will [switch to](https://link.springer.com/article/10.1007/s10664-022-10274-8#Sec22)) it will deobfuscate the src code to a human-understandable state and describe API changes. The apis found will be automatically blocked in DNSink unless overrided by the config itself[](https://)! A RSS feed will be available as well as a webhook for Discord servers for the changes in functionality of the extension.

## Steps to Deobfuscate SRC

1. [webcrack](https://www.npmjs.com/package/webcrack) is used
2. On NPM and Github the unobfuscated code for the libraries is searched for and if found is included
3. AI name deobufscation

> Eventually this tech will repurposed into its own project to enable binaries (Comprised of Machine Code and Bytecode) and conversion to a higher level language possible. I will use the vast DBs and mods of popular AI solutions with a secondary training level that keeps trying to match the compiled C to the real compiled binary.

## Required

FilterWatchdog require a JS file to configure the backend for:

- Checking interval
- Extensions checked
- API Key (for AI)
