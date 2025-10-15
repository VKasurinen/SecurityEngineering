## Task 1: Safety Concerns 

Companies often prioritize efficiency, speed of innovation and cost efficiency especially under competitive or regulatory pressure. Engineers and Managers may experience normalization of deviance, where minor risks become accepted as normal after repeated exposure without immediate consequences. Additionally, fragmented communication between design, manufacturing, and quality assurance teams can allow emerging issues to go unnoticed. 

Sudden change is typically triggered by high-profile incidents, regulatory intervention, or technological disruption. Catastrophic accidents are usually caused by various equipment faults or errors in planning. Major technological shifts like autonomous driving systems or AI-assisted diagnostics introduce unfamiliar risks that demand new safety frameworks. In both industries, true transformation usually follows moments of crisis that challenge assumptions, reshape public trust, and redefine accountability standards. 


## Task 2: Static and Dynamic Analyzers 

Static analyzers evaluate code without executing it. They inspect source or bytecode to detect potential bugs, vulnerabilities, or code smells by analyzing control flow, data flow, and variable states. In contrast, dynamic analyzers examine code during execution. They monitor runtime behavior to identify memory errors, race conditions, and undefined behavior 

Concolic testing (which is a static analyzer) systematically explores program paths by combining actual program runs with symbolic reasoning. It can find deep logical or path-dependent bugs by automatically generating inputs that trigger rare or complex execution flows. 

Dynamic analyzer for example AddressSanitizer, on the other hand, is a dynamic runtime memory error detector. It instruments compiled code to detect memory leaks, out-of-bounds access, and use-after-free errors efficiently during execution. 


## Task 4: NIS2 & RED 

### Cyber Resilience Act (CRA) 


### Concisely explain the main goal of the directive?  

The CRA aims to ensure that all digital products and connected devices placed on the EU market meet minimum cybersecurity standards throughout their entire lifecycle. 

### Which types of products does it concern?  

The directive applies to all products with digital elements, including hardware, software and operating systems etc. 

### Which types of organizations does it concern?  

It concerns manufacturers, importers, and distributors of digital products within the EU. 


### What kind of cybersecurity measures have to be implemented for a product/organization to comply with the directive?  

Manufacturers must implement secure-by-design and secure-by-default principles, continuous vulnerability handling, and provide security updates throughout the product’s lifecycle. 

 
### When (Date) do organizations/products need to comply with the directive?  

The CRA was formally adopted in March 2024. Organizations have a 36-month transition period, meaning full compliance will be required by 2027. 


### What are possible penalties?  

Non-compliance can result in fines of up to €15 million or 2.5% of global annual turnover, whichever is higher, depending on the severity of the violation. 


### Your own thoughts: How does this benefit you/society overall. Are there positive and negative aspects? 

In my opinion, this regulation benefits society by improving trust in digital products and reducing cyber risks for consumers and businesses. It promotes a higher baseline of security, making connected devices safer. But the downside is that this could potentially slower innovation and potentially rise product prices. 


## Task 5: Showcase 

### Name of the tool  

Shuffle (Open-source SOAR / security automation) 

 

### Link to the tool website/repository  

https://github.com/Shuffle/Shuffle 


### Free or Paid tool? 

Shuffle is free to use (open source) under an open-source license. 

 

### When was the tool created and by who? 

The project’s early origins can be traced to  an Open Source SOAR platform in about 2020 

### Is the tool Open Source?  

Yes,  Shuffle is open source. 

### What is the tool used for?  

Shuffle is used to build, orchestrate, and automate security workflows. It essentially functions as a SOAR tool (Security Orchestration, Automation, and Response), enabling security teams to coordinate between different tools for example alerts, ticketing, scanning and automate response actions. 

 

### What are its capabilities?  

Workflow / Playbook engine -  You can design automation flows via visual editor 

App creator - Users can define their own apps or connectors using OpenAPI definitions. 

App – There are many templates and integrations what you can use. 

 

### Who would most benefit from this tool?  

- Organizations wanting to build or adopt a SOAR without buying expensive commercial licenses.   

- Security engineers / DevSecOps teams who want to codify and scale response workflows. 

- Security Operation Centers or Security teams who face high volumes of alerts and need automation to reduce manual effort. 

### What kind of use case could you yourself have for this tool? 

I could integrate shuffle with Slack or email for notifications. There I could have workflow like this:  

When an alert arrives (some suspicous ip), Shuffle triggers and looks up IP reputation  If the IP is known malicious, automatically add firewall rule blocking. Then there could be automation in slack to let your team members know about this. 

https://medium.com/shuffle-automation/introducing-shuffle-an-open-source-soar-platform-part-1-58a529de7d12  

