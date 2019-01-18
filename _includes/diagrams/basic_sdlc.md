````mermaid

graph TB
Pre["<b>Pre-project stage</b><br/><small><b>Products: </b> Terms of reference (Internal record document)<br/><b>Goals: </b>Understand business case, high-level requirements,<br/>funding landscape etc.<br/><!--<b>Roles: </b>Analyst, Project Manager, Director''></small>"] --Go?--> 

Feas("<b>Feasibility</b><br/><small><b>Products: </b>Feasibility (Internal record for peer review),<br/>High Level Costings --> Product Quote (<i>if</i> feasible)<br/><b>Goals: </b> Assess technical feasibility, clarify roles and responsibilities<br/> and make final GO/NO GO assessment.<br/><!--<b>Roles: </b>Analyst, Project Manager, Developer, UI/UX, Systems Manager--></small>")
Pre--No go?-->endPre[Do not proceed]

Feas--Feasible?-->Kick("<b>Kick-off</b>")
Feas--Not feasible?-->endPre
Feas-->Kick
Kick-->Evo("<b>Evolutionary development</b><br/><small><b>Products: </b>Timebox plans, Timebox reviews<br/>
<b>Goals: </b>Define goals for each development timebox and work toward an<br/>iteration for eventual deployment. Review progress from previous</br>timebox and review prioritised requirements.</small>")
Evo--"Timebox review(s)"-->Dep("<b>Deployment</b><br/><small><b>Goals: </b>Bring baseline of Evolving solution into operational use.<br/>Ensure comprehensive testing by all parties.</small>")
Dep--Increment review-->Evo

Dep-->cF("<b>Change freeze</b><br/><small><b>Goals: </b>Ensure that Minimum Viable Product is not compromised by late<br/>changes in scope, design or functionality, by directing remaining<br/>resources effectively</small>")

cF-->Post["<b>Post project</b><br/><small>
<b>Goals: </b>Assess project outcomes.<br/>Ensure appropriate lifespan for project (as agreed during Feasibility.<br/>Define <b>Service Level Agreement </b> with project stakeholders.<br/>
Follow robust archiving procedures.<br/>
<b>Products: </b>Project Review Report, Service Level Agreement</small>"]

Post-->decom["<b>Decommissioning</b><br/><small>
</small>"]

Post-->Maint["<b>Maintenance</b>"]

Maint-->Evo


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5Njg0MzM4NiwtMTY5MTQ1MDU2OF19
-->