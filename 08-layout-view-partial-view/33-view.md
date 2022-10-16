# \_ViewStart.cshtml

- default layout view for all the views of a folder

# folder structure

- Views
  - Controller1
    - View1.cshtml
    - View2.cshtml
    - \_ViewStart.cshtml
  - \_ViewStart.cshtml

# execution flow

- controller
- \_ViewStart.cshtml in Views folder
- \_ViewStart.cshtml in Views/ControllerName folder
- View
- Layout View
- Generate View Result
- Response
