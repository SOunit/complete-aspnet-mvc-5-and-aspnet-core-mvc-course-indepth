# action result

- represents `result of action an action method`
- ASP.NET recommend use `ActionResult` for action method return type

# merit of using ActionResult

- can receive request from browser
- can return any action-result class conditionally
  - view
  - file
  - etc.

# ActionResult

- ContentResult
- ViewResult
- FileResult
- PartialViewResult
- RedirectResult
- RedirectToRouteResult
- JsonResult

# class

# ContentResult

- use this to return string, etc.
- return plain text / custom information to browser
  - receive `employeeId`, return `employeeName` as string

# ViewResult

- represent result of view

# FileResult

- send file
  - `PDF`

# JsonResult

- send json

# RedirectResult

- redirection to other website (HTTP 302)

# RedirectToRoute

- redirect to specific ActionMethod (HTTP 302)

# PartialViewResult

- return partial view

# method

# ContentResult

- Content(string Content, string ContentType)

# ViewResult
