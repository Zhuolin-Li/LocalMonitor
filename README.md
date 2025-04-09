# LocalMonitor

## Server Setup

1. create a SQL database with schema named "client_data",2 tables named "positions" and "assets"

2. for "positions" table, it has these columns:
   
     id(INT), username(VARCHAR), account(VARCHAR), code(VARCHAR), cost(FLOAT),current_price(FLOAT),qty(INT),datetime(VARCHAR).
     
     id is the primary key and should be unique and non null
   
4. for "assets" table, it has these columns:
     
     id(INT), username(VARCHAR), account(VARCHAR), cash(VARCHAR),datetime(VARCHAR).
     
     id is the primary key and should be unique and non null
