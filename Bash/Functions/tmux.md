# EXAMPLES
```
tmux new-session -s servers -d "ssh user_name@server_ip"
tmux send-keys -t servers "echo 'Hello World'" ENTER
tmux split-window -v "ssh user_name@server_ip"
tmux attach -t servers
```