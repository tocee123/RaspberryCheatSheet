# Search criteria
[link](https://raspberrytips.com/find-file-raspberry-pi/)
## Example 
find files, that end with `sql` and older than 40 minutes
`find ~ -type f -name "*.sql" ! -cmin -40`
find files, that end with `sql` and younger than 40 minutes
`find ~ -type f -name "*.sql" -cmin -40`
