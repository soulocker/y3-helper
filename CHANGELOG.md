# Change Log

All notable changes to the "y3-helper" extension will be documented in this file.

Check [Keep a Changelog](http://keepachangelog.com/) for recommendations on how to structure this file.

## [Unreleased]

- Initial release

## [2.5.0]

### Added

- 附加调试支持 `skipFiles`：新增设置 `Y3-Helper.DebugSkipFiles`，调试器跳过指定文件/目录（命中帧在堆栈中显示为纯文本行，单步执行跳过）

### Changed

- 不再强制依赖 `sumneko.lua` 扩展（可改用 emmylua 等语言服务；"生成接口文档"命令仍按需要求安装它）
- 不再改写项目的 `.luarc.json`（仅在缺失时复制模板，路径合并逻辑删除）

### Fixed

- 修复 recentOpenFiles 重放打开时因路径大小写不一致在 LSP 产生幽灵文档条目（emmylua duplicate-set-field 误报）