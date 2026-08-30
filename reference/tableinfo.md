# Table Information

This dataset provides table information for NASA's Exoplanet Archive TAP
service. In particular, the table name, columns, and column descriptions
are provided.

## Usage

``` r
tableinfo
```

## Format

An object of class `tbl_df` (inherits from `tbl`, `data.frame`) with 546
rows and 13 columns.

## Source

<https://exoplanetarchive.ipac.caltech.edu/docs/TAP/usingTAP.html>

## Examples

``` r
tableinfo
#> # A tibble: 546 × 13
#>    table database_column_name table_label           description      in_ps_table
#>    <chr> <chr>                <chr>                 <chr>            <lgl>      
#>  1 ps    default_flag         Default Parameter Set Boolean flag in… TRUE       
#>  2 ps    soltype              Solution Type         Disposition of … TRUE       
#>  3 ps    pl_controv_flag      Controversial Flag    Flag indicating… TRUE       
#>  4 ps    pl_name              Planet Name           Planet name mos… TRUE       
#>  5 ps    hostname             Host Name             Stellar name mo… TRUE       
#>  6 ps    pl_letter            Planet Letter         Letter assigned… TRUE       
#>  7 ps    hd_name              HD ID                 Name of the sta… TRUE       
#>  8 ps    hip_name             HIP ID                Name of the sta… TRUE       
#>  9 ps    tic_id               TIC ID                Name of the sta… TRUE       
#> 10 ps    gaia_id              GAIA ID               Name of the sta… TRUE       
#> # ℹ 536 more rows
#> # ℹ 8 more variables: in_ps_comp_pars_table <lgl>,
#> #   uncertainties_column_positive_negative <chr>, limit_column <chr>,
#> #   default <lgl>, notes <chr>, displayed_string_name <chr>, flag_column <lgl>,
#> #   number_of_measurements <lgl>
```
