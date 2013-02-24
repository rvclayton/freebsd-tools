# FreeBSD tools

Tools to maintain freebsd gardens.

`apply-updates` Apply previously fetched patches and port updates.  Output goes
to `std-out` and `std-err`; a copy of the output goes to the file named by the
environment variable `LOG_FILE` (default `/var/log/apply-updates.log`).

`fetch-updates` Fetch patches and port updates.  By default uses `cron` (random
delayed) fetching; give the `-n` command-line option to fetch with no delay.
Output goes to `std-out` or `std-err`.  If the `testing` environment variable
is non-empty, print the script commands as executed (`sh -x`) and do not do the
fetches.

These commands are based on code found at [mebsd.com](
https://mebsd.com/freebsd-security-hardening/simple-script-for-keeping-freebsd-upto-date.html).
