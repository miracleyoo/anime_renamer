# Anime Renamer

本项目用于与utorrent联动，在下载动漫剧集后自动正则匹配并重命名为串流软件（如Plex）支持的格式。

## 使用方法：

1. 与utorrent联动，在`高级-运行程序`中使用命令 `<YOUR_CMD_PATH>\run_after_done.cmd "%F" "%D"` 实现自动重命名。
2. **For Windows:** 直接将整个存放动漫的根文件夹拖放到`rename_episodes.cmd`文件上即可。该文件会调用前面提到的Python脚本，并对整个文件夹中的所有有问题的文件名进行重命名。你也可以将有问题的子目录或特定文件拖放上去，或是同时拖放多个文件/文件夹。Python脚本中有着相应的适配。
3. **For Mac/Linux:** 使用`rename_episodes.sh`，最好将其添加到你的`~/.zshrc`或`~/.bashrc`中，作为一个函数。如`rename-e`，之后只需要在terminal中输入 `rename-e <YOUR_ANIME_FOLDER_PATH>` 即可。