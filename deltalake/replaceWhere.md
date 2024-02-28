# replaceWhere 

> Selective overwrites to a delta table 

`replaceWhere` allows to one to make idempotent writes to a delta table via a specified condition.

It will still write to the delta table specified and if the replace condition does not match.


Example: 
- If the DataFrame has more events with a different process date it will write those records to the delta table and overwrite data with the process date of `2024-02-27`

```python
(
    df
        .write
        .format("delta")
        .mode("overwrite")
        .option("replaceWhere", "process_date = '2024-02-27'")
        .save("/tmp/delta/events")
)
```