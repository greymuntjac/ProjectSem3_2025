import smtplib
from email.message import EmailMessage

from_email_addr="greymuntjac@qq.com"
from_email_pass="cmsccfefjccmcjgf"
to_email-addr="3460532268@qq.com"

msg=EmailMessage()
body="Hello "
msg set_content(body)
msg['From']=from_email_addr
msg['To']=to_email_addr
msg['Subject']='TEST EMAIL'
server.SMTP('smtp.qq.com',587)
server.starttls()
server.login(from_email_addr,from_email_pass)
server.send_message(msg)
print('Email sent')
server.quit()
