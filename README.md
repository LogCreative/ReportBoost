# ReportBoost
A LaTeX IDE for a faster compiling speed.

本存储库遵循 [随便TM](LICENSE) 开源协议。

## 简明使用方法
1. 使用 VS Code 打开本文件夹。
2. 使用 Receipe: recompile header 编译 [template](template.tex) 以获得静态依赖缓存，以 `.fmt` 结尾。
3. 使用 Receipe: latexmk 编译 [project1/project1](project1/project1.tex) 即可使用该缓存。文件的第一行表明了需要使用的缓存地址，`\endofdump` 表明了静态依赖库的使用结束位置，之后为你需要为该文档新加入的导言区内容。

## 路线图

- [x] 采用 `mylatexformat` 对模板的依赖进行存储，这样可以减少编译时寻找库所花费的时间，并且可以免除以前的局部依赖文档类不能在同一个文件夹的问题。
- [x] 兼容于 tikz `external` 库用于缓存 tikz 图像。
- [ ] 多线程
- [ ] xelatex 支持与 CI 集成
- [ ] 集成脚本