# [Engineering Management - Estimation](https://confluence.softserveinc.com/display/AbilitonKnowledgeModel/Engineering+Management+-+Estimation)
### [Estimation](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2013/hh765979(v=vs.120))

Estimation is hard, one of the main reasons can be explained by Cone of Uncertainty.  
The beginning of any project is the time when we are the least certain about the project, yet it is also when we are asked to deliver estimates that are very precise.  

#### Estimation Techniques
All of these techniques require that we choose a unit of estimation—hours, days, weeks, months, ideal days, T-shirt sizing, points.  

* Counting 
* Expert judgment (individual and group)
* Decomposition
* Analogy
* Proxy estimation
* Planning poker
* Wall estimation. 

### [Scope Concept](https://en.wikipedia.org/wiki/Scope_(project_management))

In project management, the term scope has two distinct uses: Project Scope and Product Scope.  
* Project Scope: "The work that needs to be accomplished to deliver a product, service, or result with the specified features and functions."
* Product Scope: "The features and functions that characterize a product, service, or result."

Scope involves getting information required to start a project, and the features the product would have that would meet its stakeholders requirements.  Notice that Project Scope is more work-oriented (the hows), while Product Scope is more oriented toward functional requirements.  

Scope Management is the listing of the items to be produced or tasks to be done to the required quantity, quality and variety, in the time and with the resources available and agreed upon, and the modification of those variable constraints.

### [Scope creep](https://en.wikipedia.org/wiki/Scope_creep)
Refers to changes, continuous or uncontrolled growth in a project’s scope, at any point after the project begins.  
This can occur when the scope of a project is not properly defined, documented, or controlled.  
Scope creep is a risk in most projects.  
Scope creep can be a result of:
* poor change control
* lack of proper initial identification of what is required to bring about the project objectives
* weak project manager or executive sponsor
* poor communication between parties
* lack of initial product versatility

### Story based estimations 

Story points are relative values, not fixed. There is no direct correlation between hours and points.  

Mike Cohn summarizes story points: “Story points are a unit of measure for expressing the overall size of a user story, feature or other piece of work. ” Story points tell us how big a story is, relative to others, either in terms of size or complexity. Mike often refers to “dog points” when helping teams understand the concept of relative sizing. A 2-point (small) dog would be a Chihuahua. A 13-point (big) dog would be a Great Dane. With those two guides in mind, it’s fairly easy to size the other dog breeds relative to a Chihuahua or Great Dane. A Beagle, which is about twice as big as a Chihuahua, might be a 5. A Labrador, which is bigger than a Beagle but smaller than a Great Dane, might be an 8.

When you are first learning to use story points, your team will need to establish your own fixed comparison points. To do this, choose a story from your product backlog you can all agree is small (either in terms of size or complexity) and one you all agree is huge.  

Often Fibonacci prefer over, say, T-shirt sizing or growing exponentially (4/8/16/32/64/128/256, etc.) because we humans are good at base ten. When we get out of that range, even if we are in it with, say, xs, s, m, l, xl—it becomes confusing.  

### Estimates, Targets, and Commitments 
The most optimistic prediction that has a non-zero probability of coming true.  
An estimate is a prediction of how long a project will take or how much it will cost.  
An estimate is a rough measure of how long it will take to complete a task in the future. When you give estimates, you are predicting the future.

Target is a description of a desirable business objective.
A target is a goal. “We should have that finished by the end of the month,” is a target. It may not take the whole month, and in fact you may working on several other things in the month. But your goal is to have it done by then.  

Commitment is a promise to deliver defined functionality at a specific level of quality by a certain date.  
A commitment can be the same as the estimate, or it can be more aggressive or more conservative than the estimate.  
A commitment is more of a promise. “We will have that released by the end of the month.” Now you are committed.  

### Overestimate vs Underestimate 
The penalty for underestimation is more severe than the penalty for overestimation.  

Work will expand to fill available time.  
Desire to instill a sense of urgency in the development team.  
vs  
Reduced effectiveness of project plans.  
Statistically reduced chance of on-time completion.  
Poor technical foundation leads to worse-than-nominal results.  
Destructive late-project dynamics make the project worse than nominal.  

### Fundamental Estimation Techniques

#### Decomposition and Recomposition 
Decomposition by Feature or Task.  
Decomposition is the practice of separating an estimate into multiple pieces, estimating each piece individually, and then recombining the individual estimates into an aggregate estimate.  
Decomposition is a cornerstone estimation practice—as long as you watch out for a few pitfalls.  

__The Law of Large Numbers__  
If you create one big estimate, the estimate's error tendency will be completely on the high side or completely on the low side. But if you create several smaller estimates, some of the estimation errors will be on the high side, and some will be on the low side. The errors will tend to cancel each other out to some degree.

#### Analogy-based estimations 
Here is a basic estimation by analogy process that will produce better results:
1. Get detailed size, effort, and cost results for a similar previous project. If possible, get the information decomposed by feature area, by work breakdown structure (WBS) category, or by some other decomposition scheme.
2. Compare the size of the new project piece-by-piece to the old project.
3. Build up the estimate for the new project's size as a percentage of the old project's size.
4. Create an effort estimate based on the size of the new project compared to the size of the previous project.
5. Check for consistent assumptions across the old and new projects.  

Tip: Estimate new projects by comparing them to similar past projects, preferably decomposing the estimate into at least five pieces. 
 
#### Estimation by Analogy 
In proxy-based estimation, you first identify a proxy that is correlated with what you really want to estimate and that is easier to estimate or count (or available earlier in the project) than the quantity you're ultimately interested in.   
If you want to estimate a number of test cases, you might find that the count of the number of requirements is correlated with the number of test cases.  

#### Individual Expert Judgment
To create the task-level estimates, have the people who will actually do the work create the estimates.  
If your project is still in the wide part of the Cone of Uncertainty (that is, specific tasks haven't yet been identified or assigned to individuals), the estimate should be created by an expert estimator or by the most expert development, quality assurance, and documentation staff available.  

#### Expert Judgment in Groups 
* Have each team member estimate pieces of the project individually, and then meet to compare your estimates
* Don't just average your estimates and accept that 
* Arrive at a consensus estimate that the whole group accepts 

### [Wall estimation](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2013/hh765979(v=vs.120)#wall-estimation)
![wass](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2013/images/hh765979.wall2%28vs.120%29.png)
To do Wall Estimation, you must first print your user stories on cards. Then gather your team and stakeholders in a room with a big empty wall (about 14 feet long by 8-10 feet high); Understand two things about the wall:  
* Height determines priority. Stories at the top are higher; stories at the bottom are lower. A story’s priority can be based on ROI, business value, or something as simple as “it’s just important, and I don’t know why.”  
* Width is reserved for size. Stories on the left are smaller; stories on the right are bigger. (You can reverse this and move from right to left if you’re in, say, Japan and it’s more logical.) The important thing is to envision a line going horizontally and one going vertically. Team members and stakeholders should ask themselves, where, relative to the other stories, does this one fit?  

The team will use the wall to size all of the stories. The stakeholders will use the wall to prioritize stories. As with planning poker, we’re using relative sizing, but instead of using two reference stories for comparison, the wall becomes the constant. Small story? Move to the left. Big story? Move to the right. Important story? Place it high. A story that we can live without for now? Place it low.  


## Competent

### Cone of Uncertainty 

The cone demonstrates that we have the most uncertainty at the beginning of any project (a variance of 4x to 0.25x in range).

![Cone](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2013/images/hh765979.coneofuncertainty%28vs.120%29.png)

### Source of Estimation Errors 

