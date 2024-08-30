### 常用命令

```bash
# 配置 git 信息（仅第一次需要，后续不用再配置）
git config user.name "您的 GitHub 昵称"
git config user.email "您的 GitHub 邮箱"

# 提交修改
git add .
git commit -m "XX 新功能"
git push origin HEAD -u

# CI 检测到 tag 会自动进行发版
git tag v1.0.0
git push origin v1.0.0

python -m MaaDebugger

python -m pip install MaaDebugger MaaFW --upgrade

#获取当前app包名
adb shell "dumpsys window w |grep \/ |grep name="

adb shell screencap -p /sdcard/screen.png
adb pull /sdcard/screen.png

netstat -ano | findstr :8080
taskkill /F /PID 31952
```
