# codeql-monorepo

Codeql monorepo to do analysis individually.

## Overview

This repository is a monorepo for performing CodeQL analysis on a variety of codebases. It is designed to support individual analysis on projects written in multiple languages, including PHP, C#, JavaScript, CSS, ASP.NET, and HTML. The goal of this repo is to provide a centralized place for CodeQL queries, experiments, and language-specific configurations.

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/org-contoso/codeql-monorepo.git
   cd codeql-monorepo
   ```

2. **Install CodeQL CLI:**  
   Follow the instructions on the [CodeQL CLI documentation](https://docs.github.com/en/code-security/code-scanning/using-codeql-cli) to install CodeQL.

3. **Install any additional dependencies:**  
   Depending on the language you want to analyze, you may need to install additional tools or libraries (e.g., PHP, .NET SDK, Node.js).

## Usage

1. **Run a CodeQL Analysis:**
   ```bash
   codeql database create db-[language] --language=[language]
   codeql database analyze db-[language] [path-to-qlpack] --format=sarifv2.1.0 --output=results.sarif
   ```

   Replace `[language]` with the target language (e.g., php, csharp, javascript).  
   Replace `[path-to-qlpack]` with the path to the relevant CodeQL queries.

2. **View Results:**  
   The output SARIF file can be uploaded to GitHub or viewed using compatible tools like the [SARIF Viewer extension for VS Code](https://marketplace.visualstudio.com/items?itemName=MS-SarifVSCode.sarif-tools).
