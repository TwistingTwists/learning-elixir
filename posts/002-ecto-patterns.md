What is behaviour in elixir?

Why use it?

Leveraging Behaviour in Elixir to write ecto queries 

`Queryable` Behaviour 

```elixir
@callback base_query(Struct) :: Ecto.Query.t()
@callback sort_by(Ecto.Query.t(), map(), Warehouse.Facility.User.t()) :: Ecto.Query.t()
@callback filter_by(Ecto.Query.t(), map(), Warehouse.Facility.User.t()) :: Ecto.Query.t()
```

1. filters - Enum.reduce 
2. base_query --- base filters, tenants, building_ids , is_nil(deleted_at)
3. sort_by - Enum.reduce