# Binary operations

GSL supports combining multiple queries using logical operators to refine selections further.

### Logical AND

- **Operators:** `and` or `&&`
- **Function:** Selects atoms that satisfy **both** queries.

- **Examples:**
  
  ```gsl
  name P and resname POPE
  ```

  *Selects atoms named P in residues named POPE.*

  ```gsl
  serial 256 to 271 && resid 17 18
  ```

  *Selects atoms with serial numbers between 256 and 271 in residues 17 or 18.*

### Logical OR

- **Operators:** `or` or `||`
- **Function:** Selects atoms that satisfy **at least one** of the queries. Can be understood as an addition (**+**) operation.

- **Examples:**
  
  ```gsl
  name P or resname POPE
  ```

  *Selects atoms named P **+** atoms in residues POPE.*

  ```gsl
  resid 17 18 || serial 256 to 271
  ```

  *Selects atoms in residues 17 or 18 **+** atoms with serial numbers between 256 and 271.*

### Operator precedence

When combining multiple `and` and `or` operators, GSL evaluates them from **left to right**.

- **Example:**
  
  ```gsl
  resname POPE or name CA and not Protein
  ```

  *Interpreted as:*  
  *(resname POPE **or** name CA) **and not** Protein*

  *Selects atoms in residues named POPE **+** atoms named CA **−** (minus) atoms that are part of the "Protein" group.*

### Combining with autodetection macros

You can mix autodetection macros with other queries using logical operators.

- **Example:**
  
  ```gsl
  @membrane or group 'My Lipids'
  ```

  *Selects all autodetected membrane lipids **+** atoms in the "My Lipids" group.*

