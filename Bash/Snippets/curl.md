# GENERAL USAGE
```bash
# Check Weather
curl http://wttr.in/atlanta

# Check current IP
curl ipinfo.io
curl -s http://whatismyip.akamai.com
curl -s icanhazip.com

# Website Status
curl -Is https://www.twitter.com -L | grep HTTP/
curl https://www.twitter.com -m 5 -s -f -o /dev/null && echo "SUCCESS" || echo "UNREACHABLE"
```

* Send mail using curl
```bash
echo "To:receiver@gmail.net" > /tmp/mail.txt
echo "Subject:test" >> /tmp/mail.txt
echo "This is a test" >> /tmp/mail.txt

curl --url "smtps://smtp.gmail.com:465" --ssl-reqd --mail-from "sender@gmail.com" --mail-rcpt "receiver@gmail.net"   --upload-file /tmp/mail.txt --user "sender@gmail.com:sender_pass" --insecure

rm /tmp/mail.txt
```

# POST

* PushBullet API
```bash
# create push
access_token="o.blahblahblah"
body="text content"
title="title"
email="something@gmail.com"

curl --header 'Access-Token: $access_token' \
     --header 'Content-Type: application/json' \
     --data-binary '{"body":"'" $body"'","title":"'"$title"'","type":"note","email":"'"$email"'"}' \

     --request POST \
     https://api.pushbullet.com/v2/pushes

```

