# CLAD-A-Distributed-Cross-Domain-Covert-Attack-Chain-Targeting-Power-Grid-Control-Logic
CLAD: A Distributed Cross-Domain Covert Attack Chain Targeting Power Grid Control Logic

### File Descriptions

* **`exploit_core.py`**
**PC-Side Attack Engine**: 实现论文 **4.3节** 的认证绕过算法与 **5.2节** 的隐蔽传输逻辑。该脚本利用线性偏移漏洞计算有效 Session Key，并结合令牌桶算法将流量严格整形为 28 PPS，模拟高隐蔽性的初始渗透过程。
* **`packet_def.c`**
**Malformed PDU Definitions**: 定义了用于利用 **4.3.2节** “完整性缺失漏洞”的底层 C 数据结构。展示了如何通过操纵 S7CommPlus 协议中无签名的“Object Property”长度字段，构造语法合法但含有恶意 Shellcode 的畸形数据包。
* **`plc_resident_logic.txt`**
**PLC Resident Malware (SCL/STL)**: 汇编了运行于 PLC 内部的核心恶意代码，涵盖 **Stage III** 的原子化横向移动与异构协议适配逻辑，以及 **Stage IV** 的物理过程劫持（PID Man-in-the-Middle），验证了代码在嵌入式环境下的驻留与破坏能力。
