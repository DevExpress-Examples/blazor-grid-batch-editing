<!-- default badges list -->
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T1217239)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->
# Grid for Blazor – How to enable batch data editing

This example demonstrates how to implement batch data editing in the [DevExpress Blazor Grid](https://docs.devexpress.com/Blazor/403143/grid) component.

![Batch Editing in DevExpress Blazor Grid](/images/batch-editing.gif)

The example uses [DbContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.dbcontext?view=efcore-8.0) to obtain and update Grid data. When a user creates a new row or modifies/deletes an existing row, a [DbContext](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.dbcontext?view=efcore-8.0) instance tracks changes. The user can press **Save** to save all changes made in this context or press **Cancel** to dispose this context and discard accumulated changes.

The [CustomizeElement](https://docs.devexpress.com/Blazor/DevExpress.Blazor.DxGrid.CustomizeElement) event's handler uses the [DbContext.ChangeTracker](https://learn.microsoft.com/en-us/dotnet/api/microsoft.entityframeworkcore.dbcontext.changetracker?view=efcore-8.0#microsoft-entityframeworkcore-dbcontext-changetracker) property to identify and highlight modified cells.

## Files to Review

* [Weather.razor](./CS/BatchEditing/BatchEditing/Components/Pages/Weather.razor)
* [Weather.razor.css](./CS/BatchEditing/BatchEditing/Components/Pages/Weather.razor.css)

## Documentation

- [Cell Editing in Blazor Grid](https://docs.devexpress.com/Blazor/404756/components/grid/editing-and-validation/edit-modes/edit-cell)
- [Edit Model in Blazor Grid](https://docs.devexpress.com/Blazor/404759/components/grid/editing-and-validation/edit-model)

## More Examples

- [How to bind the component to data with Entity Framework Core](https://github.com/DevExpress-Examples/blazor-dxgrid-bind-to-data-with-entity-framework-core)
- [How to enable inline data editing](https://github.com/DevExpress-Examples/blazor-grid-row-editing)
