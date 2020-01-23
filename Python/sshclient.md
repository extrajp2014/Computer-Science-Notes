# Example
```python
import io
from paramiko import SSHClient
from scp import SCPClient

ssh = SSHClient()
ssh.load_system_host_keys()
ssh.connect('example.com')

# SCPCLient takes a paramiko transport as an argument
scp = SCPClient(ssh.get_transport())

# generate in-memory file-like object
fl = io.BytesIO()
fl.write(b'test')
fl.seek(0)
# upload it directly from memory
scp.putfo(fl, '/tmp/test.txt')
# close connection
scp.close()
# close file handler
fl.close()
```