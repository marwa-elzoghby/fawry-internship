# fawry-internship-marwa
# fawry-internship-marwa
## Q1 : Custom Command ( mygrep.sh )
### Reflective Section
#### 1. How does your script handle arguments and options ?
- I used getopts to parse command-line options (-n, -v) .
- The script sets flags (show_line_numbers and invert_match) based on the options .
- After parsing options, it shifts positional arguments and checks that both a search string and filename are provided .
- It validates if the given file exists .
- Based on the flags, it either shows matching lines normally, shows line numbers, or inverts the match .


#### 2. How would the structure change if regex or -i/-c/-l options were added ?
- For regex, I would replace the simple grep check with an extended regex match (grep -E) or shell pattern matching ([[ $line =~ $pattern ]]) .
- For -i (ignore case), the structure would not change because case-insensitive search is already done using grep -i .
- For -c (count matches), I would add a counter variable that increments on each match and print the count at the end .
- For -l (list filenames), I would only print the filename once if there is at least one match instead of printing lines .
- I would modularize the script into small functions to make it easier to maintain when adding more options .

#### 3. What part of the script was hardest to implement and why?
- The hardest part was correctly parsing options (-v, -n, combinations like -vn) .
- Ensuring the logic for inverted matches with line numbers was tricky, especially when combining both options .
- Using getopts and shifting positional parameters cleanly also required careful handling to avoid wrong arguments .


#### Bonus Features
- Added support for `--help` flag to print usage instructions .
- Improved command-line option parsing using `getopts` for cleaner and more efficient handling of `-n` and `-v` options .

#### Screenshots
- See folder `Question1/`.

## Q2 - Internal Service Unreachable ( Troubleshooting internal.example.com )
1. Verified DNS with dig (local and 8.8.8.8)
2. Diagnosed service with curl and telnet
3. Listed possible causes
4. Applied fixes for DNS, firewall, services
5. Bonus: Used /etc/hosts and systemd-resolved

### Screenshots
- See folder `Question2/`.
