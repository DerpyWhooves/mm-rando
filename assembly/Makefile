BUILD_PY := scripts/build.py
PYTHON   := python

# Directories used for copying built Asm patch files to MMR Resources directory.
GEN_DIR  := target/mm/data/generated
RES_DIR  := ../MMR.Randomizer/Resources/asm

# Build for Majora's Mask by default
all: mm

# Build for "mm" target (Majora's Mask)
mm:
	$(PYTHON) $(BUILD_PY) -t mm --compile-c --virtual

# Build for "oot" target (Ocarina of Time)
oot:
	$(PYTHON) $(BUILD_PY) -t oot --compile-c

copy: mm
	cp $(GEN_DIR)/rom_patch.txt $(RES_DIR)
	cp $(GEN_DIR)/symbols.json  $(RES_DIR)
