# Retrieve Data from NASAs Exoplanet Archive

A simple interface for accessing exoplanet data. At the bare minimum, a
table name is required. Tables names are documented in the \`tableinfo\`
dataset.

## Usage

``` r
exoplanets(table, columns = NULL, limit = NULL, format = "csv")
```

## Source

<https://exoplanetarchive.ipac.caltech.edu/>

## Arguments

- table:

  A table name, see \`tableinfo\`.

- columns:

  A vector of valid column names, by default will return all default
  columns, see \`tableinfo\`.

- limit:

  Number of rows to return. If NULL, returns all data in the table.

- format:

  Desired format, either csv, tsv, or json.

## Value

A `data.frame` if `format="csv"` or `format="tsv"`. A `list` if
`format="json"`.

## Details

At one time, this package used the Exoplanet Archive Application
Programming Interface (API). Since then, a handful of tables have been
transitioned to the Table Access Protocol (TAP) service. More tables
will be transitioned to TAP and as such, this package only supports
queries from TAP. For more information, you can read
<https://exoplanetarchive.ipac.caltech.edu/docs/exonews_archive.html#29April2021.>

## See also

tableinfo

## Examples

``` r
if (interactive()) {
  # request all default columns from the `ps` table
  exoplanets("ps")

  # request the planet name and discovery method from the `ps` table
  exoplanets("ps", c("pl_name", "discoverymethod"))

  # request the first 5 rows from the `keplernames` table
  exoplanets("keplernames", limit = 5)

  # request in json format (returns list)
  exoplanets("ps", c("pl_name", "discoverymethod"), format = "json")

}
```
