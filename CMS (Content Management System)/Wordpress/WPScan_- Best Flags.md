## [WPScan - Best Flags](https://github.com/wpscanteam/wpscan)

```bash
wpscan --url https://www.000webhost.com/blog --api-token EpgVU5y0FBIGnUSlKIwGvCu6F86ujEHi7MhqFYjrss4 --plugins-detection mixed -e vp,vt,cb,dbe,u1-10 --force
```

`wpscan`: This is the command to run the WPScan tool, a black box WordPress vulnerability scanner.

`--url https://example[.]com`: This specifies the URL of the WordPress website that you want to scan.

The --api-token <api token> provides authentication with the WPScan API and allows real-time access to WPScan's frequently updated vulnerability database.

`--plugins-detection mixed`: The "mixed" mode will use both passive and aggressive methods for a more thorough scan.

`--force`: This forces WPScan to scan the target website, even if it doesn't think it's a Wordpress site.

- vp: Vulnerable plugins
- vt: Vulnerable themes
- cb: Config backups
- dbe: Database exports
- u1-10: Users with IDs ranging from 1 to 10


*Credit:-* https://twitter.com/TakSec/status/1671202550844993543?s=20
