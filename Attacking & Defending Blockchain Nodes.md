TODO: Review Rosetta Validator - https://www.rosetta-api.org/docs/1.3.1/validate_correctness.html

TODO: Review Coinbase Salus - https://github.com/coinbase/salus

TODO: Check out GoSec github.com/securego/gosec

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

### Consensus mechanism implementation vulnerabilities 
(Sev: High, Prob: Med)

Blockchain specific vulnerabilities in node software (e.g. block/tx validation, following correct fork, malicious governance upgrade)
- Looking for implementation flaw

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

## Node Host Attacks
(Sev: High, Prob: low)
Malware running on the node host can arbitrarily alter node state and behavior including validating false transactions
injecting false transactions for signing, censoring unwanted transactions, etc..

## Node Admin Attack 
### Compromised Node Admin
- Phsihing, Admin messing with debug settings on node, etc...

## Network Infra Exploitation
(Severity: High, Probability: Medium)

Taking over node's supporting network infra (router, switch, DNS, BGP, etc...) to perform DoS, Eclipse, or other type of attack 




3.) Node Security Threat Model 

Node Software - Consensus Mechanism Impl Vuln Mitigations
- Functional Audits/Source code review of node software
- Node behavior validation and testing (e.g. correct handling of valid and invalid blocks and transactions)

- Fuzzing of blockchain specific node functionality (e.g. block/tx parsing and verification)

4.) Node Security Defense Top 10 

### 1.) Secure Node Software Repo Handling 
Repository Pinning - Only connect to repos you trust, and make it manual it change repo
Version Pinning - Only upgrade to versions which you trust (be deliberate in upgrading)
verification of Signatures - Ensure that the signature is legitimate 

### 2.) Build all nodes from source
Software repo has lots of eyes, but when it's built for different OS's, there can be many steps in the binary creation 
that introduce backdoors. 
- Many more steps in the process 
Same thing for CI Automation

### 3.) Securely Configure Nodes
Diversity Node Connections - diversify the number of connections your node can make, and who it can make those connections to
- this makes us more resiliant against Eclipse attacks, forks, etc...
Lock down RPC Interfaces
- OpenRPC interfaces have been used to steal priv keys

### 4.) Restrict Node Access
Require consensus for administrative tasks
- No one can bring up and down nodes arbitrarily, it requires a consensus of people. 
- More critical infra requires more people
- Define and enforce admin roles - there should be roles for nodes to be able to do certain actions (princ of least priv)
- Restrict Internal Traffic (Ingress and Egress) - your nodes could be used as stepping stones to the rest of your network 

### 5.) Monitor and log node activity 
Investigate network anomalies for Eclipse attacks
- Am I in right fork? Am I being eclipsed? 

Check on block heights and hashes
- Are others still seeing the same thing as you?
- Log all access and network events 

### 6.) Lock down base OS
Dockerize
SE Linux or similar 

### 7.) Harden Node's network connections 
- Harden Network protocols 
(Tls, DNS-Sec)
- DoS Protection 

### 8.) Consider Node/Protocol specific threats
- Stellar trusted nodes configuration 
- EOS trusted modes

### 9.) Verify node functionality before deployment
- Rosetta Validator - https://www.rosetta-api.org




