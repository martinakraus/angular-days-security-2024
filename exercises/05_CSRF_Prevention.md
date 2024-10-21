# Cross-Site Request Forgery Protection in Angular

- Checkout Branch `csrf` (`git checkout csrf`)
- We need a backend in order to implement Angular CSRF-protection: `cd src/server && npm i`
- In order to make the built-in Angular CSRF-protection work we need to build `npm build` the Angular App and it needs to be delivered from our backend
- To start the Server run `npm run start` from the root directory
- In order to get a Token we need to login: username: User1 and password: password1
- Add CSRF-Prevention to you HttpClient: `provideHttpClient(withXsrfConfiguration({}))`
- Change the headerName to `x-csrf-token` inside the XsrfConfiguration
- Investigate your Requests (by Opening the Network Tap on your Browser) and make sure the XSRF-Token is send

### Hints
```typescript
//app.config.ts
providers: [
    provideHttpClient(withXsrfConfiguration({ headerName: 'x-csrf-token' })),
    provideRouter(routes, withComponentInputBinding())
]

//login.component.ts
this.http.post('/send', {}).pipe(take(1)).subscribe((res) => console.log(res));
```

[Solution](https://github.com/martinakraus/angular-security/tree/csrf-solution)
