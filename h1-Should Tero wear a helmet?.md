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


### 1.3

## A) Security Hygiene

## B) Threat model for imaginary company

