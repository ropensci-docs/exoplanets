# Clear the exoplanets cache

Forget past results and reset the `exoplanets` cache.

## Usage

``` r
forget_exoplanets()
```

## Examples

``` r
if (interactive()) {
  system.time(exoplanets("k2names"))
  system.time(exoplanets("k2names"))
  forget_exoplanets()
  system.time(exoplanets("k2names"))
}
```
