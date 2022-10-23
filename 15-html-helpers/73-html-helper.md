# html helper

- connect model to html
- recommended to use

# items

- Html.ActionLink
  - hyper link
- Html.TextBoxFor
- Html.TextAreaFor
- Html.CheckBoxFor
- Html.RadioButtonFor
- Html.RadioButtonFor
- Html.DropDownListFor
- Html.ListBoxFor
  - multi-select listbox
- Html.HiddenFor
- Html.PasswordFor
- Html.DisplayFor
  - plain text
- Html.LabelFor
- Html.EditorFor
  - textbox
  - textarea
  - numericTextBox
  - date textBox
  - etc.

# strong typed html helper vs. normal html helper

- strong typed html helper
  - `xxxFor`
  - use this when model bound
  - automatic setting for
    - type
    - name
    - id
- normal html helper
  - used when no model bound

# sample

- `Html.ActionLink("Link Text", "Action Name", route value)`
- `Html.ActionLink("Details", "Details", new {id = item.ProductId, controller = "Products"})`
