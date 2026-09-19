# 1. SSH in
```bash
ssh <user>@<mikrus-host> -p <ssh-port>
```

# 2. Kill and restart the Python app
```bash
pkill -f serve.py
cd /path/to/your/app
nohup python3 serve.py > server.log 2>&1 &
```

# 3. Restart nginx
```bash
sudo service nginx restart
```

# 4. Confirm both are up
```bash
ps aux | grep serve.py
sudo service nginx status
```