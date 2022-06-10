~~~
while(isAlive() && !isRetired()) {
  try {
   while(timeOfDay() < endOfShift()) doWork();
  }catch(SickException e) {
    sleep(86400000);
  }catch(VacationException e) {
    doVacation();
  }catch(Exception e) {
    recover(e);
  }
}
while(isAlive()) /* do nothing */ relax();
~~~
