# PYNQ-Pmod-Camera
使用PYNQ做视频/视觉应用的时候，其输入源可以有这么几种
- 板载HDMI In输入，可以使用PC+HDMI线直接作为输入，或者另外购买一个电视盒子作为HDMI输入。还有更多HDMI输入方式也都可以作为视频源
- USB摄像头输入，缺点是USB传输带宽较小
- 本工程中介绍的PMOD摄像头，可以自行淘宝购买

## 资料
百度网盘链接：https://pan.baidu.com/s/1yESFJrVwx1nFKySRridOzw 密码：7h9q
- PYNQ_HDMI_TDM114是TDM114摄像头输入，HDMI输出，需要接在1080P的显示器上
- PYNQ_HDMI_IO是HDMI输入，HDMI输出
- PYNQ_HDMI_4in1在PYNQ_HDMI_IO基础上添加了一个HLS生成的视频处理IP，用Window buffer和linebuffer写的，可以以此为基础自己写视频处理函数
- 4in1.zip是HLS工程，即视频处理IP
- PYNQ2017.4.zip是 PYNQ SDSoC2017.4的platform，只有linux系统，密码是root
- 上电进入系统以后要手动mount SD卡
  ```console
  mount /dev/mmcblk0p1 /mnt
  cd /mnt
  ls
  ```
  就可以看到SD卡存放的文件了
