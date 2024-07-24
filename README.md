<!-- markdownlint-disable MD033 MD041 -->

<div align="center">

# MAA-NIKKE-Copilot 

</div>

## 已完成功能

- [x] 启动App进入大厅 
- [x] 拦截战
```mermaid
flowchart LR
	A[方舟] -->|IN| B(拦截战)-->|IN|C(特殊拦截战)-->D{是否可以快速战斗}-->|是|E(快速战斗)

  E-->D

  D-->|否|F{是否已经全部完成}
  F-->|是，返回到拦截战页面|B
  B-->|OUT|A

  F-->|否|G(战斗)-->D
```
- [x] 模拟室
```mermaid
flowchart LR
	A[方舟] -->|IN| B(模拟室)-->|IN|C(开始模拟)-->D(选择难度)-->E(选择地区)-->F(开始模拟)-->Z{是否完成模拟}-->|NO|G{是否可以挑选战斗节点}-->|Y|H(挑选HARD,NORMAL)-->I{是否可以快速战斗}-->|Y|J(快速战斗)

  J-->Z

  G-->|否|K{是否可以挑选增益}-->|Y|L(挑选EPIC\SSR\SR\R)-->Z

  Z-->|YES|Y(FINSH 模拟)-->A

  K-->|NO|X{是否可以选择特殊节点}-->|YES|P(选择属性提升)-->Z

```
- [x] 每日友情点
- [x] 基地奖励

## 待完成功能

- [ ] 活动：完成战斗
- [ ] 领取邮箱奖励
- [ ] 无限之塔
- [ ] 前哨基地派遣
- [ ] 咨询
- [ ] 解放室

## 致谢

本仓库为 [MaaFramework](https://github.com/MaaXYZ/MaaFramework) 所提供的项目模板，开发者可基于此模板直接创建自己的 MaaXXX 项目。MaaFramework 的 [Release 包](https://github.com/MaaXYZ/MaaFramework/releases)，解压到 `deps` 文件夹中

  ```bash
    # 配置 git 信息（仅第一次需要，后续不用再配置）
    git config user.name "您的 GitHub 昵称"
    git config user.email "您的 GitHub 邮箱"
    
    # 提交修改
    git add .
    git commit -m "XX 新功能"
    git push origin HEAD -u
 cs
    # CI 检测到 tag 会自动进行发版
    git tag v1.0.0
    git push origin v1.0.0
```

调试工具：[MaaDebugger](https://github.com/MaaXYZ/MaaDebugger)
```
python -m MaaDebugger
```
```
#获取当前app包名
adb shell "dumpsys window w |grep \/ |grep name="

adb shell screencap -p /sdcard/screen.png
adb pull /sdcard/screen.png
```
