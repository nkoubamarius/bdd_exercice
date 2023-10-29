# TP2

- Define an object

```
    set @json='
    [
        {"name":"Laptop", "color":"black", "price":"1000"},
        {"name":"Jeans", "color":"blue"}
    ]';
```

- SELECT all columns

```
    select * from json_table(@json, '$[*]'
    columns(
    name varchar(10) path '$.name',
    color varchar(10) path '$.color',
    price decimal(8,2) path '$.price' )
    ) as jt;
```

- Define ids for all the rows

```
select * from json_table(@json, '$[*]'
columns(
id for ordinality,
name varchar(10) path '$.name')
) as jt;
```

- SHOW rows with price information defined

```
select * from json_table(@json, '$[*]'
columns(
name varchar(10) path '$.name',
has_price integer exists path '$.price')
) as jt;

```

