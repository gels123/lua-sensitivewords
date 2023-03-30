# lua-sensitivewords
lua版本敏感词过滤，底层使用go，使用star较多的go实现，性能较高。
编译方法:
cd main && make linux

使用方法：
local lsensitivewords = require("lsensitivewords").new()
local path = require("lfs").currentdir().."/game/lib/lua-golibs/sensitivewords/dict.txt"
lsensitivewords:sensitiveWordLoadDict(path)
print("=============111==", lsensitivewords:sensitiveWordValidate("我嘞个草你妈的B"))
print("=============222==", lsensitivewords:sensitiveWordReplace("00000000000000我嘞个草你妈的B00000000000000", string.byte('*')))
