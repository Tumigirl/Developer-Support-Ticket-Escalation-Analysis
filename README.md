# Developer-Support-Ticket-Escalation-Analysis
This is a project that highlights the factors that increases the rate of escalation of developers tickets at Google

## Background/Inspiration
I wanted to practice the skills in a Business Data Scientist job posting at Google, so I reverse-engineered the role and had Claude generate a synthetic dataset of support tickets. The task was to find out why tickets escalate and recommend fixes. I cleaned the data and analyzed it in Python, built a Power BI dashboard, and wrote recommendations. The dataset is AI-generated; the analysis and conclusions are my own

## What is the problem?
In this practice scenario, Google’s developer support leadership noticed that too many support tickets were being escalated. About 1 in 5 tickets (21.25%) escalated.

Escalation is when a developer(client) submits a support ticket for a support agent to work on it but sometimes the agent can’t solve it, for example because they lack the experience or aren’t available, so the ticket is passed up to a more senior agent or a specialist team. A ticket can also be reassigned, meaning passed to another agent, without being escalated.

Leadership wanted to know three things:
- How often tickets escalate
- Which factors are linked to escalation
- What could be done to reduce it
- 
## Who is affected?
Developers (the clients) are the most affected. Escalated tickets aren’t noticeably slower, so the frustration likely comes from being passed around and having to explain the problem again. Senior agents are affected because escalations add to their workload, including work that may have been resolved at the first level. Newer agents are involved too i.e those with under 6 months of experience escalate about twice as often as the rest. Developers on the Free and Startup tiers also escalate more than those on Growth or Enterprise. Finally, the business is affected through unhappy customers and the cost of extra senior time.

## Where does it happen?

Overall, 21.25% of tickets escalated. Escalation is not spread evenly: it concentrates in a few segments, and for others it makes little difference.

### Segments with a clear difference

- Reassignments: escalation rises sharply with each handoff: 4.14% with 0 reassignments, 18.85% with 1, 54.81% with 2, and 85.85% with 3. Tickets reassigned more than 3 times are too few to analyse reliably, so they are left out. 
- Agent experience: agents with under 6 months’ experience escalate 36.61% of their tickets, compared with [X%] for more experienced agents.
- Issue category: Account Access (32.86%) and Billing (30.57%) have the highest rates, about 1.5 times the overall rate.
- Priority: P1 tickets escalate most often at 32.48%, followed by P2 at 25.06%. (P0 is the most urgent level.)
- Developer tier: Free-tier developers escalate 26.13% of their tickets, against [X%] for Growth and Enterprise.

### Segments with no clear difference

- Channel: Email (23.05%), chat (22.92%) and phone (21.68%) are slightly higher, but all channels fall within [X] percentage points of each other.
- Region: North America (22.71%) and EMEA (22.18%) are similar, and all regions fall within [X] points of each other, so region does not appear to matter.

