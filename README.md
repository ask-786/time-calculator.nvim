# Markdown Time Calculator

**Note:** This plugin is **only** for a very specific use case: calculating daily and grand totals in markdown tables with punch in/out times in the `HH:MM` format. Not recommended for other formats.

---

## Table Format

Your markdown table **must** look like this:

| Date       | In    | Out   | In    | Out   | Total |
| ---------- | ----- | ----- | ----- | ----- | ----- |
| 2025-01-01 | 10:14 | 13:31 | 14:10 | 16:00 | 05:07 |
| 2025-01-02 | 10:14 | 13:31 | 14:10 | 16:00 | 05:07 |
| ...        | ...   | ...   | ...   | ...   | ..... |
| GrandTotal | -     | -     | -     | -     | 10:14 |

- **Time values:** Must be in `HH:MM` format.
- **Empty cells:** Use placeholders like `-`.

---

## Installation

Using [packer.nvim](https://github.com/wbthomason/packer.nvim):

```lua
use 'Ask-786/time-calculator.nvim'
```

---

## Usage

1. Open your markdown file with the table.
2. Press `<leader>tm` (default mapping) to calculate and update totals.

**Custom mapping:**

```lua
require('time-calculator').setup({
  keymap = '<leader>calc',  -- your custom keymap
  mode = 'n',               -- mode for the mapping
  desc = 'Calculate table time',
})
```

---

Use this plugin only for its intended purpose!
