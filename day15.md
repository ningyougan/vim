day15

编辑器切换改键

window: 

关闭当前窗口：ctrl+shift+w 需要改建，因为vim原生支持的ctrl+w功能也有一些可用的地方，比如开发环境分区。这个快捷键原本的作用是关闭vscode编辑器，用不到，直接删掉了替换成了关闭当前窗口。

开关主侧栏：ctrl+b，因为vim的快捷键(回到文件第一个字符位，没啥用，可以用gg)覆盖掉了vscode原生的快捷键，直接把vim的删掉了。

其余的配置如下，window已经用powertoy改键
```json5
//keybindings.json
{
  {
    // window move left
    "key": "shift+left",
    "command": "vim.remap",
    "when": "vim.mode == 'Normal'",
    "args": {
      "after": [
        "<c-w>",
        "h"
      ]
    }
  },
  {
    // window move right
    "key": "shift+right",
    "command": "vim.remap",
    "when": "vim.mode == 'Normal'",
    "args": {
      "after": [
        "<c-w>",
        "l"
      ]
    }
  },
  {
    // window move up
    "key": "shift+up",
    "command": "vim.remap",
    "when": "vim.mode == 'Normal'",
    "args": {
      "after": [
        "<c-w>",
        "k"
      ]
    }
  },
  {
    // window move down
    "key": "shift+down",
    "command": "vim.remap",
    "when": "vim.mode == 'Normal'",
    "args": {
      "after": [
        "<c-w>",
        "j"
      ]
    }
  },
}
```