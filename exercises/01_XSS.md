# Execute XSS attack inside an Angular App

- Checkout Branch `xss` (`git checkout xss`)
- Inject following malicious JavaScript inside the `Abstract`-Input field: `<iframe src="javascript:alert('xss')">`
- Investigate the Angular Code - Do you know how the attack could happen?

