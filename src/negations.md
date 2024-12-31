# Negations

GSL allows you to exclude certain atoms from your selection using negation operators.

- **Syntax:**
  
  ```gsl
  not <query>
  ```

  *Or:*

  ```gsl
  ! <query>
  ```

- **Examples:**
  
  ```gsl
  not name CA
  ```

  *Selects all atoms **not** named CA.*
  
  ```gsl
  ! name CA
  ```

  *Equivalent to the above.*
  
  ```gsl
  not resname POPE POPG
  ```

  *Selects atoms not in residues named POPE or POPG.*
  
  ```gsl
  !Protein
  ```

  *Selects atoms not in the group named "Protein".*
