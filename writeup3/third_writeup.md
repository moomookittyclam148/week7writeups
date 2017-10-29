1. Write up
  There is a vulnerability in Wordpress where a user could use a specially formatted HTML tag to insert a XSS script into a post, to which the script is then activated running malicious code.(Example through mouse over)

2. Proof of Concept
  Place this script anywhere in the post or page.
  <a href="[caption code=">]</a><a title=" onmouseover=alert('XSS')  ">link</a>

3. Class of vulnerability
  CVE-2015-2213
  https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-2213

4. Vulnerable Versions
  Confirmed vulnerable: WordPress <= 4.0.5
