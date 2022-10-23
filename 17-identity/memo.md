# steps

- ASP.NET v5s
- not core

# install packages

```
install-package Microsoft.AspNet.Identity.EntityFramework
install-package Microsoft.AspNet.Identity.Owin
install-package Microsoft.Owin.Host.SystemWeb
```

- create owin startup class
  - add on project, select `Web/OWIN Startup class`, `Startup.cs`
  - add config
    ```
    public void Configuration(IAppBuilder app)
    {
        // For more information on how to configure your application, visit https://go.microsoft.com/fwlink/?LinkID=316888
        app.UseCookieAuthentication(new CookieAuthenticationOptions()
        {
            AuthenticationType = DefaultAuthenticationTypes.ApplicationCookie,
            LoginPath = new PathString("/Account/Login"),
        });
    }
    ```
