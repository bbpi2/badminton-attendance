## Cost Calculation Logic

```text
total_people = SUM(1 + plus_ones) for all Attendance where actual = true
session_cost = venue.cost_per_court × court_count
cost_per_person = session_cost / total_people
```
