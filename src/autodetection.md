# Selecting atoms by autodetection

GSL offers macros that automatically detect and select common molecular components. These macros simplify selections without needing to specify detailed criteria. GSL macros support atomistic, united-atom, and coarse-grained systems.

### Available macros:

- `@protein`: Selects all amino acid atoms (supports ~140 different amino acids).
- `@water`: Selects all water atoms.
- `@ion`: Selects all ion atoms.
- `@membrane`: Selects membrane lipid atoms (supports over 200 lipid types).
- `@dna`: Selects all DNA molecule atoms.
- `@rna`: Selects all RNA molecule atoms.

### Example usage:

```gsl
@protein or @membrane
```

*Selects all protein and membrane lipid atoms.*

> **Caution:** While these macros are generally reliable, they may not always perfectly identify all relevant atoms. Use them judiciously, especially when working with custom molecules.
