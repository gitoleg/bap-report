The readme is under construction,
but proposed usage of this tool is either of the next ways:

- ` bap-report --artifacts=/bin/echo,wpa_cli-2.2 --recipes=defective-symbol,jpl-rule-14`
  this will generate the file `results.html` with the results of applying
  of recipes `defective-symbol` and `jpl-rule-14`  to the artifacts `/bin/echo` and `wpa_cli-2.2`.
  Note, that the first artifact will be taken from the host machine, while the second
  one will be found in `bap-artifacts` docker repository

- `bap-report --from-config=<path>`
  reads a configuration from config file at `path`.
  the example of config file:
  ```
  (/bin/echo   (av-rule-174))
  (wpa_cli-2.2 (defective-symbol))
  (/bin/echo   (defective-symbol jpl-rule-14))
  ```
  this will generate the file `results.html`  with the results of applying
  of recipes `av-rule-174`, `defective-symbol` and `jpl-rule-14` to the
  artifact `/bin/echo`
  and of recipe `defective-symmbol` to the artifact `wpa-clie-2.2`.
