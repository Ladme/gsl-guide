# Online GSL validator

You can easily verify the validity of your GSL query using the [online validation tool](https://ladme.github.io/gsl-validator/).

> **Note:** This tool checks only the general syntax of the query. It does not account for the specific context of your molecular system. Queries that reference non-existent groups in your system will still be considered valid syntactically but will fail during execution. The tool focuses solely on syntactical correctness and cannot interpret your intent. For example, the query `resname POPC name P` is syntactically valid but will probably not achieve the desired outcome.