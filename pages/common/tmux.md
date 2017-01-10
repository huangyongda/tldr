# tmux

> Multiplex several virtual consoles.

- Start a new tmux session:

`tmux`

- Start a new named tmux session:

`tmux new -s {{name}}`

- List sessions:

`tmux ls`

- Attach to a session:

`tmux a`

- Attach to a named session:

`tmux a -t {{name}}`

- Detach from session:

`ctrl+b d`

- Kill session: 结束指定会话

`tmux kill-session -t {{name}}` 

- 选择会话 

`ctrl+b s`

- 选择会话

`ctrl+b w`

- 更改名称

`ctrl+b ,`

- 创建新的子会话

`ctrl+b c`

- 删除当前子会话

`ctrl+b x`
