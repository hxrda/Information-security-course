# H1 Homework

## X) Summaries

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
•	**Tactics** 
•	**Techniques & Sub-techniques** 
•	**Procedures**

•	<ins>**References**</ins>   
- MITRE ATT&CK Matrix for Enterprise. https://attack.mitre.org/
- MITRE ATT&CK FAQ https://attack.mitre.org/resources/faq/#general-faq 
- MITRE ATT&CK Tactics: https://attack.mitre.org/tactics/enterprise/ 
- MITRE ATT&CK Techniques https://attack.mitre.org/techniques/enterprise/ 
- https://www.ibm.com/think/topics/mitre-attack 
- https://www.picussecurity.com/resource/t1055-process-injection-of-the-mitre-attck-framework 



## A) Done
