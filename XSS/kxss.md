# Find XSS in bulk via KXSS 🧙‍♂️

1. Collecting all the domains that on scope.
2. running Subfinder and assetfinder and combine the following subdomains in one list and remove duplicates
```
subfinder -dL domains.txt -o subfider-subdomains.txt
cat domain_list.txt | assetfinder --subs-only > assetfinder-subdomains.txt
cat subfinder-subdomains.txt assetfinder-subdomains.txt > subdomains.txt
sort -u subdomains.txt > sort.txt
```
3. we need to use Httpx to quickly and efficiently identify URLs that return a status code of 200 for a given domain list.
```
cat sort.txt | httpx -mc 200 > 200_urls.txt
```
4. Running Paramspider for crawling all the paramaters.
```
for URL in $(</root/recon/target/200_urls.txt); do (python3 paramspider.py -d "${URL}");
done
```
5. running KXSS for identifying the filtered , unfiltered Sympols note that Kxss scan could take several minutes or longer. Be patient and wait for the scan to complete
```
cat filtered_urls.txt | kxss
```
