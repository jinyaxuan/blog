---
id: hex-viewers-and-editors-in-terminal
date: 2019-01-11 10:08:02
title: macOS 终端可用的 Hex 查看与编辑器
categories: Collections
tags: [CLI, macOS]
---

在 Windows 下我们可以使用 WinHex，而在 macOS 平台上，有什么不错的十六进制查看器、编辑器呢？

<!--more-->

## 准备

首先，我们创建一个文件用于测试。

```bash
echo 'welcome' > file1
```

## 正文

### HexDump

很多类 Unix 系统都包含这个工具。正如其名，功能就是导出文件的原始十六进制信息。

```bash
$ hexdump file1
0000000 6577 636c 6d6f 0a65
0000008
```

以上输出就是 `welcome` 的 ASCII 十六进制信息，如果文件很长，那将会很难与文本信息对应起来。

我们可以使用 `-C` 选项来同时打印文本。

```bash
$ hexdump -C file1
00000000  77 65 6c 63 6f 6d 65 0a              |welcome.|
00000008
```

如上，`w` 的十六进制 ASCII 码为 `77`，`e` 为 `65`。

### od

另一个十分常用的工具是 `od`。该工具提供 `-x` 参数用于输出十六进制的文件原始数据。

```bash
$ od -x file1
0000000 6577 636c 6d6f 0a65
0000010
```

同样，为了让输出更加易读，可使用 `-c` 参数输出文本。

```bash
$ od -xc file1
0000000 6577 636c 6d6f 0a65
               w   e   l   c   o   m   e  \n
0000010
```

### xxd

`xxd` 是一个稍特殊的工具，它还提供了一个 `-r` 选项，可将十六进制信息转换回原始文件，可用于编辑 Hex 内容。

```bash
$ xxd file1
0000000: 7765 6c63 6f6d 650a                    welcome.
```

假设我们有 `file2` 文件，内容如下：

```bash
$ cat file2
000000: 7765 6c63 6f6d 650a
```

那么我们可以使用 `-r` 选项来将其转换为原文件内容：

```bash
$ xxd -r file2
welcome
```

### hexyl

[sharkdp/hexyl](https://github.com/sharkdp/hexyl) 是一款使用 Rust 编写的 Hex 查看器，支持高亮不同种类的字节。

它并不常见，是我最近在 GitHub 上发现的一个小工具，前些天上到 Trending 狂揽 1k+ Stars。

```bash
$ hexyl file1
┌────────┬─────────────────────────┬─────────────────────────┬────────┬────────┐
│00000000│ 77 65 6c 63 6f 6d 65 0a ┊                         │welcome_┊        │
└────────┴─────────────────────────┴─────────────────────────┴────────┴────────┘
```

它还支持使用 `-n <N>` 选项来限制仅读取文件的前 `<N>` 个字节。

```bash
$ hexyl -n 2 file1
┌────────┬─────────────────────────┬─────────────────────────┬────────┬────────┐
│00000000│ 77 65                   ┊                         │we      ┊        │
└────────┴─────────────────────────┴─────────────────────────┴────────┴────────┘
```

### Vim

`Vim` 可谓是编辑器界的「重量级武器」了。上文我们介绍的都是 Hex 查看器，不仅如此，Vim 还提供了直接的编辑功能。

使用 Vim 打开文件后，输入 `:% ! xxd` 命令，界面将变成类似如下格式：

```
00000000: 7765 6c63 6f6d 650a                      welcome.
```

接着你可以随意编辑文本了，就像使用 `xxd` 转换后进行编辑修改一样。

完成后，输入 `:%!xxd -r` 命令并保存即可。

## 参考资料

- http://www.theunixschool.com/2011/06/3-different-ways-of-dumping-hex.html
- https://stackoverflow.com/questions/827326/whats-a-good-hex-editor-viewer-for-the-mac
