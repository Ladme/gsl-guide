# Basic queries

GSL allows you to select atoms based on their attributes. Here's how you can perform basic selections:

### 1. Residue names

Select atoms belonging to residues with specific names.

- **Syntax:** `resname XYZ`
- **Example:** `resname POPE`
  
*Selects all atoms in residues named POPE.*

### 2. Residue numbers

Select atoms based on their residue numbers.

- **Syntax:** `resid XYZ` or `resnum XYZ`
- **Example:** `resid 17`
  
*Selects all atoms in residue number 17.*

### 3. Atom names

Select atoms with specific atom names.

- **Syntax:** `name XYZ` or `atomname XYZ`
- **Example:** `name P`
  
*Selects all atoms named P.*

### 4. Serial atom numbers

Select atoms based on their serial atom numbers as understood by GROMACS.

- **Syntax:** `serial XYZ`
- **Example:** `serial 256`
  
*Selects the atom with serial atom number 256.*

> **Note:** This selection is determined using GROMACS's internal atom numbering, not the numbering found in GRO or PDB files. Here, numbering starts at 1 for the first atom and increases sequentially. Each atom is guaranteed to a have a unique serial number.

### 5. GRO/PDB atom numbers

Select atoms based on their atom numbers in the originating GRO or PDB file.

- **Syntax:** `atomnum XYZ`
- **Example:** `atomnum 124`
  
*Selects all atoms with atom number 124 in the input file.*

> **Note:** There is no guarantee that one specific atom number will be assigned to exactly one atom.

### 6. Chain identifiers

Select atoms belonging to specific chains.

- **Syntax:** `chain X`
- **Example:** `chain A`
  
  *Selects all atoms in chain 'A'.*

> **Note:** Chain information is typically available in PDB files. If absent, this selection will yield no results.

### 7. Element names

Select atoms based on their element names.

- **Syntax:** `element name XYZ` or `elname XYZ`
- **Example:** `element name carbon`
  
*Selects all carbon atoms.*

> **Note:** Element information must be available. If absent, this selection will yield no results. Read more [here](notes.md/#selecting-elements).

### 8. Element symbols

Select atoms based on their element symbols.

- **Syntax:** `element symbol X` or `elsymbol X`
- **Example:** `element symbol C`
  
*Selects all carbon atoms.*

> **Note:** Element information must be available. If absent, this selection will yield no results. Read more [here](notes.md/#selecting-elements).

### 9. Labels

Select atoms using predefined labels.

- **Syntax:** `label XYZ`
  
*Labels are discussed in detail [later](labeling.md) in this tutorial.*
