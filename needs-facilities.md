# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given visit-counter of previous week
  When there is no pandemic situation
  Then number of visitors in this week will be similar to previous week

Scenario: Alert when seating capacity is full

  Given the Visit-counter
  When the visitor count is more than "90" percent of seating capacity
  Then inform visitors other than patients to wait outside the hospital
