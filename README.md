# CLAD-A-Distributed-Cross-Domain-Covert-Attack-Chain-Targeting-Power-Grid-Control-Logic
CLAD: A Distributed Cross-Domain Covert Attack Chain Targeting Power Grid Control Logic

### File Descriptions

* **`exploit_core.py`**
**PC-Side Attack Engine**: Implements the authentication bypass algorithm (**Section 4.3**) and stealth transmission logic (**Section 5.2**). This script exploits the linear cryptographic weakness to derive valid session keys and utilizes a token bucket algorithm to shape attack traffic to a covert 28 PPS baseline.
* **`packet_def.c`**
**Malformed PDU Definitions**: Defines the underlying C data structures used to exploit the integrity protection gap (**Section 4.3.2**). It demonstrates how to manipulate the unsigned "Object Property" length field in S7CommPlus headers to construct syntactically valid PDUs that inject malicious shellcode.
* **`plc_resident_logic.txt`**
**PLC Resident Malware (SCL/STL)**: Contains the core resident logic executed inside the PLC. It covers **Stage III** atomic lateral movement with traffic shaping and heterogeneous protocol adaptation, as well as **Stage IV** physical process hijacking (PID Man-in-the-Middle) to cause physical disruption without altering control parameters.
