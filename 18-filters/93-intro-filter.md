# filter

- execute something before or after execution of action method

# type of filters

- authentication filters
- authorization filters
- action filters
- result filters
- exception filters

# authentication filters

- check if current user is valid or not
- execute fast than other filters
- `IAuthenticationFilter`

# Authorization filters

- execute first to check authorization
- `IAuthorizationFilter`
  - manager can edit product
  - but cannot delete product

# Action Filters

- modify ViewBag before / after action method execution
- `IActionFilter`

# Result filters

- modify result
- before / after result execution
- `IResultFilter`

# Exception filters

- can store exception log
- while exception occurred
- `IExceptionFilter`

# how filter execute

- Browser

  - request to server

- IAuthenticationFilter
  - OnAuthenticate
- IAuthorizationFilter
  - OnAuthorization
- IActionFilter

  - OnActionExecute

- Execute the Action Method

- IActionFilter
  - OnActionExecuted
- IResultFilter

  - OnResultExecuting
    - can change ViewBag before rendering result

- Execute Result

- IResultFilter

  - OnResultExecuted
  - request go back to Browser

- Browser
  - receive response
