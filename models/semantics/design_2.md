# Example Design

## Metric File: semantic_graph.yml

```yml
metrics:
  - name: revenue
    tests:
		- equivalence:
            equivalence_operator: '='
            value: 123
            filters: 
                - "{{ dimension('metric_time') }} = '2022-01-01'"
                - "{{ dimension('user','location_name') }} = 'Unovo'"
		
		- not_null:
			filters: 
                - "{{ dimension('metric_time') }} > '2022-01-01'"
	
		- expected_range:
			min_value: 0
		    max_value: 10
			filters: 
                - "{{ dimension('metric_time') }} > '2022-01-01'"
	
		- percent_change:
			some_config: lorem_ipsum

```