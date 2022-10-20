# agenda

- what is identity
- identity package
- identity connection string
- IdentityUser class
- IdentityDbContext class
- Identity UserStore class
- Identity UserManager class

# What is Identity

- Framework to store and manage user accounts in web applications
- 4 major components / packages
  - Microsoft.AspNet.Identity.Core
    - manage `Users` and `Roles`
  - Microsoft.AspNet.Identity.EntityFramework
    - storing `users information` in `database`
  - Microsoft.AspNet.Identity.Owin (Open Web Interface)
    - user login / logout
    - Social login
      - facebook
      - google
      - twitter
  - Microsoft.Owin.Host.SystemWeb
    - used to run `OWIN` based apps on IIS

# package to install

- EntityFramework
- Microsoft.AspNet.Identity.EntityFramework
- Microsoft.AspNet.Identity.Owin
- Microsoft.Owin.Host.SystemWeb

# connection string

# IdentityUser

- class to keep all user information
- implement IUser<TKey> interface
  - TKey represent key column in user table
    - string is default
    - int
- require `ID` and `Name` field
- can add new field by creating `ApplicationUser` extends `IdentityUser`

# IdentityDbContext

- implement `IdentityDbContext<TUser>` interface

# UserStore

- responsible for storing data to db
- implement `IUserStore<TUser, TKey>` interface

# UserManager

- changePassword
- changePhoneNumber
- confirmEmail
- createIdentity
- delete
- find
- findById
- findByName
- getEmail
- getRoles
- hasPassword
- isEmailConfirmed
- isPhoneNumberConfirmed
- isInRole
- sendEmail
- resetPassword
- removeFromRole
- update
- updatePassword
- verifyPassword
