# Labeling atoms

If atoms are labeled (using [`System::label_atom`](https://docs.rs/groan_rs/latest/groan_rs/system/struct.System.html#method.label_atom)), you can use these labels in your GSL queries.

- **Syntax:**
  
  ```gsl
  label XYZ
  ```

- **Examples:**
  
  ```gsl
  label MyAtom
  ```

  *Selects the atom labeled "MyAtom".*
  
  ```gsl
  label MyAtom AnotherAtom OneMoreAtom
  ```

  *Selects atoms labeled "MyAtom", "AnotherAtom", and "OneMoreAtom".*

### Labels with multiple words

For labels consisting of multiple words, enclose them in quotes.

- **Example:**
  
  ```gsl
  label 'Very interesting atom'
  ```

  *Selects the atom labeled "Very interesting atom".*

> **Comparison with groups:**  
> Labels are similar to groups but are guaranteed to contain **only one atom** each.

