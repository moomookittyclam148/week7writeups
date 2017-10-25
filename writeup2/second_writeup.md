1. Write up
  There is a vulnerability in Wordpress where if a user uploaded a file that was larger that 20 megabytes and the name of the file contained an XSS script. You would receive error stating that the file was too larger followed by the execution of the script.

2. Proof of Concept
  Any file that is over 20 megabytes and contains an XSS script inside of the name of the file, such as <img src=x onerror=alert(1)>

3. Class of vulnerability
  CVE-2017-9061
  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-9061

4. Vulnerable Versions
  Confirmed vulnerable: WordPress <= 4.2.14
