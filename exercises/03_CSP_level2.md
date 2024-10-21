# Content-Security-Policy Level 2

### CSP Hashes
- This is a follow up task for the Branch `csp` (`git checkout csp`) (No need to checkout a new branch)
- In index.html, declare an arbitrary inline scripting : `<script>document.write('<h1>Inline scripting is <b>not recommended</b>! But if you have not the choice, <b>secure your app with CSP</b></h1>');</script>`
- Update the CSP in order to allow this inline scripting securely (consider CSP3 SHA-256 hash syntax)

### Hints

- To generate the hash of the script content, use this online tool : [Report-Uri Hash](https://report-uri.com/home/hash) (beware of spaces and carriage returns...)

```html

<meta http-equiv="content-security-policy" content="...
    script-src 'self' 'sha256-lK+Y3vDnNUrD/ZPLGsnM6B+euoBxZ/MyiIbY2G5VoPw=';
    ...."/>
```


[Solution](https://github.com/martinakraus/angular-security/tree/csp-hashes-solution)
