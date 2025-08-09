# RISC-V Codegen Challenge

This repository contains the implementation for the **RISC-V Code Generation Challenge**, demonstrating a complete workflow from **YAML parsing** to **C header generation** and **YAML re-emission** using cross-language code generation.

## Directory Structure

codegen-challenge/
Codegen Challenge Report.docx # Detailed report of the challenge
 generate_header.py # Python script to parse YAML and generate C header
 input.yaml # Original YAML input (from RISC-V Unified Database)
 data_gen.h # Auto-generated C header file with #defines
 main.c # C program to emit YAML using header constants
 output.yaml # YAML output generated from the C program


---

## Objectives Achieved

-  Parse structured YAML input using Python  
-  Auto-generate C header (`data_gen.h`) with `#define` macros  
-  Write a C program to emit YAML using constants from the header  
-  Perform a full round-trip: **YAML â†’ Header â†’ YAML**  
-  Compile & run C code using GCC  
-  Verify generated YAML matches original input  

---

##   How to Run

### Install Dependencies
```bash
sudo apt update
sudo apt install gcc python3 python3-pip
pip3 install pyyaml
```

### Generate the C Header from YAML
```bash
python3 generate_header.py input.yaml > data_gen.h
```

### Compile the C Program
```bash
gcc main.c -o emit_yaml
```

###  Run the Program
```bash
./emit_yaml
```
This generates output.yaml.

---

## Example Output

```
- package: markdown-it_markdown-it
  version: 13.0.1
  commit: e843acc9edad115cbf8cf85e676443f01658be08
  date: May 3, 2022
  notes:
    - Rename variables that use python built-in names...
    - Convert JS `for` loops to `while` loops...
    ...
```

---

## Key Learnings

- Cross-language data transformation  
- Working with real-world YAML parsing and nested data  
- C macro usage for storing structured data  
- Managing file I/O in C  
- End-to-end simulation of compiler-style code generation  

---

## License

This project is released under the MIT License.

