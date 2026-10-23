# Project 2 — Snowflake Data Warehouse & Incremental Loading

## What it demonstrates
- Separate staging and analytics schemas
- A staging table and analytics dimension table
- Snowflake Stream to capture changes
- `MERGE` for insert/update (upsert) logic
- Optional Task that runs when stream data is available

## How to run
1. Open a Snowflake worksheet with a role allowed to create databases, schemas, tables, streams, and tasks.
2. Review `data_warehouse.sql`; replace `COMPUTE_WH` with a warehouse available to your role.
3. Run the SQL statements in order.
4. Check `DE_PROJECT.ANALYTICS.DIM_CUSTOMERS`.
5. Insert the sample updated customer and run the MERGE again to test incremental updates.
6. To enable automation, uncomment the `ALTER TASK ... RESUME` statement after checking privileges.

## Important
- The SQL is a learning/portfolio template and has not been executed against your Snowflake account.
- Stream offset advances when a transaction consumes the stream; avoid committing exploratory DML against the stream.
- Task execution requires a suitable warehouse and privileges.
- Confirm actual behavior in your own Snowflake environment before listing project outcomes or performance metrics on a resume.
