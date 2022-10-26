# steps

- ASP.NET v5s
- not core

# install packages

```
install-package Microsoft.AspNet.Identity.EntityFramework
install-package Microsoft.AspNet.Identity.Owin
install-package Microsoft.Owin.Host.SystemWeb
```

# create startup file

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

# create classes

- ApplicationUser
  - represent data structure in db
- ApplicationDbContext
- ApplicationUserStore
- ApplicationUserManager

# create a folder

- root / `Identity`

# create ApplicationUser class

- inherit `IdentityUser`
  - have these properties
    - Email
    - UserName
    - Password
    - etc
- can add your own properties

# Add Connection String

- `Web.config`

# ApplicationDbContext

- Identity/ApplicationDbContext

# Enable Migration

```
Enable-Migrations -ContextTypeName AspNetIdentitySample.Identity.ApplicationDbContext -MigrationsDirectory IdentityMigrations
```

# Error Fix

## connectionString

- copied from Official Document

  ```
  <add name="MyConnectionString"
    connectionString="Data Source=DESKTOP-VBED2PD;Initial Catalog=Company;Integrated Security=SSPI;"
    providerName="System.Data.SqlClient" />
  ```

## Enable Migration Error

- url
  https://stackoverflow.com/questions/41777590/entity-framework-value-cannot-be-null-parameter-name-type
- solution
  - upgrade EF from 6.1 to 6.4

# add migration

```
add-migration -configuration AspNetIdentitySample.IdentityMigrations.Configuration Initial
```

- Tables
  - AspNetRoles
  - AspNetUserRoles
  - AspNetUsers
  - AspNetUserClaims
  - AspNetUserLogins

# update database

- `update-database -Configuration AspNetIdentitySample.IdentityMigrations.Configuration`
