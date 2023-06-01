# alarm_clock
# 0=Sun, 1=Mon, 2=Tue, ...6=Sat; return a string of the form "7:00" indicating when the alarm clock should ring. Weekdays, the alarm should be # "7:00" and on the weekend it should be "10:00". Unless we are on vacation -- then on weekdays it should be "10:00" and weekends it should be "off".
def alarm_clock(day, vacation):
  weekend = False
  if day >= 1 and day <= 5:
    weekend = False
  if day == 0 or day == 6:
    weekend = True
    
  if vacation and weekend: 
    return "off"
  if vacation and not weekend: 
    return "10:00"
  if not vacation and weekend: 
    return "10:00"
  if not vacation and not weekend:
    return "7:00"
