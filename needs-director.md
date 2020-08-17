# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given
  When 
  Then

Scenario: Compute parking slots to reserve for visiting specialists

  Given count of visiting specialists per day and their arrival time
  
  When one hour remain before their arrival
  
  Then reserve the free spaces before their arrival if free space is available
  otherwise create free for the specialists
