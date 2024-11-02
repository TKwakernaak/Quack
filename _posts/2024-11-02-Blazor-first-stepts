```yaml
   ---
   title: "Les 1, Blazor, routing"
   date: 2024-11-01
   ---
   ```

#Blazor hybrid 

- Routing vind in blazor plaats in routes.razor. De router in app.razor is het begin punt. 
- Het toevoegen van een @Page directive zorgt ervoor dat het mogelijk is om naar een pagina te navigeren. (deze worden opgepakt
met assembly scanning)
- Pagina's kunnen parameters ontvangen.
- De NavigationManager kan gebruikt worden voor navigatie in de code

```c#
<Router AppAssembly="@typeof(MauiProgram).Assembly">
    <Found Context="routeData">
        <RouteView RouteData="@routeData" DefaultLayout="@typeof(Layout.MainLayout)" />
        <FocusOnNavigate RouteData="@routeData" Selector="h1" />
    </Found>
</Router>
```

*AppAssembly* = parameter die definieert de assembly die moeten worden gescant met de @page e attribute
*RouteView* = navigeert het component die je wil laten zien. Hier kun je bv. de layout definieren. 


Parameters:
Kunnen worden toegevoegd, net als in ASP.net API's
/floors/{Id:int}

```c#
@code{
[Parameter]
public int Id {get;set;}
}
```c#

of inline:

```c#
@code{
[SupplyParameterFromQuery(Name="FloorId")]
public int Id {get;set;}
}
```
