# fw-517-2025-02-27

![GPIO 26](https://github.com/user-attachments/assets/fe0134f6-c0c5-4620-ac32-9e4ec747760b)￼

11,12,13=heater   16=propeler    15=pump, 18= refrigerator 

<pre>
GPIO.setup(11,GPIO.OUT)<br>
GPIO.setup(12,GPIO.OUT)<br>
GPIO.setup(13,GPIO.OUT)<br>
GPIO.setup(15,GPIO.OUT) # pump<br>
GPIO.setup(18,GPIO.OUT) # freezer<br>
</pre>

<pre>
  if stime+5>=ttime:<br>
    GPIO.output(11,1)<br>
    GPIO.output(12,1)<br>
    GPIO.output(13,1)<br>
  if stime+10>=ttime>stime+5:<br>
    GPIO.output(11,0)<br>
    GPIO.output(12,0)<br>
    GPIO.output(13,0)<br>
</pre>

<pre>
    if float(array2[5])>-15.0:<br>
    if ttime <=ctime+1500.0:<br>
      ssr18="1"<br>
      GPIO.output(18,1)<br>
    if ctime+1500<=ttime<=ctime+1800:<br>
      ssr18="0"<br>
      GPIO.output(18,0)<br>
    if ctime+1800<ttime:<br>
      f18=0<br>
    else:<br>
      ssr18="0"<br>
      GPIO.output(18, 0)<br>
  GPIO.output(15,1) # pump on<br>
</pre>
