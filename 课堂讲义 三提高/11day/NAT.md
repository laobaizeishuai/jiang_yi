## NAT\(网络地址转换器\)

![](/Images/12day/nat.png)

#### 说明

1. 当在家里用宽带链接上网时，会把电话线\(今天很多地方都是光纤\)----&gt;调制解调制\(简称猫\)-------&gt;电脑等设备
2. 电脑会得到来自电信服务商的一个公网ip地址（切记只有公网ip地址才能上网），此时可以直接上网happy...

3. 为了能够让多台设备都可以上网，需要将数据进行“分流”  电话线\(今天很多地方都是光纤\)----&gt;调制解调制\(简称猫\)-------&gt;路由器------&gt;电脑等设备

4. 此时路由器的一端有一个公网ip地址，剩下的4个（路由器型号不同个数不同）可以接入电脑等设备 并且 它们的ip是私有ip\(例如 192.168.1.2\)
5. 当一个电脑（192.168.1.2）上网时，先通过DNS协议解析出某个域名对应的ip，然后
   > * 发送数据时,在经过路由器时转换为公网ip以及路由器自己分配的临时端口
   >
   > 192.168.1.2:6789-----&gt;192.168.1.1 路由器  116.226.52.212:6539-------&gt;猫----&gt;万维网
   >
   > * 接收数据时,在经过路由器时转换为路由器之前记录的ip以及port
   >
   > 万维网-------&gt;猫-----&gt;116.226.52.212:6539 路由器 192.168.1.1 ----&gt;192.168.1.2:6789



