# packed-bilibili-playinmpv
pack mpv and bilibili-playinmpv together to automate installation using scoop

What should mention is that now CI is not written. this will only be packed by my hand, hence the version may be a little fall behind.

After installation/decompression, you should edit the mpv.reg with the following format and double click on it after saving it to modify the registry file:

```powershell
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\mpv]
"URL Protocol"=""

[HKEY_CLASSES_ROOT\mpv\DefaultIcon]
@="你的MPV安装目录\\mpv.exe,1"

[HKEY_CLASSES_ROOT\mpv\shell]

[HKEY_CLASSES_ROOT\mpv\shell\open]
@=""

[HKEY_CLASSES_ROOT\mpv\shell\open\command]
@="\"你的MPV安装目录\\playinmpv.exe\" \"%1\""


```
