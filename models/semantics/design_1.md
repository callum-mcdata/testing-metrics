# Example Design

## Seed File: seeds/revenue_seed.csv

| metric_time__year      | location_type | revenue |
| ----------- | ----------- | ---------- |
| "2023-03-16"      | Unovo       | 100  |


## Metric File: semantic_graph.yml
```yaml
metrics:
- name: revenue
  description: "Our revenue"
  type: measure_proxy
  type_params:
    measure: order_total
	tests:
	  - seed: ref('revenue_seed')
		filters:
	      - "{{ dimension('metric_time') }} > '2022-01-01'"
		  - "{{ dimension('user','location_name') }} = 'Unovo'"
```