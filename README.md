# LocalMonitor

## I. Server Setup

### Database Creation
1. create a SQL database with schema named "client_data",2 tables named "positions" and "assets"

2. for "positions" table, it has these columns:
   
     id(INT), username(VARCHAR), account(VARCHAR), code(VARCHAR), cost(FLOAT),current_price(FLOAT),qty(INT),datetime(VARCHAR).
     
     id is the primary key and should be unique and non null
   
4. for "assets" table, it has these columns:
     
     id(INT), username(VARCHAR), account(VARCHAR), cash(VARCHAR),datetime(VARCHAR).
     
     id is the primary key and should be unique and non null


### Local Monitor

you can make it a website dashboard and hosted at the local server, in this way, every computer has access to your local network will have access to this website and can easily monitor all positions and assets data

## II. Polaris Code Update

1. add local server ip address to .env file
2. read that ip address from main.py
3. pass that ip address from main to position summary window during initialization
4. if position summary window's local server ip is not empty (means there is a local server ip address in .env file==> we need to sync data to that local server, if it's empty, means we do not need to sync), set a flag var: is_local_sync to true
5. every time position window fetches cash and position, if flag var is true, call local_sync() function to sync data to the local server
