Send mail using curl
```bash
echo "To:receiver@gmail.net" > /tmp/mail.txt
echo "Subject:test" >> /tmp/mail.txt
echo "This is a test" >> /tmp/mail.txt

curl --url "smtps://smtp.gmail.com:465" --ssl-reqd --mail-from "sender@gmail.com" --mail-rcpt "receiver@gmail.net"   --upload-file /tmp/mail.txt --user "sender@gmail.com:sender_pass" --insecure

rm /tmp/mail.txt
```