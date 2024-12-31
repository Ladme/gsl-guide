# Regular expressions

GSL supports the use of regular expressions (regex).

### Using regular expressions

You can apply regex patterns to various identifiers: atom names, residue names, group names, element names, element symbols, and labels.

- **Syntax:**
  
  ```gsl
  identifier r'<pattern>'
  ```

- **Examples:**
  
  ```gsl
  name r'^[1-9]?H.*'
  ```

  *Selects all atoms with names matching the regex pattern (typically hydrogen atoms).*
  
  ```gsl
  resname r'^.*PC'
  ```

  *Selects all residues with names ending in "PC".*
  
  ```gsl
  group r'^P'
  ```

  *Selects all groups with names starting with 'P'.*

### Combining regular expressions with other identifiers

You can mix regex-based identifiers with standard identifiers in a single query.

- **Examples:**
  
  ```gsl
  name r'^C.*' and resname ALA GLY
  ```

  *Selects atoms with names starting with 'C' in residues named ALA or GLY.*

  ```gsl
  name P r'^[1-9]?H.*'
  ```
  
  *Selects atoms named 'P' and hydrogen atoms.*

### Syntax rules

- **Enclosure:**  
  The regex pattern must be enclosed within a "regular expression block" starting with `r'` and ending with `'`.

- **Case sensitivity:**  
  Regex patterns are case-sensitive unless specified otherwise within the pattern.

### Supported regex features

GSL uses the `regex` crate for evaluating regular expressions. For detailed information on supported regex features, refer to the [official documentation](https://docs.rs/regex/latest/regex/).

