# Important notes

### Selecting Elements

- **Element assignment:**  
  Atoms in the system **are not** automatically assigned elements by `groan_rs` unless the elements are explicitly specified in the input structure file. *This is because elements may not always be meaningful, particularly in coarse-grained systems.*

- **Using `element` keywords:**  
  To use `element name` or `element symbol` in your selections, ensure that atoms have been assigned elements.

- **Assigning elements:**
  - **From topology files:** Creating the `System` structure from a TPR file automatically assigns elements.
  - **Guessing elements:** Use the [`System::guess_elements`](https://docs.rs/groan_rs/latest/groan_rs/system/struct.System.html#method.guess_elements) function to assign elements based on atom names.

- **Recommendation:**  
  If you're using a program that utilizes GSL, ensure that it assigns elements to atoms before using `element` keywords in selections.

### Whitespace considerations

- **Operator and parenthesis separation:**  
  Operators (`and`, `or`, `not`, etc.) and parentheses do **not** need to be separated by whitespace unless it affects query clarity.

- **Valid example:**
  
  ```gsl
  not(name CA)or(serial 1to45||Protein)
  ```
  
  *A valid query without (unnecessary) whitespace.*

- **Invalid example:**
  
  ```gsl
  not(name CA)or(serial 1to45orProtein)
  ```
  
  *Invalid because `orProtein` is unclear.*

- **Resolving ambiguity:**
  
  Enclose ambiguous parts in parentheses to clarify intent. **Or use whitespace, it is worth it.**
  
  ```gsl
  not(name CA)or(serial 1to45or(Protein))
  ```
  
  *Now, the query is valid and interpretable, but not very human-readable.*
