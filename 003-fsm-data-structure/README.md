We can create the Free Space Map extension using:

```sql
CREATE EXTENSION IF NOT EXISTS pg_freespacemap;
```

Note that creating this extension is specific to a database. Creating an extension in one database does not make it available in all databases.

To find the filenames for your table, use:

```sql
select pg_relation_filepath('<table_name>');
```

To list all the contents of the free space map, use:

```sql
SELECT * FROM pg_freespace('<table_name>');
```
