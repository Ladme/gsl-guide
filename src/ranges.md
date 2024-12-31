# Ranges

GSL allows you to specify ranges of residue or atom numbers.

### Specifying ranges

- **Using `to`:**
  
  ```gsl
  resid 14 to 20
  ```

  *Selects atoms in residues numbered 14 through 20 (including 20).*

- **Using `-`:**
  
  ```gsl
  resid 14-20
  ```

  *Equivalent to `resid 14 to 20`.*

### Combining with multiple ranges and numbers

You can mix explicit numbers with ranges for more complex selections.

- **Example:**
  
  ```gsl
  serial 1 3 to 6 10 12-14 17
  ```

  *Expands to selecting serial numbers 1, 3, 4, 5, 6, 10, 12, 13, 14, and 17.*

### Open-ended ranges

GSL supports open-ended ranges using comparison operators.

- **Operators:**
  - `<` : Less than
  - `>` : Greater than
  - `<=`: Less than or equal to
  - `>=`: Greater than or equal to

- **Examples:**
  
  ```gsl
  serial <= 180
  ```

  *Selects all atoms with serial numbers ≤ 180.*
  
  ```gsl
  resid > 33
  ```

  *Selects atoms in residues numbered 34 and above.*

### Combining open-ended and explicit selections

- **Example:**
  
  ```gsl
  serial 1 3-6 >=20
  ```

  *Selects atoms with serial numbers 1, 3, 4, 5, 6, and 20 or higher.*

