# evitaLab metadata database

This repo acts as public database for different kinds of metadata that are not connected to one particular version of [evitaLab](https://github.com/lukashornych/evitalab/) or [evitaLab Desktop](https://github.com/lukashornych/evitalab-desktop).

## Contents

### evitaLab version lookup table

[`evitalab-database.csv`](evitalab-database.csv)

A lookup table used primarily by the [evitaDB Desktop](https://github.com/lukashornych/evitalab-desktop) application to find appropriate evitaLab driver version
for an evitaDB server the application is connecting to.

The table is constructed from published evitaLab release metadata.

#### Columns

- `evitalab-version` - release evitaLab version
- `min-evitadb-version` - the oldest evitaDB version needed for particular evitaLab version (constructed from the [`.evitadbrc`](https://github.com/lukashornych/evitalab/blob/dev/.evitadbrc))
