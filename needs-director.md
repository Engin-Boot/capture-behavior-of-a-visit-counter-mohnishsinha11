# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given "Visit-counter" for a day
  and number of hospital staff is known
  and visitor card is issued for all patients relatives for a day
  
  When hospital staff and number of visitor card issued is subtracted
  from "Visit-counter"
  Then the result will be number of patients visiting hospital in a day

Scenario: Compute parking slots to reserve for visiting specialists

  Given count of visiting specialists per day and their arrival time
  and visit-count
  
  When one hour remain before their arrival
  
  Then reserve the free spaces before their arrival if free space is available
  otherwise create free for the specialists
