# Selecting molecules

GSL provides operators to select entire molecules (i.e., groups of bonded atoms) based on specific criteria.

### `molecule with` (or `mol with`) operator

- **Function:** Selects all atoms in the same molecule(s) as the atoms matching the inner query.

- **Syntax:**
  
  ```gsl
  molecule with <query>
  ```

  *Or:*

  ```gsl
  mol with <query>
  ```

- **Examples:**
  
  ```gsl
  molecule with serial 15
  ```

  *Selects all atoms in the molecule containing the atom with serial number 15.*
  
  ```gsl
  molecule with resid 4 17 29
  ```

  *Selects all atoms in molecules containing any atom from residues 4, 17, or 29.*
  
  ```gsl
  molecule with name P
  ```

  *Selects all atoms in molecules that include an atom named P.*

### Operator precedence with `molecule with`

- **Example 1:**
  
  ```gsl
  molecule with serial 15 or name BB
  ```

  *Selects atoms in the molecule containing serial 15 **+** selects atoms named BB.*

- **Example 2:**
  
  ```gsl
  molecule with (serial 15 or name BB)
  ```

  *Selects all atoms in molecules that contain either atom 15 **or** any atom named BB.*


> **Note:**
> - **Topology requirement:** The system must contain topology information to use molecule selections. Without it, no atoms will be selected. Topology information is available, for instance, in TPR files and some PDB files.

