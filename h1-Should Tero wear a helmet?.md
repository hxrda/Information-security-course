# H1 Homework

## X) Summaries

### 1.1 Threat modelling manifesto

•	**Definition of thread modelling**  

    - Thread modelling is a process that models and analyses representations of systems to identify and address potential security and privacy concerns associated with them.  
    
•	**Threat modelling process**  

    - At its highest level, attempts to answer 4 key questions:  
      1. What are we working on?  
      2. What can go wrong?  
      3. What are we going to do about it?  
      4. Did we do a good enough job?  
    
•	**Purpose of threat modelling**  

    - Helps identify potential threats or issues to be addressed and mitigated  
    - Informs decision making in system design, development, testing and post-deployment phases     
    - Helps improve security and privacy of a system throughout its development phases and lifetime  
    - Outcomes should provide value to stakeholders, match with relevant development practices and align with the organization’s goals  
    
•	**The threat modelling manifesto**  

    - The manifesto serves as a conceptual guide for refining and producing more effective thread modelling methodologies, suited for individual needs.   
    - The manifesto is a set of ideas, and it is not tied to any specific methodology or framework nor does it provide concrete step-by-step/ how-to guides for thread modelling 
      (cf. Agile principles)  
    - The manifesto defines a list of relative “values”, where items on the left are valued over items on the right:  
        -Finding and fixing design issues over checkbox compliance  
        -People and collaboration over processes, methodologies or tools  
        -Understanding over security or privacy snapshot  
        -Thread modelling implementation over discussions about it  
        -Continuous refinement over single delivery    
    - The manifesto also provides a list of “principles” which serve as axioms/ fundamental truths on which threat modelling is based upon:  
        A) Primary principles that enable successful threat modelling  
        B) Highly recommended patterns  
            - Systematic approach, Informed creativity, Varied viewpoints, Useful toolkit, theory into practice  
        C) Patterns to avoid (anti-patterns)  
            - Hero threat modeler, Admiration of the problem, Overfocus on details, Single perfect representation    
            
•	<ins>**References**</ins>   
    Braiterman et al 2020: [Threat Modeling Manifesto](https://www.threatmodelingmanifesto.org/)

### 1.2 Short Thread Modeling Course – videos  

•	**Definition**  

    - Thread modelling refers to a set of methods that address security concerns associated with a particular system to-be built. 
    
•	**Purpose of thread modeling** 

    - Anticipating problems at a time point when it’s still inexpensive, quick and easy to deal with them (i.e. before implementing or production stage)
    - Allows building more secure systems
    
•	**Process**  

    - Follows a 4-question framework. Threat modelling should answer each of these high-level questions
        1. What are we working on?
            - Tools: Sketching, DFDs (Elements: external entities, processes, data flows, data stores, trust boundaries), Collaboration
            - Requires documentation of record
        2. What can go wrong?
            - Tools: STRIDE (spoofing, tampering, repudiation, information disclosure, DoS, elevation of privileges), Kill chain
            - Threats should be recorded, tracked and treated as development items in the backlog of the design process
        3. What are we going to do about it?
            - Each threat needs an actionable response
            - Example responses: writing a feature, deploying a control, risk management
            - Risk management: 
                - applied to a subset of the discovered threats
                - used to quantify the probability and impact of the threat
                - helps in response planning
                - e.g. techniques: transferring, acceptance
        4. Did we do a good job?
            - Assessing the results e.g. by evaluating whether the threat model can be recommended for use
    - Different models/structures/frameworks/approaches can be used to answer the questions in a more precise and consistent way
    
  •	<ins>**References**</ins>     
    Shostack 2022: [Welcome to the Worlds Shortest Threat Modeling Course](https://www.youtube.com/playlist?list=PLCVhBqLDKoOOZqKt74QI4pbDUnXSQo0nf)


### 1.3 OWASP CheatSheets – Thread Modeling  

•	**Thread modeling definition** 

    -A structured, repeatable process that models a particular system for the purpose of identifying and analyzing the security threats associated with it. The process allows to gain actionable insights into the security characteristics, strengths and gaps, of the particular system being examined. 
    
•	**Advantages of threat modelling** 

    - Allows security to be built-into a system through identifying potential security issues early on during system design
    - Increased security awareness due to requiring critical, creative and collaborative thinking, often incorporating the perspective of the threat actor. 
    - Improves visibility of the target system / target of evaluation (TOE), since it requires deep knowledge of the system’s data flows, trust boundaries etc.
    
•	**The threat modelling process**

    -Analyzes the system from an adversarial security perspective, focusing on how threat actors can exploit systems
    -Threat modeling should be integrated into the SDLC process
    -Threat modeling should be performed early and repeatedly throughout the systems development iterations/ phases and post development. I.e. the model should be continuously 
     updated alongside the system.
     
    - At the high level, should answer 4 key questions:** 
        1. What are we working on?
        2. What can go wrong?
        3. What are we going to do about it?
        4. Did we do a good enough job?
        
    - While there is no single universally accepted standard for the modeling process, most approaches include (refer to 4 key questions):
        1.System modeling
            - Goal: understand the system (data, data flows, data stores, processes, trust boundaries, entities interacting with the system) so that you can understand the 
              threats applicable to it. These often represent potential attack points.
            - Approaches: Data flow diagrams (DFDs), Brainstorming
        2. Threat identification, ranking (probability and impact) & prioritization
            - Done in the context of the system being examined, based on the model
            - Techniques & approaches: STRIDE, ATT&CK, LINDDUN, PASTA, OCTAVE
        3. Risk response & mitigation strategies
            - Goal: defining actionable responses to mitigate each threat identified
            - List of responses:
            - Mitigate, Eliminate, Transfer, Accept
            - Tools for formulating responses: ASVS, CWE list, LINDDUN, PASTA
        4. Review & validation
            - The thread model must be reviewed by all stakeholders
            - Areas of focus:
                - Does the system model reflect the system?
                - Have all threats been identified?
                - For each threat, is there an agreed response strategy
                - Have mitigation or response strategies been properly developed?
                - Has the thread model been formally documented
                - Can responses or mitigations be measured?
                - Are the requirements and recommendations of the thread models measurable (success vs. failure)?

•	**Challenges of threat modelling** 

    - Lack of security knowledge and experience may hinder effective utilization of methodologies and frameworks to identify and model or rank threats and formulate response 
      strategies
    - Thread modelling process is time-consuming and complex
    - Lack of effective communication interdepartmentally, e.g. due to non-shared terminology
    - Fixes:Training, Supportive automation tools, Collaboration & cross-team workshops, Regular reviews

•	<ins>**References**</ins>     
    OWASP CheatSheets Series Team 2021: [Threat Modeling Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html) 

### 1.4 Infosec scene - Darknet Diaries Podcast: Episode 107 on social engineering 

    - The interviewee, Alethe, is a social engineer who professionally attempts to manipulate and trick people to do what she wants them to do, such as   
    provide their passwords or key information which allows her access to confidential data, break into systems or locations. She, and the company she works for  
    (Critical Insight), are looking toward expanding their social engineering activities to include more vishing, phishing and social engineering physicals onsite in the       
    future. Their current clientele includes organizations providing critical infrastructure as well as DoD contractors  
      
    - Her career choice is based on:
        - Her innate ability to read people, a skill she acquired and honed already in her early childhood. As a young child, she learned how to be sneaky,  
        get away with lies and manipulate adults into getting what she wanted. Any mistakes she made, helped her improve the relevant skill early on. 
        - Academics: Later, she also developed an obsession with computer science, tech and coding, which contributed to her choice of career path.
        - Job history: Although she worked at minimum wage jobs during a rough patch in her life, e.g. working in retail taught her new skills on how to deal with  
        customers and improved her social and communication skills. Additionally, another job at a title company allowed her to develop research and OSINT  
        (open source intelligence gathering) skills. A string of other jobs allowed her to further hone her knowledge and capabilities before setting up her own security      
        focused IT company. Later, after her experiences at Defcon, she launched her career officially as a social engineer consultant.
        - Official hacking/ social engineering activities: Around the same time as establishing her IT company, she also learned about Defcon which is the largest annual 
        hacking conference hosted in Las Vegas. She discovered that her accumulated skills all came together under the umbrella of social engineering. At first Alethe was     
        focused on observing other SE hackers and contestants, particularly on the manipulation and coercion side of SE. Observing other social engineers made her realize her
        calling in the field, leading her to take part (and even win) in the SE contests, such as capture the flag competition. The competition mentioned involves capturing
        “flags” which are publicly available information regarding a company, its employees, and company-wide technology in use (such as VPN providers, availability of on-site
        wi-fi, ssid or name of wi-fi, type and version of browser, pdf viewer, model of laptop or computer issued to employees etc.). This information can be found from
        websites, review sites, job descriptions, social media in addition to more detailed snooping, such as Google dorking. The information is used for building rapport,
        impersonation and other manipulative purposes with the target. 
    - Other notes about SE
        - Alethe believes that the skills required for SE also make her a better business owner, communicator, employee, parent and spouse.

•	<ins>**References**</ins>     
    https://darknetdiaries.com/episode/107/ 

### 1.5 Additional questions to consider:

- How to translate the values and principles of the manifesto into concrete step-by-step methodologies that serve individual needs? What are some examples of suitable and successfully field-tested techniques and approaches?
- How to continuously and properly refine the modelling process throughout the development iterations and system’s lifecycle?
- How to properly balance needs for threat modelling & fixing design issues vs. business goals, needs and cost or time constraints?
- What is the sufficient number of viewpoints to be included in each case?
- What are some good sources for learning about SE & how to practice those skills (legally)?

## A) Security Hygiene

•	**List of Basic Security Hygiene practices** 

    - Educate and familiarize necessary parties with common attack vectors.
    - Don’t give away personal data
    - Protect sensitive data at rest and in transit
    - Update software regularly
    - Regularly evaluate & address vulnerabilities and threats (e.g. threat modelling)
    - Implement active inventory/asset control management (IT resources & other enterprise assets, e.g. end-user, network or IoT devices and servers)
    - Apply security configurations to both hardware and software
    - Actively manage backups & data recovery
    - Implement strong identity and access management – IAM. Manage and secure user accounts (strong passwords, 2FA/MFA, principle of least privilege, 
      other access controls, password manager as a supportive tool etc.)
    - Audit log management
    - Be vigilant of suspicious links in various contexts, such as email scams (e.g. phishing attempts)
    - Utilize effective security software and tools, such as anti-malware/virus software and endpoint security solutions across your devices and networks
    - Implement active network monitoring and network security controls, such as firewalls, secure configurations of network devices
    - Use secured VPN & secure access points when connecting to remote networks, such as your corporate’s network.
    - Set up a separate secure network for business transactions or other tasks involving sensitive work data from the network connected to your home devices. 
    - Conduct regular security/penetration testing to identify vulnerabilities
    - Incorporate an incident response and recovery plan in case of an attack occurring to limit the scope of the attack and to minimize downtime


•	<ins>**References**</ins>     
- https://www.fortinet.com/blog/industry-trends/basic-cyber-hygiene-practices-that-go-a-long-way?utm_source=chatgpt.com 
- https://www.avertium.com/blog/understanding-cybersecurity-best-practices?utm_source=chatgpt.com 
- https://www.cisecurity.org/controls/v8-1 
- https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html 


    
## B) Threat model for imaginary company (HeliX)

### **Company description**

    -HeliX is a personal/consumer genomics and biotechnology company based in Finland. The company provides direct-to-consumer DNA testing to generate reports relating to
    a customer’s ancestry and genetic predispositions to health -related topics.  The customers provide a saliva sample in exchange for a personalized report and choose
    whether they want their data kept strictly private or be used anonymized in scientific research. Focusing on security and privacy, HeliX states that customer genetic
    data is protected and used ethically.

### 1. What are we working on?

### 2. What can go wrong?

### 3. What are we going to do about it?

### 4. Did we do good enough job?


•	<ins>**References**</ins>    
- Karvinen 2025 - Information security at https://terokarvinen.com/information-security/#h1-should-tero-wear-a-helmet
- Cyberthreats to Biotechnology 2021 PDF by HHS 
- https://www.researchgate.net/figure/Ethical-aspects-of-the-23andMe-model-and-connections-with-Google-Information-flows_fig3_299521348
- https://threat-modeling.com/threat-modeling-the-23andme-data-breach/
- https://bmcmedethics.biomedcentral.com/articles/10.1186/s12910-016-0101-9
- https://medium.com/@axialxyz/case-study-on-23andme-41f25c885c3c
- https://aws.amazon.com/solutions/case-studies/23andMe-case-study/
- https://en.wikipedia.org/wiki/23andMe_data_leak
- https://www.vice.com/en/article/myheritage-hacked-data-breach-92-million/
- https://www.theverge.com/2018/6/5/17430146/dna-myheritage-ancestry-accounts-compromised-hack-breach
- https://blog.cloudflare.com/bigger-and-badder-how-ddos-attack-sizes-have-evolved-over-the-last-decade/
- https://en.wikipedia.org/wiki/STRIDE_model
- https://en.wikipedia.org/wiki/Threat_actor
- https://www.mitnicksecurity.com/blog/common-hacking-techniques-2023?utm_source=chatgpt.com
- https://www.biospace.com/biopharma-confronts-a-rising-tide-of-ransomware-attacks
- https://www.infosecurity-magazine.com/news/enzo-biochem-hit-ransomware/?utm_source=chatgpt.com
- https://www.tributech.io/blog/how-to-prevent-data-tampering
- https://www.cypressdatadefense.com/blog/data-tampering-prevention/
- https://www.wallarm.com/what/what-is-an-information-disclosure-examples-and-prevention
- https://www.upguard.com/blog/prevent-data-breaches#toc-1  
