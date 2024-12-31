# Parentheses

Parentheses allow you to control the evaluation order of your queries.

### Changing evaluation order

Use parentheses to group queries and dictate the sequence of operations.

- **Example:**
  
  ```gsl
  resname POPE or (name CA and not resid 18 to 21)
  ```

  *Selects atoms in residues named POPE **+** atoms named CA which are not in residues 18 to 21.*

- **Changing the position of parentheses:**
  
  ```gsl
  (name CA or resname POPE) and not resid 18 to 21
  ```

  *Selects atoms which are either named CA or in residues named POPE, **but are not** in residues 18 to 21.*

### Nested Parentheses

You can nest parentheses to create complex selection logic.

- **Example:**
  
  ```gsl
  serial 1 to 6 or (name CA and resname POPE || (resid 1 to 7 or serial 123 to 128)) and Protein
  ```

  *A valid, albeit complex, query that combines multiple conditions.*

### Negating Parenthetical Expressions

You can apply negation to entire parenthetical groups.

- **Example:**
  
  ```gsl
  !(serial 1 to 6 && name P)
  ```

  *Selects atoms that **do not** have serial numbers between 1 and 6 while being named P.*

