![Build CSV Output Files](https://github.com/ktower/acb-config/workflows/Build%20CSV%20Output%20Files/badge.svg)
# acb-config Introduction
My Anytone DMR configuration files

These files are meant to be fed into K7ABD's Anytone Config Builder (ACB), 
available https://github.com/K7ABD/anytone-config-builder or https://www.k7abd.net/anytone-config-builder/

# Building
## Via the web
Browse to [K7ABD's website](https://www.k7abd.net/anytone-config-builder/) and submit the `.csv` files there.  Click "Upload" to process, and expect to immediately download a ZIP file with the results.

## Via CLI
### Requirements
Before running the ACB script, the `libtext-csv-perl` package (Ubuntu) must be installed.

### Executing
The following command probably will work:
```
anytone-config-builder.pl \
  --analog-csv=./analog.csv \
  --digital-others-csv=./digital-others.csv \
  --digital-repeaters-csv=./digital-repeaters.csv \
  --talkgroups-csv=./talkgroups.csv \
  --output-directory=wherever \
  --nicknames=prefix
```

# Important Notes
# lf vs crlf
The ACB utility expects all .csv input files to have crlf line endings, not
just lf.  Otherwise the program will run to completion without any error
but the output files will not have anything other than a header line.

