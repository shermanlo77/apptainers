# apptainers

Example Apptainer definition files for Python and R

## `python.def`

- `export PYTHONNOUSERSITE=1` ensures packages in the home directory are not
   read

## `R.def`

- `export R_LIBS_USER=""` ensures packages in the home directory are not
   read
- `export DEBIAN_FRONTEND="noninteractive"` and
  `export DEBCONF_NONINTERACTIVE_SEEN=true` ensures no user input during
  installation. For example, R may ask the user for a time zone.

## `R-devtools.def`

Definition file for R with `devtools`

## `R_v3.2.2.def`

Definition file for R `v3.2.2` with the packages `iterators` `v1.0.8`, `foreach`
`v1.4.3` and `glmnet` `v2.0-2`. This definition file builds R from source and
ubuntu `v14.04.1`.

This came about because the official R docker images are based on Debian
testing, which makes it difficult to do commands like `apt update`.
