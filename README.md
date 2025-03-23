# evitaLab metadata database

This repo acts as public database for different kinds of metadata that are not connected to one particular version of [evitaLab](https://github.com/lukashornych/evitalab/) or [evitaLab Desktop](https://github.com/lukashornych/evitalab-desktop).

## Contents

### evitaLab version lookup table

[`evitalab-version-lookup-table.csv`](evitalab-version-lookup-table.csv)

A lookup table used primarily by the [evitaDB Desktop](https://github.com/lukashornych/evitalab-desktop) application to find appropriate evitaLab driver version
for an evitaDB server the application is connecting to.

The table is constructed from the [`.evitadbrc`](https://github.com/lukashornych/evitalab/blob/dev/.evitadbrc) file in the evitaLab repository which represents
the oldest evitaDB server version needed for an evitaLab version.
All the evitaLab versions are then grouped by their oldest needed evitaDB version into this table and sorted from the oldest to the newest.

Thanks to this, a consumer is able to lookup the newest evitaLab version for a particular evitaDB server version by iterating over this table from the bottom and searching for the first evitaDB version that is the same or older that the looked up evitaDB version. When a suitable evitaDB version is found, the newest available evitaLab version is the last version in the evitaLab version list.

#### Columns

- `evitadb-version` - the oldest evitaDB version needed for particular list of evitaLab version
- `evitalab-versions` - all evitaLab versions that defines such evitaDB version as the oldest needed one
    - versions are delimited by `,`
