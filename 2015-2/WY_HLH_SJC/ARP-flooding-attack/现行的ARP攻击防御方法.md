# ARP防火墙的分析
 * ARP防火墙不能定位ARP攻击源并对攻击源做相应的处理，网络中依然存在大量虚假的ARP数据包。
     * 分析ARP防火墙的功能：
      * 1.拦截ARP攻击。在系统内核层拦截外部虚假ARP数据包，保障系统不受ARP欺骗,  ARP攻击影响，保持网络畅通及通讯安全;在系统内核层拦截本机对外的ARP攻击数据包，以减少感染恶意程序后对外攻击给用户带来的麻烦;
      * 2.拦截IP冲突。在系统内核层拦截IP冲突数据包，保障系统不受IP冲突攻击的影响;
      * 3. DOS (Denial of Service)攻击抑制。在系统内核层拦截本机对外的TCP SYN/UDP/ICMP/ARP DOS攻击数据包，定位恶意发动DOS攻击的程序，从而保证网络的畅通;
      * 4.安全模式。除了网关外，不响应其它机器发送的ARP请求，达到隐身效果，减少受到ARP攻击的几率;
      * 5. ARP数据分析。分析本机接收到的所有ARP数据包，掌握网络动态，找出潜在的攻击者或中毒的机器;
      * 6.监测ARP缓存。自动监测本机ARP缓存表，如发现网关MAC地址被恶意程序篡改，将报警并自动修复，以保持网络畅通及通讯安全;
      * 7.主动防御。主动与网关保持通讯，通告网关正确的MAC地址，以保持网络畅通及通讯安全;
      * 8.追踪攻击者。发现攻击行为后，自动快速锁定攻击者IP地址;
      * 9. ARP病毒专杀。发现本机有对外攻击行为时，自动定位本机感染的恶意程序、病毒程序。

  * 总结不足：
  
     综上所述，ARP防火墙的功能很强大，但是这种防火墙只能防止单个主机被ARP攻击，而且不能定位ARP攻击源并对攻击源做相应的处理，导致网络中依然存在大量虚假的ARP数据包。
