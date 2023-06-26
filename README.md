# strftime
This PHP script defines (if not exists) a `strftime()` function that is deprecated and will be removed from standard PHP functions in the future. The only thing you need to do is to load the script before everything else. In this way, it is possible to run older code work based on `strftime()` function on PHP version that doesn't support it without modifying your code.

The script uses two methods to get the text:

- using shell command;
- using `IntlDateFormatter` class and additional processing.

The choice between these two methods is automatic. The first method is used if the system allows execution of shell commands and it is the more reliable option. The second method is not complete. I'm having trouble finding a solution for the `%V`, `%g`, `%G`, `%X`, `%c`, `%x` tags.
