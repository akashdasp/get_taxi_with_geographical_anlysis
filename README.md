 # Insights from Failed Orders
### with geospecial analysis 
- Gett, previously known as GetTaxi, is an Israeli-developed technology platform solely focused on corporate Ground Transportation Management (GTM). They have an application where clients can order taxis, and drivers can accept their rides (offers). At the moment, when the client clicks the Order button in the application, the matching system searches for the most relevant drivers and offers them the order. In this task, we would like to investigate some matching metrics for orders that did not completed successfully, i.e., the customer didn't end up getting a car.
- # Data Description
We have two data sets: data_orders and data_offers, both being stored in a CSV format. The data_orders data set contains the following columns:

- order_datetime - time of the order
- origin_longitude - longitude of the order
- origin_latitude - latitude of the order
- m_order_eta - time before order arrival
- order_gk - order number
- order_status_key - status, an enumeration consisting of the following mapping:
                 -  4 - cancelled by client,
                 - 9 - cancelled by system, i.e., a reject
- is_driver_assigned_key - whether a driver has been assigned
- cancellation_time_in_seconds - how many seconds passed before cancellation
- The data_offers data set is a simple map with 2 columns:
         - order_gk - order number, associated with the same column from the orders data set
         - offer_id - ID of an offer
        ![alt text](https://github.com/akashdasp/get_taxi_with_geographical_anlysis/blob/d56e347b43fce04649a5fbcdfe24ba81216c22c3/git_map_picture.JPG?raw=True)
