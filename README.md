
# AXP Format Overview
The AXP (Application eXtreme Properties) format is a straightforward application description model that uses a single JSON file to define an entire application. This format can be used to create webpages, desktop applications, and mobile apps; however, it has limitations and cannot be used to build more complex applications like e-commerce sites or games. AXP primarily focuses on analytics, data editing, and data visualization, allowing systems to represent information that is difficult to convey with words, especially when the data is too large to fit into an Excel spreadsheet. Initially, the goal of AXP was to aid in understanding the results of deep learning, but I now use it to build effective data processing systems, such as my agency management tools and a daily stand-up report system.



# How it works?

The system consists of four modules, divided into two sides and two layers. The sides are the front-end and back-end, which function as separate MVC-like systems. Both can operate in standalone, peer-to-peer (P2P), or swarm modes. The two layers are the data transfer protocol and the data storage layer, with one layer on the front end and two on the back end. Each module has its own submodules. Currently, the front end supports the Hel tools and Vue.js, while the back end only supports Laravel with Eloquent. Future plans include extending support to Express and Panthera.



 Data format:

 Mayor data structure. Every element has 2 different IDs. One is the serial ID that is used inside the module and the uniqeId is the same on every module. 


 Code overwrite:

 Every provided function and class can be overridden. But has some temporary rules. This rule should be changed in the future. The reverse keywords are expectations from these rules.

 -The code override is driven by the variable or the function's first character. You cannot override anything that ends with``` _```. The function that started with ```_``` should be overridden only at a higher level.
 -The functions/classes name words are separated with upper case. ```ThisIsAClass``` ```thisIsAFunction```.
 -The variable name snakifid. ```this_is_a_variable```.
 -Functions that started with Upper case should be managed as a class. 
 -Only class names can start with upper case. NOTHING ELSE CAN START WITH UPPER CASE. In theory, the builder recognizes your mistake. However, that has no guarantee. 



# FAQ


### **Why not YAML?**  

 **Short**: Because it's not.  

 **Long**: Processing YAML is more complex and prone to bugs. Given my limited time and zero budget for this project, I aim to build quickly and with minimal complications.


### **Can I have access to the backend builder?**

 **Short**: Not yet.  

 **Long**: The only existing version is rust-based, which I use for my games, machine learning projects, and job searches. Thus, I cannot open-source it yet. A Python-based version is planned for open source in the future.


### **Can I have access to the frontend builder?** 

 **Short**: Yes, but that should be access over an api soon.
