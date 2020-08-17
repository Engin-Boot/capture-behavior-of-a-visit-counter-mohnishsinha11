# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given the entry-card issuer issues card to all the visitors
  and sensor was running properly
  and hospital staff attendance system works properly
  
  When we calculate the difference between number of cards issued
  and visitor count ignoring and ignoring the number of hospital staff
  
  Then we can recover from the restarts of the server that runs visit-counter

Scenario: Reconcile counts if the sensor is offline for a while

  Given the entry-card issuer issues card to all the visitors and
  hospital staff attendance system works properly
  
  When we count the number of cards issued
  
  Then we can restore the visitor count for the sensor
