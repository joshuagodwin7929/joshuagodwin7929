# Okunnuwa Joshua Godwin

**Detection Engineering · SOC · Active Directory Security**

I build Active Directory labs, attack them, and write the detections, then prove the detections actually fire. Everything on this profile is work I've run end to end in my own lab, not notes from a tutorial. Where a technique stayed invisible, the write-up says so and shows how I closed the gap.

My method is the same on every project: **log first, attack second, hunt third, then formalize.** I don't write a detection until I've run the real attack and seen what it looks like in the telemetry.

**Certifications:** CompTIA Security+ · ISC2 Certified in Cybersecurity (CC) · working toward CompTIA CySA+

---

## Featured work

**Start with [AD-Attack-Defense-Lab](https://github.com/joshuagodwin7929/AD-Attack-Defense-Lab)** if you only open one. It's the flagship and the others grow out of it.

| Project | What I did, and what it proves |
|---|---|
| [AD-Attack-Defense-Lab](https://github.com/joshuagodwin7929/AD-Attack-Defense-Lab) | Built an AD domain and a self-hosted Elastic SIEM, then ran a seven-phase attack chain (LLMNR poisoning through Kerberoasting, BloodHound mapping and lateral movement to DCSync and a Golden Ticket). I hunted each step in Kibana, documented exactly where host-based visibility broke, closed the two biggest gaps, and wrote it up as an incident report. |
| [Purple-Team-Automation](https://github.com/joshuagodwin7929/Purple-Team-Automation) | Re-ran the credential-access chain through MITRE Caldera to validate my detections, and confirmed four techniques firing as live Kibana alerts. The re-test also caught and fixed a real bug in one of my own detection rules. Mapped to ATT&CK with a coverage heatmap. |
| [Detection-Engineering](https://github.com/joshuagodwin7929/Detection-Engineering) | Turned the lab's hunt queries into version-controlled Sigma rules, compiled to Elastic/KQL, mapped to MITRE ATT&CK and tuned against deliberate false positives, with a CI check on every push. |
| [Wazuh-SIEM-Lab](https://github.com/joshuagodwin7929/Wazuh-SIEM-Lab) | Custom AD/Kerberos detection rules, Active Response, and CIS hardening on Wazuh, validated with a Caldera purple-team run that found and fixed a real detection gap. |
| [Network-Intrusion-Analysis-Natureforce](https://github.com/joshuagodwin7929/Network-Intrusion-Analysis-Natureforce) | Packet-level investigation with Wireshark and tshark: found the infected host, extracted and verified the malware, measured the follow-on C2 session, and ended with draft Suricata and Sigma rules. |

---

## How I work

- **Build, then break, then detect.** I stand up the environment and the logging first, run real attacks against it, and only then write detections against the telemetry they actually produced.
- **Honest gaps over polished demos.** Two of my attacks left almost nothing in host-based logs. Rather than hide that, I documented why (DS Access auditing off, a forged ticket that only surfaces as a normal logon) and built the fixes.
- **Validate, don't assume.** A detection isn't done until an automated attack trips it. That habit is what caught a rule of mine that had been passing its checks while matching nothing.

---

## Tools I work with

**SIEM and detection:** Elastic Stack (Elasticsearch, Kibana, Logstash) · Wazuh · KQL · Sigma · Winlogbeat

**Endpoint and emulation:** Sysmon · MITRE Caldera · Impacket · NetExec · BloodHound · Responder

**Platforms and frameworks:** Windows Server / Active Directory · Linux · Docker · MITRE ATT&CK

---

## Connect

- LinkedIn: [okunnuwa-joshua-godwin](https://www.linkedin.com/in/okunnuwa-joshua-godwin)
- X: [@247shield](https://x.com/247shield)
