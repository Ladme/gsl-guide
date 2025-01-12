# Selecting atoms using groups

GSL allows you to select atoms using the previously constructed groups of atoms.

### Creating groups

Before selecting using groups, you must construct them. This is typically done within your workflow or by loading predefined groups, e.g. [from NDX files](#loading-groups-from-ndx-files).

### Selecting groups

- **Syntax:**
  
  ```gsl
  group GroupName1 GroupName2
  ```

  *Or simply:*

  ```gsl
  GroupName1 GroupName2
  ```

- **Example:**
  
  ```gsl
  Protein Membrane
  ```

  *Selects all atoms in the groups named "Protein" and "Membrane".*

> **Important:** If a specified group does not exist, an error will be raised.

### Loading groups from NDX files

If you've loaded an NDX file using [`System::read_ndx`](https://docs.rs/groan_rs/latest/groan_rs/system/struct.System.html#method.read_ndx), you can utilize groups defined within that file.

> **Note:** If a program using `groan_rs` loads an NDX file, you will typically be able to select groups defined in the NDX file.

### Groups with multiple words

For groups with names comprising multiple words, enclose the group name in quotes.

- **Example:**
  
  ```gsl
  Protein 'My Lipids'
  ```

  *Selects atoms in the "Protein" group and the "My Lipids" group.*
