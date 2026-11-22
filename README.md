# aside

An Emacs popup for coding agents over ACP. Needs Emacs 30.1+ and a signed-in
agent on Emacs's `exec-path`: OpenCode, `claude-agent-acp`, `codex-acp` or Cline.

```elisp
(use-package aside
  :vc (:url "https://github.com/siroccoros/aside" :rev :newest)
  :bind (("C-c o" . aside)
         ("C-c h" . aside-toggle)
         ("C-c r" . aside-resume)))
```

Open a project file, press `C-c o`, write a prompt, then `C-c C-c` to send
(Evil: `:w`). Reply below the answer to continue.

| Popup key | Action |
| --- | --- |
| `C-c C-k` | Stop |
| `C-c C-a` | Switch agent |
| `C-c C-m` / `C-c C-e` | Model / effort |
| `C-c C-l` | Full history |
| `C-c ?` | All keys |

![Permission request](docs/working.png)

Configure with `M-x customize-group RET aside`. For tiling window managers,
float windows whose titles begin with `aside · `.
Update with `M-x package-vc-upgrade RET aside`.

[MIT](LICENSE).
