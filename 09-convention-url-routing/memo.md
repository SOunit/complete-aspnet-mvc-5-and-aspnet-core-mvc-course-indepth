# avoid conflict

- these 2 routes conflict
  - `{controller}/{action}/{productName}`
  - `{controller}/{action}/{id}`

# how to solve conflict url

- literal
  - use unique url
  - have to define specific controller and action
  - `products/GetProductID/{productName}`
- constraints
  - recommended
  - use regular expression
    - if character, then use this url
