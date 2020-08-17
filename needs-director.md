# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given "Visit-counter" for a day
  and hospital staff attendance system works properly
  and visitor card is issued for all patients relatives for a day
  
  When we calculate the value obtained from taking difference
  between the values of hospital staff
  and number of visitor card issues by card issuer
  and "Visit-counter"
  Then the result will be number of patients visiting hospital in a day

Scenario: Compute parking slots to reserve for visiting specialists

  Given count of visiting specialists per day and their arrival time
  and visit-count
  
  When one hour remain before their arrival
  
  Then reserve the free spaces before their arrival if free space is available
  otherwise create free for the specialists
