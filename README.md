# Dependency Cruiser

This document provides instructions on how to install and use Dependency Cruiser to visualize your project's dependencies.

## Installation

### Step 1: Install Dependency Cruiser

```bash
npm install --save-dev dependency-cruiser
```

### Step 2: Generate Configuration File
Initialize Dependency Cruiser and create a configuration file (.dependency-cruiser.js

```bash
npx depcruise --init
```

### Step 3: Install Graphviz (Windows Only)
For Windows, you will need to install Graphviz to generate dependency graphs. Download and install the installer from the following link:

[Download Graphviz](<[https://gitlab.com/api/v4/projects/4207231/packages/generic/graphviz-releases/12.2.1/windows_10_cmake_Release_graphviz-install-12.2.1-win64.exe]>).


### Step 4: Add Graphviz to System Path
After installation, add the Graphviz bin folder to your system's PATH:

```bash
C:\Program Files\Graphviz\bin
```

check installation
```bash
dot -v
```

### Step 5: Add Script to package.json
Add the following script to your package.json to generate a PNG image of the dependency graph:

```bash
"scripts": {
  "dep-graph": "npx depcruise --output-type dot src | dot -T png -o dependency-graph.png"
}

```



I also created a Loom video explaining the process. Check it out [here](<https://www.loom.com/share/8290e56753a54717b1f95f60b229af43>).





