# Combinio

![License](https://img.shields.io/badge/license-MIT-blue.svg)

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Exclusion Lists](#exclusion-lists)
- [Supported File Extensions](#supported-file-extensions)
- [Example](#example)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

**Combinio** is a Node.js script designed to aggregate all your project’s code files into a single `combined.txt` file. This is particularly useful for utilizing AI tools to review your code structure or for creating a consolidated view of your project.

## Features

- **Recursive Directory Traversal**: Scans through all subdirectories starting from the root directory.
- **Exclusion Options**: Excludes specified directories and files from the aggregation process.
- **Selective File Inclusion**: Combines only files with specified extensions.
- **Whitespace Optimization**: Reduces unnecessary whitespace in the combined output.
- **Error Handling**: Logs errors encountered during file reading without halting the process.

## Prerequisites

- **Node.js**: Ensure you have Node.js installed. You can download it from [here](https://nodejs.org/).

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/combinio.git
   ```

2. **Navigate to the Project Directory**

   ```bash
   cd combinio
   ```

3. **Install Dependencies**

   This project uses only Node.js built-in modules, so there are no external dependencies. However, if you plan to extend it, initialize `package.json`:

   ```bash
   npm init -y
   ```

## Configuration

Before running the script, you can configure the exclusion lists and file extensions as needed. Open the `combine.js` file and modify the following sections:

### Excluded Directories

```javascript
const excludeDirs = ['node_modules', '.git', 'dist', 'build', '.svcode'];
```

### Excluded Files

```javascript
const excludeFiles = ['package-lock.json'];
```

### Included File Extensions

```javascript
const includeExtensions = [
  '.js',
  '.jsx',
  '.ts',
  '.tsx',
  '.html',
  '.css',
  '.scss',
  '.json',
  '.md',
  '.py',
  '.java',
  '.cpp',
  '.c',
  // Add other extensions as needed
];
```

## Usage

1. **Run the Script**

   Ensure you are in the project root directory and execute:

   ```bash
   node combine.js
   ```

2. **Output**

   Upon successful execution, a `combined.txt` file will be generated in the root directory containing all the aggregated code files.

## Exclusion Lists

The script excludes certain directories and files to prevent unnecessary or sensitive data from being included in the combined output.

### Excluded Directories

- `node_modules`: Contains project dependencies.
- `.git`: Git version control folder.
- `dist` / `build`: Distribution/build folders.
- `.svcode`: Custom directory (can be modified as needed).

### Excluded Files

- `package-lock.json`: Lockfile for npm dependencies.

## Supported File Extensions

The script includes files with the following extensions by default:

- **JavaScript**: `.js`, `.jsx`
- **TypeScript**: `.ts`, `.tsx`
- **Markup**: `.html`, `.md`
- **Stylesheets**: `.css`, `.scss`
- **Data**: `.json`
- **Python**: `.py`
- **Java**: `.java`
- **C/C++**: `.c`, `.cpp`
- **Add more as needed in the `includeExtensions` array.**

## Example

After running the script, your `combined.txt` might look like this:

```
===== src/index.js =====
const fs = require('fs');
const path = require('path');
// ... rest of the code

===== src/utils/helper.js =====
function helper() {
  // ... helper functions
}

===== README.md =====
# Project Title
...
```

Each file's content is preceded by a header indicating its relative path.

## Contributing

Contributions are welcome! Please follow these steps:

1. **Fork the Repository**

2. **Create a New Branch**

   ```bash
   git checkout -b feature/YourFeature
   ```

3. **Commit Your Changes**

   ```bash
   git commit -m "Add feature XYZ"
   ```

4. **Push to the Branch**

   ```bash
   git push origin feature/YourFeature
   ```

5. **Open a Pull Request**

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

- **Author**: Your Name
- **Email**: your.email@example.com
- **GitHub**: [yourusername](https://github.com/yourusername)
