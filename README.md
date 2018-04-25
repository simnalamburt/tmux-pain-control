tmux-pane
========
Tmux plugin for controlling panes. You can install this plugin with [TPM].
```shell
# .tmux.conf
set -g @plugin 'simnalamburt/tmux-pane'
```
This plugin was forked from [tmux-pain-control] and customized for my use cases.

[TPM]: https://github.com/tmux-plugins/tpm
[tmux-pain-control]: https://github.com/tmux-plugins/tmux-pain-control

&nbsp;

Bindings
--------
Notice most of the bindings emulate vim cursor movements.

<img align="right" src="/screenshots/pane_resizing.gif" alt="pane resizing"/>

**Resizing panes**

- `prefix + h`<br/>
  resize current pane 5 cells to the left
- `prefix + j`<br/>
  resize 5 cells in the down direction
- `prefix + k`<br/>
  resize 5 cells in the up direction
- `prefix + l`<br/>
  resize 5 cells to the right

These mappings are `repeatable`.

The amount of cells to resize can be configured with `@pane_resize` option. See
[configuration section](#configuration) for the details.

<br/><br/>

<img align="right" src="/screenshots/pane_splitting.gif" alt="pane splitting"/>

**Splitting panes**

- `prefix + \ `<br/>
  split current pane horizontally
- `prefix + -`<br/>
  split current pane vertically

Newly created pane always has the same path as the original pane.

<br/><br/><br/><br/><br/>

**Swapping windows**

- `prefix + <` - moves current window one position to the left
- `prefix + >` - moves current window one position to the right

&nbsp;

Configuration
--------
You can set `@resize_vertical` and `@resize_horizontal` Tmux option to choose number of resize cells for the
resize bindings.

```shell
set-option -g @resize_vertical "5"       # Default: "3"
set-option -g @resize_horizontal "15"    # Default: "10"
```

&nbsp;

### License
[MIT](LICENSE.md)
