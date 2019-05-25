## [Requirements - Software Requirements](https://confluence.softserveinc.com/display/AbilitonKnowledgeModel/Software+Requirements)

### Requirement definition 
1. A condition or capability needed by a user to solve a problem or achieve an objective.  
2. A condition or capability that must be met or possessed by a system or system component to satisfy a contract, standard, 
specification, or other formally imposed document.  
3. A documented representation of a condition or capability as in 1 or 2.  

This definition encompasses both the user's view of the requirements and the developer's view.

Requirements are…a specification of what should be implemented. They are descriptions of how the system should behave, 
or of a system property or attribute. They may be a constraint on the development process of the system.  

### Levels of Requirements

#### Business
Business requirements represent high-level objectives of the organization or customer who requests the system.  
Business requirements typically come from the funding sponsor for a project, the acquiring customer, 
the manager of the actual users, the marketing department, or a product visionary.  
Business requirements describe why the organization is implementing the system—the objectives the organization hopes to achieve.  
I like to record the business requirements in a vision and scope document, 
sometimes called a project charter or a market requirements document.   

#### User
User requirements describe user goals or tasks that the users must be able to perform with the product.  
Valuable ways to represent user requirements include use cases, scenario descriptions, and event-response tables.  
User requirements therefore describe what the user will be able to do with the system.  
An example of a use case is "Make a Reservation" using an airline, a rental car, or a hotel Web site.  

#### Functional requirements 
A functional requirement describes what a software system should do, 
while non-functional requirements place constraints on how the system will do so.  
The functional requirement is describing the behavior of the system as it relates to the system's functionality. The non-functional requirement elaborates a performance characteristic of the system.  

Typically non-functional requirements fall into areas such as:
* Accessibility
* Documentation
* recovery
* Fault tolerance
* Maintainability
* Privacy
* Reliability
* Resilience
* Response time
* Scalability
* Security
* Stability

Functional requirements specify the software functionality that the developers must build into the product 
to enable users to accomplish their tasks, thereby satisfying the business requirements.  
Sometimes called behavioral requirements, these are the traditional "shall" statements: 
"The system shall e-mail a reservation confirmation to the user."  
Functional requirements describe what the developer needs to implement.  
The term system requirements describes the top-level requirements for a product that contains multiple subsystems.  
Documented in a software requirements specification (SRS).  


#### Most common requirements risks 
* Insufficient User Involvement  
Customers often don't understand why it is so essential to work hard on gathering requirements and assuring their quality. 
Developers might not emphasize user involvement, either because working with users isn't as much fun as writing code or 
because they think they already know what the users need.

* Creeping User Requirements  
Scope creep. Constant requirements modifications make the problem worse. 
The problem lies partly in the users' frequent requests for changes in the requirements and partly in the way 
that developers respond to these requests.  

* Ambiguous Requirements  
Reader can interpret a requirement statement in several ways.  

* Gold Plating  
Gold plating takes place when a developer adds functionality that wasn't in the requirements specification but that 
the developer believes "the users are just going to love."   

* Minimal Specification  
* Overlooked User Classes 

* Inaccurate Planning  

#### Characteristics of Excellent Requirements 
Requirement Statement Characteristics  

* Complete - Each requirement must fully describe the functionality to be delivered.  
* Correct - Each requirement must accurately describe the functionality to be built.  
* Feasible - It must be possible to implement each requirement within the known capabilities and limitations of the system and its operating environment.  
* Necessary - Each requirement should document a capability that the customers really need or one that's required for conformance to an external system requirement or a standard.  
* Prioritized - Assign an implementation priority to each functional requirement.  
* Unambiguous - All readers of a requirement statement should arrive at a single, consistent interpretation of it, but natural language is highly prone to ambiguity.  
* Verifiable - See whether you can devise a few tests or use other verification approaches, such as inspection or demonstration, to determine whether the product properly implements each requirement.  

It's not enough to have excellent individual requirement statements.  
Sets of requirements that are collected into a specification ought to exhibit the characteristics described in the following sections.  

Requirements Specification Characteristics
* Complete
* Consistent
* Modifiable
* Traceable

#### Benefits from a High-Quality Requirements Process 

* Fewer requirements defects
* Reduced development rework
* Fewer unnecessary features
* Lower enhancement costs
* Faster development
* Fewer miscommunications
* Reduced scope creep
* Reduced project chaos
* More accurate system-testing estimates
* Higher customer and team member satisfaction
