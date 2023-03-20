# Example Design

## Metric File: tests/revenue_range.sql

```sql

with assert_revenue_range as (

	select *
	from {{ 
		metricflow.query(
			metrics=['revenue'] 
			dimensions=['metric_time.granularity(month)']
		}}

)

select *
from assert_revenue_range
where revenue between 1 and 27
```