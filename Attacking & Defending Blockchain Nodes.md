Video: https://www.youtube.com/watch?v=ht-oztt7kns

1.) How many coins do you have?
- Wallet asks the question to the larger cloud...

We trust Node software, libraries and infra not to drop modify, or craft transactions to steal funds

- Devs could be attacked 



BGP network was hijacked to eclipse attack Doge and Bitcoin miner pools

EOS Node code execution vuln. (the first of many hahaha)

Monero - 2019
- Monero Website compromised to serve backdoored client (wallet) stealing funds

Ravencoin 
- Inflation Bug exploited 300M RVN minted

2.) Breaking the nodes

Out of Scope Attacks:
- Consensus Mechanisms, 51% attacs, reorgs, protocol design issue
- Key Mgmgt - handling key material outside of node software
- Incorrect usage - not understanding protocol quireks such as Ripple's tfPartialPayment
- Smart Contacts: Layer 2 vulns in Smart contracts, defi, etc...

In Scope: 
- Implementation - Protocol, software flaws, attack resilience
- Infrastructure - Underlying OS, network stack
- Management - Access management, configuration, source control

What's A threat Model?
- Process to identify potential threats, assess their risk, and prioritize mitigations
- [OWASP Theat Modeling Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html)

Attack Surface:
- Sum of different attack vectors with a threat agent can interact with an environment with 

Threat Agent: 
- An entity that can manifest a threat


![image](https://user-images.githubusercontent.com/25730423/170534821-3e17a821-0aba-4559-a9a8-e4fb2122d5ad.png)

## Node Software Attacks:

### Protocol Vulns 
(Sev: High, Probability: Medium):
- ie Protocol exploit (Send a bad packet to create a buff overflow) 
- Blockchain specific vulns and implementation flaws (block/tx validation, following correct fork, malivious governance upgrades, inflation bugs, etc...)
- Malformed block header that creates 

### Generic Software Vulns
(Sev: High, Probability: High)
- Exploit software that supports the node implementation 
- General software vulns in node software, ie... Parity Web Server, EOS DB, MS 
- Vuln version of NGinx

## Software Repository Attacks
### Node Repo Compromised 
(Severity: High, Probability: High)
Backdoored node software from a compromised or untrusted resource results in unwanted behavior (Monero Key Stealing, Ravencoin Money Printing)

### Software Dependencies 
(Severity: High, Probability: High)
Supply chain attack on a critical component of the node software (encryption or consensus lib)
Results in unwanted node behavior 

## Node Admin Attack s
### Compromised Node Admin
- Phsihing, Admin messing with debug settings on node, etc...

## Network Infra Exploitation
(Severity: High, Probability: Medium)

Taking over node's supporting network infra (router, switch, DNS, BGP, etc...) to perform DoS, Eclipse, or other type of attack 




3.) Node Security Threat Model 

4.) Node Security Defense Top 10 
