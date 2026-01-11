import RPi.GPIO as GPIO
import time
import smtplib
from email.message import EmailMessage
from date time import datetime

channel=4
GPIO.setmode(GPIO.BCM)
GPIO.setup(channel,GPIO.IN)

from_email_addr="3922048237@qq.com"
from_email_pass="cexxoerfhfsttbfug"
to_email_addr="3460532268@qq.com"

for i in range(5):
  if GPIO.input(channel):
    plant_status="Water enough"
  else:
    plant_status="More Water"

msg=EmailMessage()
msg.set_content(f"Plant status: {plant_status}")
msg['From']=from_email_addr
msg['To']=to_email_addr
msg['Subject']='Plant Watering Status'

server=smtplib.SMTP('smtp.qq.com',587)
server.starttles()
server.login(from_email_addr,from_email_pass)
server.send_message(msg)
print(f"Email sent: {plant_status}")
server.quit

time.sleep(6*60*60)
