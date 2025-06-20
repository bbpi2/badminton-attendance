## Data Model

### Player
- `email`: string  
  **Primary key** — Unique identifier for each player  
- `name`: string  
  Display name  
- `default_days`: array of strings  
  Days the player typically attends (e.g., ['mon', 'thu'])

### Venue
- `id`: UUID  
- `name`: string  
  Name of the location  
- `cost_per_court`: float  
  Cost of one court per session

### Session
- `id`: UUID  
- `date`: date  
  Date of badminton session  
- `venue_id`: UUID  
  Reference to Venue  
- `court_count`: integer  
  Number of courts booked  
- `calculated_cost`: float  
  (Derived: venue.cost_per_court × court_count — can be overridden if needed)

### Attendance
- `id`: UUID  
  Unique attendance record  
- `player_email`: string  
  Reference to Player  
- `session_id`: UUID  
  Reference to Session  
- `planned`: boolean  
  Whether the player intended to attend  
- `actual`: boolean  
  Whether the player actually showed up  
- `plus_ones`: integer  
  Number of additional guests brought
