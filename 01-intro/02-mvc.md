# What is ASP.NET MVC

- Web Application Framework
- MVC pattern
- separation of concern
- full control over markup

# old one

- `ASP.NET WebForms` Framework
  - old one
  - no clean separation of concerns
  - server side too heavy
    - post backs
    - page life cycle
    - slower performance

# Main Advantage

- clean separation of concerns

  - Model
  - View
  - Controller

- Faster performance
  - no server control
    - deleted
      - page-life-cycle
      - view-state
      - etc

# ASP.NET

- ASP.NET MVC
- ASP.NET Web API

# What is MVC

- architecture pattern
  - Model
    - Data Structure
    - Business Logic
  - View
    - Presentation Logic
    - read data from model
  - Controller
    - define execution flow
    - start from controller
    - fill data into model
    - pass model to view

# advantage

- support clean separation of concerns
- support unit testing
- support dependency injection
  - use configuration file
  - DI is just pass objet
- faster than `ASP.NET Web Forms`
- no page-life-cycle, controls, post-back and view-state
