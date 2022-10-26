# link

- `@Url.Action("Action", "Controller")`
  - `@Url.Action("Create", "Products")`
  - recommended approach
  - `/products/create` do not work on deploy?

# model binding

- add `name` to input tag

# render flow

- request
- view
- layout

# filter flow

- IAuthenticationFilter.IAuthentication
- IAuthorizationFilter.IAuthorization
- IActionFilter.OnActionExecuting
- Action Method
- IActionFilter.OnActionExecuted
