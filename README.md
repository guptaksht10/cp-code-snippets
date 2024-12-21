# Competitive Programming Setup
This repository contains code snippets and Sublime Text build settings tailored for competitive programming. The goal is to streamline the workflow for problem-solving by providing reusable templates and efficient build configurations.

## Repository Contents
  1. Code Snippets
      Predefined templates for frequently used algorithms and data structures.
      Snippets are categorized by their purpose, such as:
          a. Graph snippets (DFS/BFS)
          b. Dynamic Programming patterns
          c. Common utilities (modular arithmetic, fast I/O)
  
  2. Sublime Text Build Settings
        Custom build configurations to compile and run programs quickly.
        Configured for popular language used in CP : C++: Leveraging g++ with optimization flags.

## How to Use Code Snippets
  1. Clone the repository:
     
          git clone https://github.com/guptaksht10/cp-code-snippets/

  2. Copy or reference the snippets as needed in your solutions.
  3. To integrate into Sublime Text, save snippets in the Packages/User folder:
  Path: Preferences > Browse Packages > User

## Sublime Text Build Settings
  1. Navigate to Tools > Build System > New Build System....
  2. Replace the content with the provided settings

          {
              "cmd": ["g++", "-std=c++17", "-Wall", "-Wextra", "-O2", "$file", "-o", "${file_path}/${file_base_name}.out"],
              "file_regex": "^(.*):([0-9]+):?([0-9]*)",
              "working_dir": "${file_path}",
              "selector": "source.c++, source.cpp",
              "variants": [
                  {
                      "name": "Run",
                      "cmd": ["${file_path}/${file_base_name}.out"]
                  }
              ]
          }

  3. Save the file as CP-C++.sublime-build in the same User directory.

## Recommended Sublime Text Plugins
  1. Competitive Programming Helper: Automates input/output setup for CP.
  2. C++ Snippets: Provides commonly used C++ code templates.
  3. SublimeLinter: Highlights syntax and runtime errors in real-time.

## Usage Tips
  Use the Run variant in the build system for quick execution after compilation.
  Map custom keyboard shortcuts for faster compilation:
  Go to Preferences > Key Bindings and add:

    {
      "keys": ["ctrl+b"], 
      "command": "build", 
      "args": {"variant": "Run"}
    }

## License
Feel free to use and adapt this setup for your competitive programming needs. Contributions are welcome!


