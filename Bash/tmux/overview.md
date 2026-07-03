## Server Management

| Code | Description |
|------|-------------|
| `tmux` | Starts a new tmux server and creates a new session. |
| `tmux new-session` | Creates a new session. Alias: `new`. |
| `tmux new-session -s session_name` | Creates a new session with a custom name. |
| `tmux new-session -d` | Creates a new session in detached mode. |
| `tmux new-session -A -s session_name` | Attaches to an existing session or creates a new one. |
| `tmux new-session -t session_name` | Creates a new session in a specific target session. |
| `tmux attach-session` | Attaches to the most recently used session. Alias: `attach`. |
| `tmux attach-session -t session_name` | Attaches to a specific session. |
| `tmux attach-session -d` | Attaches to a session in detached mode. |
| `tmux detach` | Detaches the current client from the session. Alias: `detach`. |
| `tmux detach -P` | Detaches the current client and prints the session name. |
| `tmux kill-server` | Kills the tmux server and all sessions. |
| `tmux kill-server -a` | Kills the tmux server and all clients. |
| `tmux list-sessions` | Lists all sessions. Alias: `ls`. |
| `tmux list-sessions -a` | Lists all sessions, including unattached ones. |
| `tmux list-sessions -F "#{session_name}"` | Lists sessions with a custom format. |
| `tmux show-server-access` | Shows server access information. Alias: `showserveraccess`. |
| `tmux server-access -a` | Adds server access for a user. |
| `tmux server-access -r` | Removes server access for a user. |
| `tmux server-access -l` | Lists server access permissions. |
| `tmux server-info` | Shows information about the tmux server. |

---
## Session Management

| Code | Description |
|------|-------------|
| `tmux new-session -s session_name` | Creates a new session with a custom name. |
| `tmux rename-session -t old_name new_name` | Renames a session. Alias: `rename`. |
| `tmux switch-client -t session_name` | Switches the current client to a different session. Alias: `switch`. |
| `tmux switch-client -l` | Switches to the last session. |
| `tmux switch-client -n` | Switches to the next session. |
| `tmux switch-client -p` | Switches to the previous session. |
| `tmux switch-client -c` | Switches to a new session. |
| `tmux kill-session -t session_name` | Kills a specific session. Alias: `kill-session`. |
| `tmux kill-session -a` | Kills all sessions except the current one. |
| `tmux kill-session -a -t session_name` | Kills all sessions except the specified one. |
| `tmux has-session -t session_name` | Checks if a session exists. Returns 0 if it exists, 1 if not. |
| `tmux suspend-client` | Suspends the current client. Alias: `suspendc`. |
| `tmux suspend-client -t session_name` | Suspends a specific client. |
| `tmux attach-client -t session_name` | Attaches a suspended client. Alias: `attachc`. |
| `tmux detach-client` | Detaches a specific client. Alias: `detachc`. |
| `tmux detach-client -t session_name` | Detaches a client from a specific session. |
| `tmux detach-client -P` | Detaches the current client and prints the session name. |
| `tmux lock-client` | Locks the current client. Alias: `lockc`. |
| `tmux lock-session` | Locks all clients in the current session. Alias: `lock`. |
| `tmux lock-server` | Locks all clients on the server. Alias: `locks`. |
| `tmux list-clients` | Lists all connected clients. Alias: `lsc`. |
| `tmux list-clients -t session_name` | Lists clients attached to a specific session. |
| `tmux list-clients -F "#{client_name}"` | Lists clients with a custom format. |
| `tmux refresh-client` | Refreshes the current client. Alias: `refresh`. |
| `tmux refresh-client -t session_name` | Refreshes a specific client. |
| `tmux send-keys -t session_name "command"` | Sends keys to a specific session. |
| `tmux send-keys -t session_name:window.pane "command"` | Sends keys to a specific pane in a window. |
| `tmux send-keys -t session_name C-c` | Sends Ctrl+C to a session. |
| `tmux send-keys -t session_name "command" C-m` | Sends a command followed by Enter to a session. |
| `tmux send-prefix -t session_name` | Sends the prefix key to a session. |
| `tmux display-message -t session_name "message"` | Displays a message in a session. Alias: `display`. |
| `tmux display-panes -t session_name` | Displays all panes in a session. Alias: `displayp`. |

---
## Window Management

| Code | Description |
|------|-------------|
| `tmux new-window` | Creates a new window in the current session. Alias: `neww`. |
| `tmux new-window -n window_name` | Creates a new window with a custom name. |
| `tmux new-window -t session_name` | Creates a new window in a specific session. |
| `tmux new-window -t session_name:window_index` | Creates a new window at a specific index. |
| `tmux new-window -a` | Creates a new window after the last window. |
| `tmux new-window -b` | Creates a new window before the last window. |
| `tmux new-window -d` | Creates a new window in detached mode. |
| `tmux new-window -c /path/to/dir` | Creates a new window with a custom working directory. |
| `tmux list-windows` | Lists all windows in the current session. Alias: `lsw`. |
| `tmux list-windows -t session_name` | Lists all windows in a specific session. |
| `tmux list-windows -a` | Lists all windows, including those in other sessions. |
| `tmux list-windows -F "#{window_name}"` | Lists windows with a custom format. |
| `tmux select-window -t window_index` | Selects a window by index. Alias: `selectw`. |
| `tmux select-window -t window_name` | Selects a window by name. |
| `tmux select-window -n` | Selects the next window. |
| `tmux select-window -p` | Selects the previous window. |
| `tmux select-window -l` | Selects the last window. |
| `tmux select-window -f` | Selects the first window. |
| `tmux next-window` | Moves to the next window. Alias: `nextw`. |
| `tmux previous-window` | Moves to the previous window. Alias: `prevw`. |
| `tmux last-window` | Moves to the last window. Alias: `lastw`. |
| `tmux swap-window -s source_window -t target_window` | Swaps two windows. Alias: `swapw`. |
| `tmux swap-window -t target_window` | Swaps the current window with the target window. |
| `tmux move-window -s source_window -t target_session` | Moves a window to a different session. Alias: `movew`. |
| `tmux move-window -t target_session:target_index` | Moves a window to a specific index in a session. |
| `tmux move-window -r` | Renumbers windows in a session. |
| `tmux link-window -s source_window -t target_session` | Links a window to another session. Alias: `linkw`. |
| `tmux unlink-window -t window` | Unlinks a window from a session. Alias: `unlinkw`. |
| `tmux kill-window -t window` | Kills a specific window. Alias: `killw`. |
| `tmux kill-window -a` | Kills all windows except the current one. |
| `tmux rename-window -t window new_name` | Renames a window. Alias: `renamew`. |
| `tmux select-layout -t window layout_name` | Applies a specific layout to a window. Alias: `selectl`. |
| `tmux select-layout -n` | Applies the next layout. |
| `tmux select-layout -p` | Applies the previous layout. |
| `tmux select-layout -t` | Toggles between the current and last layout. |
| `tmux next-layout` | Applies the next layout. Alias: `nextl`. |
| `tmux previous-layout` | Applies the previous layout. Alias: `prevl`. |
| `tmux rotate-window -D` | Rotates window down. |
| `tmux rotate-window -U` | Rotates window up. |
| `tmux balance-window` | Balances the sizes of panes in a window. |
| `tmux balance-window -t window` | Balances the sizes of panes in a specific window. |

---
## Pane Management

| Code | Description |
|------|-------------|
| `tmux split-window` | Splits the current pane into two. Alias: `splitw`. |
| `tmux split-window -h` | Splits the current pane horizontally. |
| `tmux split-window -v` | Splits the current pane vertically. |
| `tmux split-window -t target_pane` | Splits a specific pane. |
| `tmux split-window -c /path/to/dir` | Splits the pane with a custom working directory. |
| `tmux split-window -d` | Splits the pane in detached mode. |
| `tmux split-window -p 25` | Splits the pane with 25% of the current pane size. |
| `tmux split-window -l 25` | Splits the pane with 25 lines. |
| `tmux split-window -b` | Splits the pane before the current pane. |
| `tmux split-window -a` | Splits the pane after the current pane. |
| `tmux list-panes` | Lists all panes in the current window. Alias: `lsp`. |
| `tmux list-panes -t session:window` | Lists all panes in a specific window. |
| `tmux list-panes -a` | Lists all panes, including those in other sessions. |
| `tmux list-panes -F "#{pane_index}"` | Lists panes with a custom format. |
| `tmux select-pane -t pane_index` | Selects a pane by index. Alias: `selectp`. |
| `tmux select-pane -U` | Selects the pane above. |
| `tmux select-pane -D` | Selects the pane below. |
| `tmux select-pane -L` | Selects the pane to the left. |
| `tmux select-pane -R` | Selects the pane to the right. |
| `tmux select-pane -l` | Selects the last pane. |
| `tmux next-pane` | Selects the next pane. |
| `tmux previous-pane` | Selects the previous pane. |
| `tmux swap-pane -s source_pane -t target_pane` | Swaps two panes. Alias: `swapp`. |
| `tmux swap-pane -U` | Swaps the current pane with the pane above. |
| `tmux swap-pane -D` | Swaps the current pane with the pane below. |
| `tmux move-pane -t target_pane` | Moves the current pane to a new position. Alias: `movep`. |
| `tmux move-pane -s source_pane -t target_pane` | Moves a specific pane to a new position. |
| `tmux move-pane -l` | Moves the current pane to the left. |
| `tmux move-pane -r` | Moves the current pane to the right. |
| `tmux move-pane -u` | Moves the current pane up. |
| `tmux move-pane -d` | Moves the current pane down. |
| `tmux move-pane -t session:window.index` | Moves a pane to a specific window and index. |
| `tmux kill-pane -t pane` | Kills a specific pane. Alias: `killp`. |
| `tmux kill-pane -a` | Kills all panes except the current one. |
| `tmux resize-pane -t pane -x width` | Resizes a pane horizontally. Alias: `resizep`. |
| `tmux resize-pane -t pane -y height` | Resizes a pane vertically. |
| `tmux resize-pane -t pane -L 5` | Resizes a pane by moving its left border 5 cells to the left. |
| `tmux resize-pane -t pane -R 5` | Resizes a pane by moving its right border 5 cells to the right. |
| `tmux resize-pane -t pane -U 5` | Resizes a pane by moving its top border 5 cells up. |
| `tmux resize-pane -t pane -D 5` | Resizes a pane by moving its bottom border 5 cells down. |
| `tmux resize-pane -t pane 20` | Resizes a pane to a specific size. |
| `tmux break-pane -t pane` | Breaks a pane off into a new window. Alias: `breakp`. |
| `tmux break-pane -t pane -n window_name` | Breaks a pane into a new window with a custom name. |
| `tmux break-pane -t pane -t session:window.index` | Breaks a pane into a specific window and index. |
| `tmux join-pane -s source_pane -t target_pane` | Joins a pane into a window. Alias: `joinp`. |
| `tmux join-pane -t target_pane` | Joins the current pane into a target pane. |
| `tmux join-pane -h -t target_pane` | Joins the current pane horizontally into a target pane. |
| `tmux join-pane -v -t target_pane` | Joins the current pane vertically into a target pane. |

---
## Copy Mode and Scrollback

| Code | Description |
|------|-------------|
| `<prefix> [` | Enters copy mode. |
| `q` | Quits copy mode. |
| `Space` | Starts selection at the current cursor position. |
| `Enter` | Copies the current selection to the paste buffer and exits copy mode. |
| `y` | Yanks (copies) the current selection to the paste buffer. |
| `Y` | Yanks the current selection to a named buffer. |
| `p` | Pastes from the paste buffer. |
| `P` | Pastes from the paste buffer (with mouse support). |
| `Ctrl-space` | Starts a new selection. |
| `Ctrl-a` | Goes to the start of the line. |
| `$` | Goes to the end of the line. |
| `0` | Goes to the start of the line. |
| `^` | Goes to the first non-whitespace character of the line. |
| `G` | Goes to the bottom of the scrollback. |
| `g` | Goes to the top of the scrollback. |
| `M-g` | Goes to a specific line number (prompts for line number). |
| `/` | Enters forward search mode. |
| `?` | Enters backward search mode. |
| `n` | Goes to the next search match. |
| `N` | Goes to the previous search match. |
| `C-s` | Saves the current selection to a file. |
| `:` | Enters command mode from copy mode. |
| `C-u` | Scrolls up by half a page. |
| `C-d` | Scrolls down by half a page. |
| `M-u` | Scrolls up by half a page. |
| `M-d` | Scrolls down by half a page. |
| `Page Up` | Scrolls up by one page. |
| `Page Down` | Scrolls down by one page. |
| `Half Page Up` | Scrolls up by half a page. |
| `Half Page Down` | Scrolls down by half a page. |
| `C-b` | Moves the cursor back one page. |
| `C-f` | Moves the cursor forward one page. |
| `C-Up` | Scrolls up one line. |
| `C-Down` | Scrolls down one line. |
| `Mouse drag` | Selects text with the mouse. |
| `Mouse click` | Pastes the selection at the cursor position. |
| `Double click` | Selects a word. |
| `Triple click` | Selects a line. |
| `Mouse wheel` | Scrolls the pane. |

---
## Buffer Management

| Code | Description |
|------|-------------|
| `tmux list-buffers` | Lists all paste buffers. Alias: `lsb`. |
| `tmux list-buffers -F "#{buffer_name}"` | Lists buffers with a custom format. |
| `tmux show-buffer` | Displays the contents of the most recent paste buffer. Alias: `showb`. |
| `tmux show-buffer -b buffer_name` | Displays the contents of a specific paste buffer. |
| `tmux save-buffer -b buffer_name -a` | Appends the contents of a paste buffer to a file. Alias: `saveb`. |
| `tmux save-buffer -b buffer_name file` | Saves the contents of a paste buffer to a file. |
| `tmux paste-buffer` | Pastes the contents of the most recent paste buffer. Alias: `pasteb`. |
| `tmux paste-buffer -b buffer_name` | Pastes the contents of a specific paste buffer. |
| `tmux paste-buffer -t target_pane` | Pastes to a specific pane. |
| `tmux delete-buffer -b buffer_name` | Deletes a specific paste buffer. Alias: `deleteb`. |
| `tmux delete-buffer -a` | Deletes all paste buffers. |
| `tmux choose-buffer` | Interactively selects a paste buffer to insert. Alias: `chooseb`. |
| `tmux choose-buffer -t target_pane` | Interactively selects a paste buffer to insert into a specific pane. |
| `tmux load-buffer file` | Loads the contents of a file into a paste buffer. Alias: `loadb`. |
| `tmux load-buffer -b buffer_name file` | Loads the contents of a file into a specific paste buffer. |
| `tmux append-buffer -b buffer_name file` | Appends the contents of a file to a paste buffer. Alias: `appendb`. |

---
## Key Bindings

| Code | Description |
|------|-------------|
| `tmux list-keys` | Lists all key bindings. Alias: `lk`. |
| `tmux list-keys -t prefix` | Lists all key bindings for the prefix key. |
| `tmux list-keys -t root` | Lists all key bindings for the root table. |
| `tmux bind-key` | Binds a key to a command. Alias: `bind`. |
| `tmux bind-key key command` | Binds a key to a command. |
| `tmux bind-key -n key command` | Binds a key to a command with a note. |
| `tmux bind-key -r key command` | Binds a key to a command with repeat enabled. |
| `tmux bind-key -T prefix key command` | Binds a key to a command for a specific terminal type. |
| `tmux bind-key -c key command` | Binds a key to a command for a specific client. |
| `tmux unbind-key key` | Unbinds a key. Alias: `unbind`. |
| `tmux unbind-key -T prefix key` | Unbinds a key for a specific terminal type. |
| `tmux bind-key C-b send-prefix` | Binds Ctrl+b to send the prefix key. |
| `tmux bind-key -r C-b send-prefix` | Binds Ctrl+b to send the prefix key with repeat enabled. |
| `tmux bind-key C-a send-prefix` | Changes the prefix key to Ctrl+a. |
| `tmux bind-key -n new-window "new-window -n #{window_name}"` | Binds a key to create a new window with a custom name. |
| `tmux bind-key -n split-window "split-window -v -c #{pane_current_path}"` | Binds a key to split the window vertically in the current directory. |
| `tmux bind-key -n attach-session "attach-session -t #{session_name}"` | Binds a key to attach to a session. |
| `tmux bind-key -n detach "detach"` | Binds a key to detach from the session. |
| `tmux bind-key -n run-command "run-shell 'command'"` | Binds a key to run a shell command. |
| `tmux bind-key -n copy-mode "copy-mode"` | Binds a key to enter copy mode. |
| `tmux bind-key -n paste-buffer "paste-buffer"` | Binds a key to paste from the buffer. |
| `tmux bind-key -n switch-client "switch-client -l"` | Binds a key to switch to the last session. |
| `tmux bind-key -n next-window "next-window"` | Binds a key to move to the next window. |
| `tmux bind-key -n previous-window "previous-window"` | Binds a key to move to the previous window. |
| `tmux bind-key -n select-window-0 "select-window -t 0"` | Binds a key to select window 0. |
| `tmux bind-key -n select-window-1 "select-window -t 1"` | Binds a key to select window 1. |

---
## Configuration Commands

| Code | Description |
|------|-------------|
| `tmux set-option` | Sets a session or global option. Alias: `set`. |
| `tmux set-option -g option value` | Sets a global option. |
| `tmux set-option -t session_name option value` | Sets an option for a specific session. |
| `tmux set-option -t session_name:window option value` | Sets an option for a specific window. |
| `tmux set-option -t session_name:window.pane option value` | Sets an option for a specific pane. |
| `tmux set-option -a` | Sets an option for all sessions. |
| `tmux set-option -q` | Quietly sets an option (no error if option does not exist). |
| `tmux set-option -o` | Sets an option and overrides the default. |
| `tmux set-option -g prefix C-a` | Changes the prefix key to Ctrl+a globally. |
| `tmux set-option -g base-index 1` | Changes the base index for windows and panes to 1. |
| `tmux set-option -g pane-base-index 1` | Changes the base index for panes to 1. |
| `tmux set-option -g bell-action none` | Disables the terminal bell. |
| `tmux set-option -g visual-activity on` | Enables visual activity notification. |
| `tmux set-option -g visual-bell on` | Enables visual bell notification. |
| `tmux set-option -g visual-silence on` | Enables visual silence notification. |
| `tmux set-option -g default-command "bash"` | Sets the default command for new windows. |
| `tmux set-option -g default-path "/home/user"` | Sets the default path for new windows. |
| `tmux set-option -g display-time 2000` | Sets the display time for messages in milliseconds. |
| `tmux set-option -g escape-time 500` | Sets the escape time in milliseconds. |
| `tmux set-option -g history-limit 10000` | Sets the maximum number of lines in the scrollback buffer. |
| `tmux set-option -g buffer-limit 50` | Sets the maximum number of paste buffers. |
| `tmux set-option -g repeat-time 500` | Sets the repeat time for key repeats in milliseconds. |
| `tmux set-option -g status on` | Enables the status bar. |
| `tmux set-option -g status off` | Disables the status bar. |
| `tmux set-option -g status-interval 1` | Sets the status bar refresh interval in seconds. |
| `tmux set-option -g status-justify centre` | Centers the status bar. |
| `tmux set-option -g status-left ""` | Clears the left side of the status bar. |
| `tmux set-option -g status-right ""` | Clears the right side of the status bar. |
| `tmux set-option -g status-left-length 20` | Sets the length of the left side of the status bar. |
| `tmux set-option -g status-right-length 50` | Sets the length of the right side of the status bar. |
| `tmux set-option -g status-bg colour0` | Sets the background color of the status bar. |
| `tmux set-option -g status-fg colour7` | Sets the foreground color of the status bar. |
| `tmux set-option -g status-attr dim` | Sets the attribute of the status bar to dim. |
| `tmux set-option -g window-status-current-bg colour2` | Sets the background color of the current window in the status bar. |
| `tmux set-option -g window-status-current-fg colour0` | Sets the foreground color of the current window in the status bar. |
| `tmux set-option -g window-status-current-attr bold` | Sets the attribute of the current window in the status bar to bold. |
| `tmux set-option -g window-status-bg colour0` | Sets the background color of windows in the status bar. |
| `tmux set-option -g window-status-fg colour7` | Sets the foreground color of windows in the status bar. |
| `tmux set-option -g pane-border-status off` | Disables pane border status indicators. |
| `tmux set-option -g pane-border-status top` | Shows pane border status at the top. |
| `tmux set-option -g pane-border-light` | Uses light pane borders. |
| `tmux set-option -g pane-border-dark` | Uses dark pane borders. |
| `tmux set-option -g pane-border-bg colour0` | Sets the background color of pane borders. |
| `tmux set-option -g pane-border-fg colour7` | Sets the foreground color of pane borders. |
| `tmux set-option -g mouse on` | Enables mouse support. |
| `tmux set-option -g mouse off` | Disables mouse support. |
| `tmux set-option -g mouse-resize on` | Enables mouse resize support. |
| `tmux set-option -g mouse-sb on` | Enables mouse scrollback support. |
| `tmux set-option -g mode-keys vi` | Uses vi key bindings in copy mode. |
| `tmux set-option -g mode-keys emacs` | Uses emacs key bindings in copy mode. |
| `tmux set-environment` | Sets environment variables. Alias: `setenv`. |
| `tmux set-environment -g VAR value` | Sets a global environment variable. |
| `tmux set-environment -t session_name VAR value` | Sets an environment variable for a specific session. |
| `tmux set-environment -r VAR` | Removes an environment variable. |
| `tmux set-environment -U VAR` | Unsets an environment variable. |
| `tmux show-options` | Shows the options for a session or global options. Alias: `show`. |
| `tmux show-options -g` | Shows global options. |
| `tmux show-options -t session_name` | Shows options for a specific session. |
| `tmux show-options -t session_name:window` | Shows options for a specific window. |
| `tmux show-options -t session_name:window.pane` | Shows options for a specific pane. |
| `tmux show-options -q` | Shows options quietly (no error if option does not exist). |
| `tmux show-environment` | Shows environment variables. Alias: `showenv`. |
| `tmux show-environment -g` | Shows global environment variables. |
| `tmux show-environment -t session_name` | Shows environment variables for a specific session. |

---
## Window Options

| Code | Description |
|------|-------------|
| `tmux set-window-option` | Sets a window option. Alias: `setw`. |
| `tmux set-window-option -g option value` | Sets a global window option. |
| `tmux set-window-option -t session_name:window option value` | Sets an option for a specific window. |
| `tmux set-window-option -a` | Sets an option for all windows. |
| `tmux set-window-option -q` | Quietly sets an option (no error if option does not exist). |
| `tmux set-window-option -g automatic-rename on` | Enables automatic renaming of windows. |
| `tmux set-window-option -g automatic-rename off` | Disables automatic renaming of windows. |
| `tmux set-window-option -g automatic-rename-format "#I:#W"` | Sets the format for automatic window renaming. |
| `tmux set-window-option -g window-status-format "#I:#W"` | Sets the format for window status. |
| `tmux set-window-option -g window-status-current-format "#[bold]#I:#W#[default]"` | Sets the format for the current window status. |
| `tmux set-window-option -g window-status-bg colour0` | Sets the background color of window status. |
| `tmux set-window-option -g window-status-fg colour7` | Sets the foreground color of window status. |
| `tmux set-window-option -g window-status-attr none` | Sets the attribute of window status. |
| `tmux set-window-option -g window-status-current-bg colour2` | Sets the background color of the current window status. |
| `tmux set-window-option -g window-status-current-fg colour0` | Sets the foreground color of the current window status. |
| `tmux set-window-option -g window-status-current-attr bold` | Sets the attribute of the current window status. |
| `tmux set-window-option -g synchronize-panes on` | Enables synchronized input for all panes in a window. |
| `tmux set-window-option -g synchronize-panes off` | Disables synchronized input for all panes in a window. |
| `tmux show-window-options` | Shows the options for a window. Alias: `showw`. |
| `tmux show-window-options -g` | Shows global window options. |
| `tmux show-window-options -t session_name:window` | Shows options for a specific window. |

---
## Pane Options

| Code | Description |
|------|-------------|
| `tmux set-pane-option` | Sets a pane option. |
| `tmux set-pane-option -t session_name:window.pane option value` | Sets an option for a specific pane. |
| `tmux set-pane-option -g option value` | Sets a global pane option. |
| `tmux set-pane-option -a` | Sets an option for all panes. |
| `tmux show-pane-options` | Shows the options for a pane. |
| `tmux show-pane-options -t session_name:window.pane` | Shows options for a specific pane. |

---
## Hooks

| Code | Description |
|------|-------------|
| `tmux set-hook` | Sets a hook. Alias: `sethook`. |
| `tmux set-hook -g hook_name command` | Sets a global hook. |
| `tmux set-hook -t session_name hook_name command` | Sets a hook for a specific session. |
| `tmux set-hook -t session_name:window hook_name command` | Sets a hook for a specific window. |
| `tmux set-hook -t session_name:window.pane hook_name command` | Sets a hook for a specific pane. |
| `tmux set-hook -a hook_name command` | Sets a hook for all sessions, windows, or panes. |
| `tmux set-hook -r hook_name` | Removes a hook. |
| `tmux set-hook -l hook_name` | Lists hooks. |
| `tmux show-hooks` | Shows all hooks. Alias: `showhooks`. |
| `tmux show-hooks -g` | Shows global hooks. |
| `tmux show-hooks -t session_name` | Shows hooks for a specific session. |
| `tmux run-shell` | Runs a shell command when a hook is triggered. Alias: `run`. |
| `tmux run-shell -g command` | Runs a shell command globally. |
| `tmux run-shell -t session_name command` | Runs a shell command for a specific session. |
| `tmux run-shell -b hook_name command` | Runs a shell command when a specific hook is triggered. |
| `tmux run-shell -c client_name command` | Runs a shell command for a specific client. |
| `tmux run-shell -t session_name:window command` | Runs a shell command for a specific window. |

---
## Common Hooks

| Code | Description |
|------|-------------|
| `client-attached` | Triggered when a client is attached to a session. |
| `client-detached` | Triggered when a client is detached from a session. |
| `session-created` | Triggered when a session is created. |
| `session-closed` | Triggered when a session is closed. |
| `session-renamed` | Triggered when a session is renamed. |
| `window-created` | Triggered when a window is created. |
| `window-closed` | Triggered when a window is closed. |
| `window-renamed` | Triggered when a window is renamed. |
| `pane-created` | Triggered when a pane is created. |
| `pane-closed` | Triggered when a pane is closed. |
| `pane-exited` | Triggered when a pane's command exits. |
| `alert-silence` | Triggered when an alert is silenced. |
| `alert-activity` | Triggered when activity occurs in a window. |
| `alert-bell` | Triggered when a bell is rung in a window. |
| `client-resized` | Triggered when a client is resized. |
| `pane-resized` | Triggered when a pane is resized. |
| `session-alert` | Triggered when an alert is set for a session. |

---
## Default Key Bindings

| Code | Description |
|------|-------------|
| `<prefix>` | Activates the prefix key. Default: Ctrl-b. |
| `<prefix> ?` | Lists all key bindings. |
| `<prefix> :` | Enters command mode. |
| `<prefix> c` | Creates a new window. |
| `<prefix> %` | Splits the current pane horizontally. |
| `<prefix> "` | Splits the current pane vertically. |
| `<prefix> x` | Kills the current pane. |
| `<prefix> !` | Breaks the current pane off into a new window. |
| `<prefix> o` | Selects the next pane. |
| `<prefix> ;` | Toggles between the current and last pane. |
| `<prefix> n` | Selects the next window. |
| `<prefix> p` | Selects the previous window. |
| `<prefix> l` | Selects the last window. |
| `<prefix> 0-9` | Selects window 0-9. |
| `<prefix> '` | Prompts for a window index to select. |
| `<prefix> w` | Displays an interactive window list. |
| `<prefix> s` | Selects a session from a list. |
| `<prefix> d` | Detaches from the current session. |
| `<prefix> $` | Renames the current session. |
| `<prefix> &` | Kills the current window. |
| `<prefix> ,` | Renames the current window. |
| `<prefix> .` | Moves the current window to a new index. |
| `<prefix> f` | Prompts to search for text in the current pane. |
| `<prefix> [` | Enters copy mode. |
| `<prefix> ]` | Pastes from the paste buffer. |
| `<prefix> -` | Deletes the most recent paste buffer. |
| `<prefix> =` | Prompts to choose a paste buffer to insert. |
| `<prefix> \` | Swaps the current pane with the next pane. |
| `<prefix> {` | Swaps the current window with the next window. |
| `<prefix> }` | Swaps the current window with the previous window. |
| `<prefix> Space` | Toggles between layouts. |
| `<prefix> M-1` | Selects the alternate layout 1. |
| `<prefix> M-2` | Selects the alternate layout 2. |
| `<prefix> M-5` | Toggles the pane border status. |
| `<prefix> M-o` | Rotates the panes in the current window. |
| `<prefix> M-n` | Moves to the next window with a bell or activity. |
| `<prefix> M-p` | Moves to the previous window with a bell or activity. |
| `<prefix> M-c` | Creates a new session. |
| `<prefix> M-$` | Renames the current session. |
| `<prefix> M-&` | Kills all windows except the current one. |
| `<prefix> M-d` | Selects the first client in the session. |
| `<prefix> M-Up` | Resizes the current pane up. |
| `<prefix> M-Down` | Resizes the current pane down. |
| `<prefix> M-Left` | Resizes the current pane left. |
| `<prefix> M-Right` | Resizes the current pane right. |
| `<prefix> M-q` | Briefly displays pane numbers. |
| `<prefix> M-w` | Selects a window by name. |
| `<prefix> M-s` | Synchronizes all panes in the window. |
| `<prefix> M-:` | Prompts for a command and executes it in all panes. |
| `<prefix> M-m` | Marks the current pane. |
| `<prefix> M-Enter` | Toggles the current pane between full-screen and normal size. |

---
## Copy Mode Key Bindings

| Code | Description |
|------|-------------|
| `q` | Quits copy mode. |
| `Space` | Starts selection at the current cursor position. |
| `Enter` | Copies the current selection to the paste buffer and exits copy mode. |
| `y` | Yanks (copies) the current selection to the paste buffer. |
| `Y` | Yanks the current selection to a named buffer. |
| `p` | Pastes from the paste buffer. |
| `P` | Pastes from the paste buffer (with mouse support). |
| `Ctrl-Space` | Starts a new selection. |
| `Ctrl-a` | Goes to the start of the line. |
| `Ctrl-e` | Goes to the end of the line. |
| `Ctrl-b` | Moves the cursor back one character. |
| `Ctrl-f` | Moves the cursor forward one character. |
| `Ctrl-u` | Scrolls up by half a page. |
| `Ctrl-d` | Scrolls down by half a page. |
| `Ctrl-y` | Copies the current selection to the paste buffer. |
| `Ctrl-p` | Pastes from the paste buffer. |
| `Ctrl-k` | Clears the current selection. |
| `Ctrl-l` | Clears the screen and moves the cursor to the top. |
| `Ctrl-w` | Deletes the current selection. |
| `Ctrl-r` | Refreshes the screen. |
| `Ctrl-s` | Saves the current selection to a file. |
| `0` | Goes to the start of the line. |
| `$` | Goes to the end of the line. |
| `^` | Goes to the first non-whitespace character of the line. |
| `G` | Goes to the bottom of the scrollback. |
| `g` | Goes to the top of the scrollback. |
| `M-g` | Goes to a specific line number (prompts for line number). |
| `/` | Enters forward search mode. |
| `?` | Enters backward search mode. |
| `n` | Goes to the next search match. |
| `N` | Goes to the previous search match. |
| `:` | Enters command mode from copy mode. |
| `v` | Enters visual selection mode. |
| `V` | Enters line-wise visual selection mode. |
| `Ctrl-v` | Enters block-wise visual selection mode. |
| `C` | Enters rectangular selection mode. |
| `Page Up` | Scrolls up by one page. |
| `Page Down` | Scrolls down by one page. |
| `Half Page Up` | Scrolls up by half a page. |
| `Half Page Down` | Scrolls down by half a page. |
| `Up Arrow` | Moves the cursor up one line. |
| `Down Arrow` | Moves the cursor down one line. |
| `Left Arrow` | Moves the cursor left one character. |
| `Right Arrow` | Moves the cursor right one character. |

---
## Vi Mode Key Bindings

| Code | Description |
|------|-------------|
| `set-option -g mode-keys vi` | Enables vi key bindings in copy mode. |
| `h` | Moves the cursor left one character. |
| `j` | Moves the cursor down one line. |
| `k` | Moves the cursor up one line. |
| `l` | Moves the cursor right one character. |
| `0` | Goes to the start of the line. |
| `$` | Goes to the end of the line. |
| `^` | Goes to the first non-whitespace character of the line. |
| `G` | Goes to the bottom of the scrollback. |
| `g` | Goes to the top of the scrollback. |
| `gg` | Goes to the top of the scrollback. |
| `M-g` | Goes to a specific line number (prompts for line number). |
| `w` | Moves forward to the start of the next word. |
| `W` | Moves forward to the start of the next word (ignoring punctuation). |
| `b` | Moves backward to the start of the previous word. |
| `B` | Moves backward to the start of the previous word (ignoring punctuation). |
| `e` | Moves forward to the end of the next word. |
| `E` | Moves forward to the end of the next word (ignoring punctuation). |
| `ge` | Moves backward to the end of the previous word. |
| `gE` | Moves backward to the end of the previous word (ignoring punctuation). |
| `f` | Moves forward to the next occurrence of a character (prompts for character). |
| `F` | Moves backward to the previous occurrence of a character (prompts for character). |
| `t` | Moves forward to the next occurrence of a character before it (prompts for character). |
| `T` | Moves backward to the previous occurrence of a character before it (prompts for character). |
| `;` | Repeats the last f, F, t, or T command. |
| `,` | Repeats the last f, F, t, or T command in the opposite direction. |
| `/` | Enters forward search mode. |
| `?` | Enters backward search mode. |
| `n` | Goes to the next search match. |
| `N` | Goes to the previous search match. |
| `v` | Enters visual selection mode. |
| `V` | Enters line-wise visual selection mode. |
| `Ctrl-v` | Enters block-wise visual selection mode. |
| `C` | Enters rectangular selection mode. |
| `Space` | Starts selection at the current cursor position. |
| `y` | Yanks (copies) the current selection to the paste buffer. |
| `Y` | Yanks the current line to the paste buffer. |
| `p` | Pastes from the paste buffer. |
| `P` | Pastes from the paste buffer (with mouse support). |
| `dd` | Deletes the current line. |
| `D` | Deletes from the cursor to the end of the line. |
| `yy` | Yanks the current line to the paste buffer. |
| `cw` | Changes from the cursor to the end of the word. |
| `C` | Changes from the cursor to the end of the line. |
| `r` | Replaces the character under the cursor. |
| `R` | Enters replace mode. |
| `~` | Toggles the case of the character under the cursor. |
| `x` | Deletes the character under the cursor. |
| `X` | Deletes the character before the cursor. |
| `i` | Enters insert mode. |
| `I` | Enters insert mode at the start of the line. |
| `a` | Enters insert mode after the cursor. |
| `A` | Enters insert mode at the end of the line. |
| `Esc` | Exits insert mode or visual mode. |

---
## Mouse Mode Key Bindings

| Code | Description |
|------|-------------|
| `set-option -g mouse on` | Enables mouse support. |
| `set-option -g mouse off` | Disables mouse support. |
| `set-option -g mouse-resize on` | Enables mouse resize support. |
| `set-option -g mouse-sb on` | Enables mouse scrollback support. |
| `Left click` | Selects a pane. |
| `Right click` | Pastes from the paste buffer. |
| `Mouse drag` | Selects text. |
| `Double click` | Selects a word. |
| `Triple click` | Selects a line. |
| `Mouse wheel` | Scrolls the pane. |
| `Ctrl + Mouse wheel` | Zooms the pane font size. |
| `Shift + Mouse wheel` | Scrolls the pane horizontally. |
| `Middle click` | Pastes the primary selection. |

---
## Command Mode Commands

| Code | Description |
|------|-------------|
| `new-session` | Creates a new session. Alias: `new`. |
| `new-session -s session_name` | Creates a new session with a custom name. |
| `new-session -d` | Creates a new session in detached mode. |
| `new-session -A -s session_name` | Attaches to an existing session or creates a new one. |
| `attach-session` | Attaches to the most recently used session. Alias: `attach`. |
| `attach-session -t session_name` | Attaches to a specific session. |
| `detach` | Detaches from the current session. Alias: `detach`. |
| `detach -P` | Detaches and prints the session name. |
| `kill-session` | Kills the current session. Alias: `kill-session`. |
| `kill-session -t session_name` | Kills a specific session. |
| `kill-session -a` | Kills all sessions except the current one. |
| `switch-client` | Switches to the most recently used session. Alias: `switch`. |
| `switch-client -t session_name` | Switches to a specific session. |
| `switch-client -l` | Switches to the last session. |
| `switch-client -n` | Switches to the next session. |
| `switch-client -p` | Switches to the previous session. |
| `rename-session` | Renames the current session. Alias: `rename`. |
| `rename-session -t old_name new_name` | Renames a session. |
| `new-window` | Creates a new window. Alias: `neww`. |
| `new-window -n window_name` | Creates a new window with a custom name. |
| `new-window -t session_name` | Creates a new window in a specific session. |
| `kill-window` | Kills the current window. Alias: `killw`. |
| `kill-window -t window` | Kills a specific window. |
| `next-window` | Selects the next window. Alias: `nextw`. |
| `previous-window` | Selects the previous window. Alias: `prevw`. |
| `last-window` | Selects the last window. Alias: `lastw`. |
| `select-window` | Selects a window by index. Alias: `selectw`. |
| `select-window -t window_index` | Selects a window by index. |
| `select-window -n` | Selects the next window. |
| `select-window -p` | Selects the previous window. |
| `select-window -l` | Selects the last window. |
| `swap-window` | Swaps two windows. Alias: `swapw`. |
| `swap-window -s source_window -t target_window` | Swaps two windows. |
| `move-window` | Moves a window to a different session. Alias: `movew`. |
| `move-window -t target_session` | Moves the current window to a different session. |
| `link-window` | Links a window to another session. Alias: `linkw`. |
| `link-window -s source_window -t target_session` | Links a window to another session. |
| `unlink-window` | Unlinks a window from a session. Alias: `unlinkw`. |
| `unlink-window -t window` | Unlinks a specific window. |
| `rename-window` | Renames the current window. Alias: `renamew`. |
| `rename-window -t window new_name` | Renames a window. |
| `split-window` | Splits the current pane. Alias: `splitw`. |
| `split-window -h` | Splits the current pane horizontally. |
| `split-window -v` | Splits the current pane vertically. |
| `split-window -t target_pane` | Splits a specific pane. |
| `kill-pane` | Kills the current pane. Alias: `killp`. |
| `kill-pane -t pane` | Kills a specific pane. |
| `select-pane` | Selects a pane. Alias: `selectp`. |
| `select-pane -t pane_index` | Selects a pane by index. |
| `select-pane -U` | Selects the pane above. |
| `select-pane -D` | Selects the pane below. |
| `select-pane -L` | Selects the pane to the left. |
| `select-pane -R` | Selects the pane to the right. |
| `swap-pane` | Swaps two panes. Alias: `swapp`. |
| `swap-pane -s source_pane -t target_pane` | Swaps two panes. |
| `move-pane` | Moves a pane to a new position. Alias: `movep`. |
| `move-pane -t target_pane` | Moves the current pane to a new position. |
| `resize-pane` | Resizes a pane. Alias: `resizep`. |
| `resize-pane -t pane -x width` | Resizes a pane horizontally. |
| `resize-pane -t pane -y height` | Resizes a pane vertically. |
| `resize-pane -t pane -L 5` | Resizes a pane by moving its left border 5 cells to the left. |
| `resize-pane -t pane -R 5` | Resizes a pane by moving its right border 5 cells to the right. |
| `resize-pane -t pane -U 5` | Resizes a pane by moving its top border 5 cells up. |
| `resize-pane -t pane -D 5` | Resizes a pane by moving its bottom border 5 cells down. |
| `break-pane` | Breaks a pane off into a new window. Alias: `breakp`. |
| `break-pane -t pane` | Breaks a specific pane into a new window. |
| `join-pane` | Joins a pane into a window. Alias: `joinp`. |
| `join-pane -t target_pane` | Joins the current pane into a target pane. |
| `select-layout` | Applies a specific layout. Alias: `selectl`. |
| `select-layout -t window layout_name` | Applies a specific layout to a window. |
| `select-layout -n` | Applies the next layout. |
| `select-layout -p` | Applies the previous layout. |
| `next-layout` | Applies the next layout. Alias: `nextl`. |
| `previous-layout` | Applies the previous layout. Alias: `prevl`. |
| `rotate-window` | Rotates the panes in a window. |
| `rotate-window -D` | Rotates window down. |
| `rotate-window -U` | Rotates window up. |
| `balance-window` | Balances the sizes of panes in a window. |
| `list-sessions` | Lists all sessions. Alias: `ls`. |
| `list-windows` | Lists all windows in the current session. Alias: `lsw`. |
| `list-panes` | Lists all panes in the current window. Alias: `lsp`. |
| `list-clients` | Lists all connected clients. Alias: `lsc`. |
| `list-buffers` | Lists all paste buffers. Alias: `lsb`. |
| `list-keys` | Lists all key bindings. Alias: `lk`. |
| `list-commands` | Lists all available commands. Alias: `lscm`. |
| `show-options` | Shows options. Alias: `show`. |
| `show-options -g` | Shows global options. |
| `show-options -t session_name` | Shows options for a specific session. |
| `set-option` | Sets an option. Alias: `set`. |
| `set-option -g option value` | Sets a global option. |
| `set-window-option` | Sets a window option. Alias: `setw`. |
| `set-window-option -g option value` | Sets a global window option. |
| `set-hook` | Sets a hook. Alias: `sethook`. |
| `set-hook -g hook_name command` | Sets a global hook. |
| `run-shell` | Runs a shell command when a hook is triggered. Alias: `run`. |
| `run-shell -g command` | Runs a shell command globally. |
| `send-keys` | Sends keys to a pane. |
| `send-keys -t session_name:window.pane "command"` | Sends keys to a specific pane. |
| `send-keys -t session_name C-c` | Sends Ctrl+C to a session. |
| `send-prefix` | Sends the prefix key to a session. |
| `display-message` | Displays a message. Alias: `display`. |
| `display-message -t session_name "message"` | Displays a message in a session. |
| `display-panes` | Displays all panes in a session. Alias: `displayp`. |
| `copy-mode` | Enters copy mode. |
| `copy-mode -t session_name:window.pane` | Enters copy mode in a specific pane. |
| `paste-buffer` | Pastes from the paste buffer. Alias: `pasteb`. |
| `paste-buffer -t target_pane` | Pastes from the paste buffer to a specific pane. |
| `save-buffer` | Saves the contents of a paste buffer to a file. Alias: `saveb`. |
| `save-buffer -b buffer_name file` | Saves the contents of a specific paste buffer to a file. |
| `load-buffer` | Loads the contents of a file into a paste buffer. Alias: `loadb`. |
| `load-buffer file` | Loads the contents of a file into a paste buffer. |
| `delete-buffer` | Deletes a paste buffer. Alias: `deleteb`. |
| `delete-buffer -b buffer_name` | Deletes a specific paste buffer. |
| `choose-buffer` | Interactively selects a paste buffer to insert. Alias: `chooseb`. |
| `clock-mode` | Enters clock mode. |
| `clock-mode -t session_name:window` | Enters clock mode in a specific window. |
| `refresh-client` | Refreshes the current client. Alias: `refresh`. |
| `refresh-client -t session_name` | Refreshes a specific client. |
| `suspend-client` | Suspends the current client. Alias: `suspendc`. |
| `suspend-client -t session_name` | Suspends a specific client. |
| `lock-client` | Locks the current client. Alias: `lockc`. |
| `lock-session` | Locks all clients in the current session. Alias: `lock`. |
| `lock-server` | Locks all clients on the server. Alias: `locks`. |
| `kill-server` | Kills the tmux server and all sessions. |
| `has-session` | Checks if a session exists. |
| `has-session -t session_name` | Checks if a specific session exists. |
| `server-info` | Shows information about the tmux server. |

---
## Format Variables

| Code | Description |
|------|-------------|
| `#{session_name}` | Name of the session. |
| `#{session_id}` | ID of the session. |
| `#{session_created}` | Time when the session was created. |
| `#{session_last_attached}` | Time when the session was last attached. |
| `#{session_last_activity}` | Time of last activity in the session. |
| `#{session_activity}` | Activity status of the session. |
| `#{session_attached}` | Number of clients attached to the session. |
| `#{session_group}` | Group of the session. |
| `#{session_group_list}` | List of sessions in the same group. |
| `#{session_groups}` | List of groups the session is in. |
| `#{session_windows}` | Number of windows in the session. |
| `#{session_path}` | Working directory of the session. |
| `#{session_user}` | User of the session. |
| `#{session_tty}` | Controlling terminal of the session. |
| `#{window_name}` | Name of the window. |
| `#{window_index}` | Index of the window. |
| `#{window_id}` | ID of the window. |
| `#{window_panes}` | Number of panes in the window. |
| `#{window_active}` | Whether the window is active. |
| `#{window_last_activity}` | Time of last activity in the window. |
| `#{window_activity}` | Activity status of the window. |
| `#{window_bell}` | Whether the window has a bell. |
| `#{window_silence}` | Whether the window is silenced. |
| `#{window_flags}` | Flags of the window. |
| `#{window_layout}` | Layout of the window. |
| `#{pane_id}` | ID of the pane. |
| `#{pane_index}` | Index of the pane. |
| `#{pane_current_path}` | Current working directory of the pane. |
| `#{pane_current_command}` | Current command running in the pane. |
| `#{pane_pid}` | PID of the shell in the pane. |
| `#{pane_title}` | Title of the pane. |
| `#{pane_width}` | Width of the pane. |
| `#{pane_height}` | Height of the pane. |
| `#{pane_left}` | Left position of the pane. |
| `#{pane_top}` | Top position of the pane. |
| `#{pane_right}` | Right position of the pane. |
| `#{pane_bottom}` | Bottom position of the pane. |
| `#{pane_dead}` | Whether the pane is dead. |
| `#{pane_dead_status}` | Status of the pane if dead. |
| `#{pane_exit_code}` | Exit code of the pane's command. |
| `#{pane_last_command}` | Last command run in the pane. |
| `#{client_name}` | Name of the client. |
| `#{client_id}` | ID of the client. |
| `#{client_pid}` | PID of the client. |
| `#{client_user}` | User of the client. |
| `#{client_tty}` | Terminal of the client. |
| `#{client_width}` | Width of the client. |
| `#{client_height}` | Height of the client. |
| `#{client_termname}` | Terminal name of the client. |
| `#{client_termtype}` | Terminal type of the client. |
| `#{client_session}` | Session of the client. |
| `#{client_last_session}` | Last session of the client. |
| `#{client_activity}` | Activity status of the client. |
| `#{buffer_name}` | Name of the paste buffer. |
| `#{buffer_size}` | Size of the paste buffer. |
| `#{buffer_created}` | Time when the paste buffer was created. |
| `#{line}` | Current line number in copy mode. |
| `#{column}` | Current column number in copy mode. |
| `#{cursor_x}` | X position of the cursor in copy mode. |
| `#{cursor_y}` | Y position of the cursor in copy mode. |
| `#{scroll_region_up}` | Top of the scroll region in copy mode. |
| `#{scroll_region_down}` | Bottom of the scroll region in copy mode. |
| `#{search_match}` | Current search match in copy mode. |
| `#{wrap_flag}` | Whether text is wrapped in copy mode. |
| `#{insert_flag}` | Whether insert mode is active in copy mode. |
| `#{alternate_on}` | Whether alternate screen is active. |
| `#{alternate_saved_x}` | Saved X position when alternate screen is active. |
| `#{alternate_saved_y}` | Saved Y position when alternate screen is active. |

---
## Color Variables

| Code | Description |
|------|-------------|
| `colour0` | Black. |
| `colour1` | Red. |
| `colour2` | Green. |
| `colour3` | Yellow. |
| `colour4` | Blue. |
| `colour5` | Magenta. |
| `colour6` | Cyan. |
| `colour7` | White. |
| `colour8` | Bright black (gray). |
| `colour9` | Bright red. |
| `colour10` | Bright green. |
| `colour11` | Bright yellow. |
| `colour12` | Bright blue. |
| `colour13` | Bright magenta. |
| `colour14` | Bright cyan. |
| `colour15` | Bright white. |
| `colour16` | Default background color. |
| `colour17` | Default foreground color. |
| `colour18` | Default cursor color. |
| `colour19` | Default mouse foreground color. |
| `colour20` | Default mouse background color. |
| `colour21` | Default mouse cursor color. |
| `colour256` | 256-color mode. |
| `#RRGGBB` | Hexadecimal color (e.g., `#FF0000` for red). |
| `rgb:RR/GG/BB` | RGB color (e.g., `rgb:FF/00/00` for red). |
| `default` | Default color. |
| `terminal` | Terminal's default color. |

---
## Attribute Variables

| Code | Description |
|------|-------------|
| `none` | No attributes. |
| `bold` | Bold text. |
| `dim` | Dim text. |
| `underscore` | Underlined text. |
| `blink` | Blinking text. |
| `reverse` | Reverse video text. |
| `hidden` | Hidden text. |
| `italics` | Italic text. |
| `strikeout` | Strikeout text. |

---
## Environment Variables

| Code | Description |
|------|-------------|
| `TMUX` | Path to the tmux server socket. |
| `TMUX_PANE` | Pane ID of the current pane. Format: `%session_name:%window_index.%pane_index`. |
| `TMUX_WINDOW` | Window ID of the current window. Format: `%session_name:%window_index`. |
| `TMUX_SESSION` | Name of the current session. |
| `TMUX_VERSION` | Version of tmux. |
| `TMUX_SUDO` | Set to `1` if tmux was started with sudo. |
| `TERM` | Terminal type (usually `screen` or `screen-256color`). |
| `TERMCAP` | Terminal capabilities. |
| `COLUMNS` | Number of columns in the terminal. |
| `LINES` | Number of lines in the terminal. |
| `PWD` | Current working directory. |
| `SHLVL` | Shell level. |
| `HOME` | Home directory of the user. |
| `USER` | Username of the current user. |
| `LOGNAME` | Login name of the current user. |
| `SHELL` | Path to the user's shell. |
| `PATH` | Search path for commands. |

---
## Configuration File Commands

| Code | Description |
|------|-------------|
| `set-option -g option value` | Sets a global option in the configuration file. |
| `set-option -t session_name option value` | Sets an option for a specific session. |
| `set-window-option -g option value` | Sets a global window option. |
| `set-environment -g VAR value` | Sets a global environment variable. |
| `set-environment -t session_name VAR value` | Sets an environment variable for a specific session. |
| `bind-key key command` | Binds a key to a command. |
| `bind-key -n key command` | Binds a key to a command with a note. |
| `bind-key -r key command` | Binds a key to a command with repeat enabled. |
| `bind-key -T prefix key command` | Binds a key to a command for a specific terminal type. |
| `unbind-key key` | Unbinds a key. |
| `set-hook -g hook_name command` | Sets a global hook. |
| `set-hook -t session_name hook_name command` | Sets a hook for a specific session. |
| `run-shell command` | Runs a shell command when a hook is triggered. |
| `run-shell -g command` | Runs a shell command globally. |
| `new-session -s session_name` | Creates a new session at startup. |
| `source-file file` | Sources another configuration file. |
| `source-file ~/.tmux.conf` | Sources the default configuration file. |
| `set-option -g prefix C-a` | Changes the prefix key to Ctrl+a. |
| `unbind-key C-b` | Unbinds the default prefix key. |
| `bind-key C-b send-prefix` | Binds Ctrl+b to send the prefix key. |
| `bind-key C-a send-prefix` | Binds Ctrl+a to send the prefix key. |
| `set-option -g base-index 1` | Changes the base index for windows and panes to 1. |
| `set-option -g pane-base-index 1` | Changes the base index for panes to 1. |
| `set-option -g bell-action none` | Disables the terminal bell. |
| `set-option -g visual-activity on` | Enables visual activity notification. |
| `set-option -g visual-bell on` | Enables visual bell notification. |
| `set-option -g visual-silence on` | Enables visual silence notification. |
| `set-option -g default-command "bash"` | Sets the default command for new windows. |
| `set-option -g default-path "/home/user"` | Sets the default path for new windows. |
| `set-option -g display-time 2000` | Sets the display time for messages in milliseconds. |
| `set-option -g escape-time 500` | Sets the escape time in milliseconds. |
| `set-option -g history-limit 10000` | Sets the maximum number of lines in the scrollback buffer. |
| `set-option -g buffer-limit 50` | Sets the maximum number of paste buffers. |
| `set-option -g repeat-time 500` | Sets the repeat time for key repeats in milliseconds. |
| `set-option -g status on` | Enables the status bar. |
| `set-option -g status off` | Disables the status bar. |
| `set-option -g status-interval 1` | Sets the status bar refresh interval in seconds. |
| `set-option -g status-justify centre` | Centers the status bar. |
| `set-option -g status-left ""` | Clears the left side of the status bar. |
| `set-option -g status-right ""` | Clears the right side of the status bar. |
| `set-option -g status-left-length 20` | Sets the length of the left side of the status bar. |
| `set-option -g status-right-length 50` | Sets the length of the right side of the status bar. |
| `set-option -g status-bg colour0` | Sets the background color of the status bar. |
| `set-option -g status-fg colour7` | Sets the foreground color of the status bar. |
| `set-option -g status-attr dim` | Sets the attribute of the status bar to dim. |
| `set-window-option -g window-status-current-bg colour2` | Sets the background color of the current window in the status bar. |
| `set-window-option -g window-status-current-fg colour0` | Sets the foreground color of the current window in the status bar. |
| `set-window-option -g window-status-current-attr bold` | Sets the attribute of the current window in the status bar. |
| `set-window-option -g window-status-bg colour0` | Sets the background color of windows in the status bar. |
| `set-window-option -g window-status-fg colour7` | Sets the foreground color of windows in the status bar. |
| `set-window-option -g window-status-attr none` | Sets the attribute of windows in the status bar. |
| `set-option -g pane-border-status off` | Disables pane border status indicators. |
| `set-option -g pane-border-status top` | Shows pane border status at the top. |
| `set-option -g pane-border-light` | Uses light pane borders. |
| `set-option -g pane-border-dark` | Uses dark pane borders. |
| `set-option -g pane-border-bg colour0` | Sets the background color of pane borders. |
| `set-option -g pane-border-fg colour7` | Sets the foreground color of pane borders. |
| `set-option -g mouse on` | Enables mouse support. |
| `set-option -g mouse off` | Disables mouse support. |
| `set-option -g mouse-resize on` | Enables mouse resize support. |
| `set-option -g mouse-sb on` | Enables mouse scrollback support. |
| `set-option -g mode-keys vi` | Uses vi key bindings in copy mode. |
| `set-option -g mode-keys emacs` | Uses emacs key bindings in copy mode. |
| `set-option -g history-limit 10000` | Sets the scrollback buffer size. |
| `set-option -g buffer-limit 50` | Sets the maximum number of paste buffers. |

---
## Common Configuration Examples

| Code | Description |
|------|-------------|
| `set-option -g prefix C-a` | Changes the prefix key to Ctrl+a. |
| `unbind-key C-b` | Unbinds the default prefix key. |
| `bind-key C-b send-prefix` | Binds Ctrl+b to send the prefix key. |
| `bind-key C-a send-prefix` | Binds Ctrl+a to send the prefix key. |
| `bind-key -n C-h select-pane -L` | Binds Ctrl+h to select the pane to the left. |
| `bind-key -n C-j select-pane -D` | Binds Ctrl+j to select the pane below. |
| `bind-key -n C-k select-pane -U` | Binds Ctrl+k to select the pane above. |
| `bind-key -n C-l select-pane -R` | Binds Ctrl+l to select the pane to the right. |
| `bind-key -n C-n next-window` | Binds Ctrl+n to select the next window. |
| `bind-key -n C-p previous-window` | Binds Ctrl+p to select the previous window. |
| `bind-key -n C-c new-window` | Binds Ctrl+c to create a new window. |
| `bind-key -n C-v split-window -v` | Binds Ctrl+v to split the window vertically. |
| `bind-key -n C-s split-window -h` | Binds Ctrl+s to split the window horizontally. |
| `bind-key -n C-x kill-pane` | Binds Ctrl+x to kill the current pane. |
| `bind-key -n C-q confirm-before -p "kill-pane #P? (y/n)" kill-pane` | Binds Ctrl+q to kill the current pane with confirmation. |
| `bind-key -n C-r source-file ~/.tmux.conf` | Binds Ctrl+r to reload the configuration file. |
| `bind-key -n C-f command-prompt -p "Find: " "send-keys -t '#{pane_id}' '/%1' C-m"` | Binds Ctrl+f to search in the current pane. |
| `set-option -g status on` | Enables the status bar. |
| `set-option -g status-position top` | Sets the status bar position to top. |
| `set-option -g status-position bottom` | Sets the status bar position to bottom. |
| `set-option -g status-interval 1` | Sets the status bar refresh interval to 1 second. |
| `set-option -g status-justify centre` | Centers the status bar. |
| `set-option -g status-left-length 20` | Sets the left status length to 20 characters. |
| `set-option -g status-right-length 50` | Sets the right status length to 50 characters. |
| `set-option -g status-left "[#S] "` | Sets the left status to show the session name. |
| `set-option -g status-right "#[align=right]#[fg=colour233]#H #[fg=colour255]%H:%M #[fg=colour237]%d %b %Y #[fg=colour245]#[default]"` | Sets the right status to show host, time, date, and battery. |
| `set-window-option -g window-status-format "#I:#W"` | Sets the window status format. |
| `set-window-option -g window-status-current-format "#[bold]#I:#W#[default]"` | Sets the current window status format. |
| `set-option -g pane-border-status off` | Disables pane border status indicators. |
| `set-option -g pane-border-status top` | Shows pane border status at the top. |
| `set-option -g pane-border-light` | Uses light pane borders. |
| `set-option -g mouse on` | Enables mouse support. |
| `set-option -g mouse-resize on` | Enables mouse resize support. |
| `set-option -g mouse-sb on` | Enables mouse scrollback support. |
| `set-option -g history-limit 10000` | Sets the scrollback buffer size to 10000 lines. |
| `set-option -g buffer-limit 50` | Sets the maximum number of paste buffers to 50. |