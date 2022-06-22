
# System Design Interview Notes

## Back-of-the-Envelope Math

### Query per second calculation
```
QPD (Query per day) = 
[Daily active users] x
[% of active users making the query] x
[Average number of queries made by each user per day] x
[Scaling factor]
 ```

Query per second (QPS) ~= QPD / 100k
> There are 84,600 (24 x 60 x 60) seconds per day, you can round that up to 100k for easier calculation.

### Storage Calculation

```
Storage capacity for time horizon =
[Daily active users] x
[% of active users making the query to persist] x
[Average number of queries made by each user] x
[Data size per query] x
[Replication factor] x
[Time horizon]
```
