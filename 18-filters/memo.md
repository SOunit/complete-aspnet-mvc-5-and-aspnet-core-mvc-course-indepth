- filter is like lifecycle method in React
- you can add some logic to each phase of lifecycle

# filter execution flow

- IAuthenticationFilter.IAuthentication
- IAuthorizationFilter.IAuthorization
- IActionFilter.OnActionExecuting
- Action Method
- IActionFilter.OnActionExecuted
- IResultFilter.OnResultExecuting
- Result Execution
- IResultFilter.OnResultExecuted

- IExceptionFilter.OnException
