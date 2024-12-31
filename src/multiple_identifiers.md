# Multiple identifiers

GSL allows you to specify multiple identifiers within a single query, enabling the selection of atoms matching **any** of the provided criteria.

### Examples:

- **Residue names:**
  
  ```gsl
  resname POPE POPG
  ```

    *Selects all atoms in residues named POPE or POPG.*

- **Residue numbers:**
  
  ```gsl
  resid 13 15 16 17
  ```

    *Selects atoms in residues numbered 13, 15, 16, or 17.*

- **Atom names:**
  
  ```gsl
  name P CA HA
  ```

    *Selects atoms named P, CA, or HA.*

- **Serial numbers:**
  
  ```gsl
  serial 245 267 269 271
  ```

    *Selects atoms with serial numbers 245, 267, 269, or 271.*

- **Chains:**
  
  ```gsl
  chain A B C
  ```

    *Selects atoms in chains 'A', 'B', or 'C'.*

- **Element names:**
  
  ```gsl
  elname carbon hydrogen
  ```

    *Selects all carbon and hydrogen atoms.*

- **Element symbols:**
  
  ```gsl
  elsymbol C H
  ```

    *Selects all carbon and hydrogen atoms.*
