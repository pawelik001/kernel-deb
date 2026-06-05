# 一键更新内核脚本
# 优先使用root账户执行脚本避免不必要的错误！！！
# 从6.18更新到7.0以上需要先手动卸载firmware-xiaomi-raphael.deb再安装对应的firmware-xiaomi-raphael.deb
```bash

# 直接使用GitHub原始链接
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/GengWei1997/kernel-deb/refs/heads/main/Update-kernel.sh)"

# 使用ghproxy加速
sudo bash -c "$(curl -fsSL https://ghfast.top/https://raw.githubusercontent.com/GengWei1997/kernel-deb/refs/heads/main/ghproxy-Update-kernel.sh)"

```

# 更新示例：执行完后出现
```bash
8. 为所有内核生成initramfs镜像
update-initramfs: Generating /boot/initrd.img-7.0.0-sm8150-g7fda0e443cd3
9. 清理旧的启动文件
10. 重命名启动文件
   将最新的initrd.img移动到/boot/initramfs
   已移动: /boot/initrd.img-7.0.0-sm8150-g7fda0e443cd3 -> /boot/initramfs
   将最新的vmlinuz移动到/boot/linux.efi
   已移动: /boot/vmlinuz-7.0.0-sm8150-g7fda0e443cd3 -> /boot/linux.efi
11. 显示/boot目录内容
total 35068
drwx------  5 root root     4096 Jan  1  1970 .
drwxr-xr-x 18 root root     4096 Jun  5 12:51 ..
-rwx------  1 root root  6418190 Jun  5 16:30 System.map-7.0.0-sm8150-g7fda0e443cd3
-rwx------  1 root root   251400 Jun  5 16:30 config-7.0.0-sm8150-g7fda0e443cd3
drwx------  3 root root     4096 Jun  5 17:08 dtbs
drwx------  3 root root     4096 Nov 22  2025 efi
-rwx------  1 root root 15565162 Jun  5 17:08 initramfs
-rwx------  1 root root 13644288 Jun  5 16:30 linux.efi
drwx------  3 root root     4096 Nov 22  2025 loader
=== 验证启动文件 ===
✓ 验证成功：
  - /boot/initramfs 文件存在
  - /boot/linux.efi 文件存在

文件详细信息：
-rwx------ 1 root root 15M Jun  5 17:08 /boot/initramfs
-rwx------ 1 root root 14M Jun  5 16:30 /boot/linux.efi
12. 清理下载的文件
=== 脚本执行完成 ===
```

# 重启手机即可

