# Example Design

## Metric File: semantic_graph.yml

```sql

with assert_arr_range as (

	select *
	from {{ 
		metricflow.query(
			metrics=['revenue'] 
			dimensions=['metric_time.granularity(month)']
		}}

)

select *
from assert_arr_growth_range
where revenue between 1 and 27
```