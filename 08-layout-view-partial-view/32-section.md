# section

- define data in page

```
@section SideBarOptions
{
    <a href="#" class="list-group-item text-white"
       style="background-color: transparent;">Admin Home</a>
    <a href="#" class="list-group-item text-white"
       style="background-color: transparent;">Agent Home</a>
    <a href="#" class="list-group-item text-white"
       style="background-color: transparent;">Customer Home</a>
}
```

- use data in layout

```
@RenderSection("SideBarOptions")
```
