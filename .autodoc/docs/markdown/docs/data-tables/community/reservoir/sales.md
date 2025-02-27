[View code on GitHub](https://dune.com/docs/data-tables/community/reservoir/sales.md)

# Sales

This section of the app technical guide covers the `reservoir.sales` table, which contains records with information about each sale. The table includes various columns such as `id`, `contract`, `token_id`, `order_id`, `order_kind`, `order_side`, `order_source`, `from`, `to`, `price`, `usd_price`, `currency_address`, `currency_symbol`, `currency_price`, `amount`, `fill_source`, `aggregator_source`, `wash_trading_score`, `is_primary`, `tx_hash`, `tx_log_index`, `tx_batch_index`, `tx_timestamp`, `created_at`, and `updated_at`.

The purpose of this guide is to provide an overview of the `reservoir.sales` table and its columns, as well as query examples that can be used to retrieve data from the table. The guide also includes a description of each column, its data type, and its purpose.

For example, the `id` column contains the internal sale id, while the `contract` column contains the contract address. The `price` column contains the sale price in the native currency, while the `usd_price` column contains the sale price in USD. The `amount` column contains the amount of tokens sold, while the `is_primary` column indicates whether the sale is a paid mint.

The guide also includes query examples that can be used to retrieve data from the `reservoir.sales` table. These examples demonstrate how to use the `SELECT` statement to retrieve specific columns from the table, as well as how to use the `WHERE` clause to filter the results based on specific criteria.

Overall, this section of the app technical guide provides a comprehensive overview of the `reservoir.sales` table and its columns, as well as query examples that can be used to retrieve data from the table.
## Questions: 
 1. What is the purpose of the `reservoir.sales` table in the context of blockchain? 
- The `reservoir.sales` table contains records with information about each sale in the blockchain context.

2. What is the significance of the `currency_address` and `currency_symbol` columns in the `reservoir.sales` table? 
- The `currency_address` and `currency_symbol` columns in the `reservoir.sales` table indicate the currency used for a particular sale in the blockchain context.

3. How is the `wash_trading_score` column calculated in the `reservoir.sales` table? 
- The `wash_trading_score` column in the `reservoir.sales` table is calculated based on past sales and indicates the internal wash trading score in the blockchain context.