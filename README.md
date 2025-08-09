# RISC-V Codegen Challenge

A cross-language code generation workflow: **YAML → Python → C header → C program → YAML**.

##  Highlights
- Parse structured YAML input (`input.yaml`) using Python
- Auto-generate a C header (`data_gen.h`) with `#define` macros
- Use a C program (`main.c`) to emit YAML based on the header
- Complete round-trip transformation with verified output

## Key Files
- `generate_header.py` – Python script to convert YAML → C header
- `data_gen.h` – Auto-generated constants
- `main.c` – Emits YAML using header constants
- `output.yaml` – Final generated YAML

##  Usage
```bash
# Install dependencies
sudo apt update
sudo apt install gcc python3 python3-pip
pip3 install pyyaml

# Generate header
python3 generate_header.py input.yaml > data_gen.h

# Compile & run
gcc main.c -o emit_yaml
./emit_yaml

 Learnings

    Cross-language data transformation

    Real-world YAML parsing with nested structures

    File I/O and macro handling in C

 Read the full documentation here


---

I added a **link at the bottom** so visitors can click to see the full detailed README in `docs/README-full.md`.  

Do you want me to now give you the **full detailed version** so we can place it in `docs/README-full.md`? That way your repo will be complete.
