---
title: Storage
type: docs
weight: 2
# prev: /
# next: docs/folder/
---

## Declaration

```yaml
imports:
  my_storage_client:
    storage:
      # Key for the schema to use
      schema_key: my_storage_schema
      
      # Frequcency that the storage is reset
      #  - daily: storage resets at the start of each day
      #  - weekly: storage resets on monday at midnight
      #  - monthly: storage resets on the first of the month
      #  - never: storage is persisent and won't be automatically reset
      # default: daily     
      resets: daily
schemas: 
  my_storage_schema:
    type_input: object
    properties:
      property1: {}
```

## JavaScript API

### Methods

- `get()`: loads the stored data and returns it as a JSON object
- `save(data)`: saves the json object to the data store
  - `data` (object): data to save. Must be JSON serializable and a valid instance of the schema declared in `import`.

## Example

```javascript
my_storage_client.save({hello: "world"});
console.log(my_storage_client.get().hello);
```
