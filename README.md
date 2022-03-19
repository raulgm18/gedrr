# gedrr
# Install released version from CRAN
install.packages("pkgdown")
# Run once to configure your package to use pkgdown
usethis::use_pkgdown()
pkgdown::build_site()
usethis::use_pkgdown_github_pages()
url: https://pkgdown.r-lib.org
template:
  bootstrap: 5
  bootswatch: cerulean
lang: es
reference:
- title: "Connecting to Spark"
  desc: >
    Functions for installing Spark components and managing
    connections to Spark
  contents: 
  - spark_config
  - spark_connect
  - spark_disconnect
  - spark_install
  - spark_log
- title: "Reading and Writing Data"
  desc: "Functions for reading and writing Spark DataFrames."
  contents:
  - starts_with("spark_read")
  - starts_with("spark_write")
  - matches("saveload")
