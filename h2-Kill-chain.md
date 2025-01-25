# H2 Homework

## X) Summary

•	**Key points** 

    - Traditional / conventional security defense tools and response methodologies focus on vulnerabilities and hold the following assumptions: a response 
    should happen after a successful attack and the compromise is the result of a fixable flaw. This “reactive” approach is often ineffective against more 
    sophisticated threats (e.g. APTs), threat actors, tools and techniques. 
    
    - More traditional computer network threats involved automated self-propagating code (viruses, worms etc.), but their risk has been mitigated with 
    conventional anti-virus technology. 
    
    - APT (Advanced Persistent Threats) is a new, more sophisticated class of threats which represents well-resourced and highly skilled attackers who 
    conduct long-term intrusion campaigns targeting highly sensitive information (e.g. economic, proprietary or national security information).
    
    - The Intelligence-driven computer network defense (CND) is a is a risk management strategy / approach that improves security and reduces the 
    likelihood of adversary success by leveraging knowledge gained about these adversaries -> continuous and iterative analysis of attacker behavior 
    from each intrusion attempt (including thinking from the perspective of the adversary), identification of patterns, and predictions of future 
    intrusion attempts. This approach is more “proactive” as it mitigates not only vulnerabilities, but the threat components of a risk as well. 
    
    - Key components of the CND include:
        - Indicators and the indicator lifecycle. Indicators (atomic, computed or behavioral) describe and help detect intrusions. Revelation, maturation 
        and utilization are states of the indicator LC.
        - Intrusion Kill Chain for describing phases of an attack and for developing defensive strategies against the patterns behaviors and tools 
        associated with each phase. Courses of defensive action include: detect, deny,  degrade, deceive, destroy
        - Intrusion Reconstruction which analyzes past intrusions for identifying and addressing security gaps and advance intrusion detection to 
        earlier phases of the Kill Chain. Analysis should include both successful and unsuccessful attempts.

    - The CND utilizes the Kill Chain -model. The model describes distinct phases of an intrusion and maps the key features of each phase to actionable 
    defense responses: detection, mitigation and response. It helps track and stop intrusion attacks at different points of the chain, develop resilient 
    mitigations and intelligently prioritize investments to defense technologies or processes
    
    - In the Kill Chain -model, the attacker must successfully progress through each stage, in order, before reaching their objective. A single mitigation 
    has the potential to disrupt the chain and thus also the attacker. 
    - The stages of the Kill Chain -model include:
        -	Reconnaissance
        -	Weaponization
        -	Delivery
        -	Exploitation
        -	Installation
        -	Command & control (C2)
        -	Actions on objectives

    - One goal of the CND is implementing defensive countermeasures faster than the pace of adversary evolution since it “raises the cost” of intrusion 
    attempts, thus making it a less appealing endeavour.
    - Besides APT & Kill Chains, other phase-based models also exist for defensive and countermeasure strategies for military, counterterrorism or 
    cybersecurity contexts, including: ABSAC, SCP, Ecploitation Life Cycle, and frameworks by US DoD, AF and army. 



•	**Own questions or insights** 

    -	Proper, resilient security measures are multi-layered
    -	How does the Kill Chain -model compare to other cybersecurity models?
    -	How do the current cybersecurity / defensive models fare against AI-driven cyber attacks or could AI be used to enhance detection and aid with disrupting the Kill Chain?
    -	How do APTs adapt to defensive responses based on the Kill Chain -model / CND?


•	<ins>**References**</ins>   
  Hutchins et al 2011: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains
  

## A) MITRE ATT&CK 

•	**The MITRE ATT&CK Framework**  

    - A universally accessible knowledge base of adversary tactics and techniques based on known attack patterns of cybercriminals/ threat actors. 
    It is used for developing treat models and methodologies, detecting, preventing and defending against cybersecurity threats.
    
    - The framework categorizes cybercriminal tactics, techniques and procedures (TTPs) across each phase of the cyberattack lifecycle.
    
    - “ATT&CK” stands for Adversarial tactics, Techniques and Common knowledge


•	**Tactics** 

    - A tactic represents the reason, the “why”, behind an adversary action. I.e., it describes the underlying the objective/goal which 
    the adversary is attempting to achieve by using a technique or sub-technique.
    - Examples
        - Resource development:
            > Involves establishing resources to support attack operations, such as acquiring infrastructure, creating accounts, developing 
            capabilities and malware before attacking. These resources are leveraged throughout the cyberattack chain/lifecycle. More specific 
            implementation examples belong in the domain of techniques.
        - Persistence:
            > Involves maintaining access to a compromised system across restarts, credential changes or other disruptions that could cut off access. 
            This involves techniques associated with replacing or hijacking legitimate code or introducing startup code.
        - Lateral movement:
            > Involves gaining the ability to move within the compromised network beyond the initial access point and the expansion of access to reach 
            additional valuable assets/ resources within the system. The adversaries attempt to reach their objective via pivoting through multiple systems 
            and/or accounts. This lateral movement might be accomplished by utilizing remote access tools or legitimate credentials in the network.
        - Defense evasion:
            > Involves avoiding detection throughout a compromise once inside a target system. It incorporates techniques for abusing trusted processes, 
            hiding or masking malware, uninstalling or disabling security software and/or obscuring or encrypting data and scripts. 


•	**Techniques & Sub-techniques** 

    - A technique represents “how” an adversary achieves a specific tactic (tactical goal). 
    - A sub-technique is a more granular/ specific variation of a technique.
    - Examples
        - T1055 - Process injection technique (Tactics category: Defense evasion, Privilege escalation)
            > Injecting malicious code into legitimate or seemingly benign processes to execute/run code in the context and under the privileges 
            of the other process. This is often done to evade security defenses by masking the malicious code under the legitimate process, for 
            gaining access to the legitimate process’s memory, system or network resources and to elevate privileges.
            > For example, injecting malware into common native built-in Windows processes (explorer.exe, cmd.exe) or other commonly used software 
            such as browsers (chrome.exe), antiviruses (mcafee.exe), office tools (winword.exe) or utilities.
        - T1055.003 – Thread execution hijacking sub-technique (Tactics category: Defense evasion, Privilege escalation)
            > The attacker executes malicious code in the context of an already existing process on the target system to hide malware inside trusted 
            programs/processes. Malicious code is injected into the pre-existing process and execution of one of the threads of that process is forcefully 
            redirected to run the malicious code. The technique is similar to the process hollowing technique, but the latter involves creating a new process 
            in a suspended state instead of using a pre-existing process on the target system.
            > General attack lifecycle: 1.Process handle acquisition, 2.Thread suspension, 3.Memory allocation (for the malicious code), 
            4. Writing shellcode (malicious payload), 5. Hijacking thread context, 6. Context manipulation (changing execution flow of the 
            thread to the malicious code), 7. Thread resumption.


•	**Procedures**

    - A procedure is a specific implementation of a technique or sub-technique used by adversaries. They describe an exact, “in-the-wild”, 
    use of techniques to execute an attack.
    - Examples
        -	For Process injection technique:
                > TrickBot trojan spyware for e.g. using Native API functions to inject code into legitimate processes such as wermgr.exe
                > Wiarp trojan software to create backdoors which remote attackers can use to inject files into running processes
        -	For Thread execution hijacking sub-technique
                > Gazer backdoor to perform thread execution hijacking on a running thread of a remote process
                > Waterbear malware for lateral movement, decrypting, triggering payloads, injecting shellcode into security 
                software processes and hiding network behaviors. 
                > Pikabot for creating a suspended instance of a legitimate process, allocate memory for malicious code and 
                redirecting exeution flow to the malicious code once the thread is resumed.


•	<ins>**References**</ins>   
- MITRE ATT&CK Matrix for Enterprise. https://attack.mitre.org/
- MITRE ATT&CK FAQ https://attack.mitre.org/resources/faq/#general-faq 
- MITRE ATT&CK Tactics: https://attack.mitre.org/tactics/enterprise/ 
- MITRE ATT&CK Techniques https://attack.mitre.org/techniques/enterprise/ 
- https://www.ibm.com/think/topics/mitre-attack 
- https://www.picussecurity.com/resource/t1055-process-injection-of-the-mitre-attck-framework 



## B) Done
