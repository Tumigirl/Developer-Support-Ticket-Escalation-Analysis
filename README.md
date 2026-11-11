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
- Agent experience: agents with under 6 months’ experience escalate 36.61% of their tickets
- Issue category: Account Access (32.86%) and Billing (30.57%) have the highest rates, about 1.5 times the overall rate.
- Priority: P1 tickets escalate most often at 32.48%, followed by P2 at 25.06%. (P0 is the most urgent level.)
- Developer tier: Free-tier developers escalate 26.13% of their tickets

### Segments with no clear difference

- Channel: Email (23.05%), chat (22.92%) and phone (21.68%) are slightly higher
- Region: North America (22.71%) and EMEA (22.18%) are similar


## Why Does It Happen?
This are Inferences I have made on my own
- Reassignment: When tickets are reassigned and passed from agents to agents, information can tend to get lost and will need to be escalated for the senior agents to resolve.
- Agent with less than 6months of experience are likely to not have the skillset to resolve tickets compared to agents with more experience hence, escalation
- As for Account access and billing, one possible explanation is that these issues often need permissions or approvals that first-level agents don’t have. This was not tested in the data.
- Urgent tickets (P0 and P1) escalate more often than low-priority ones, with P1 highest at 32.48%
- Free-tier developers escalate more often (26.13%), which may reflect more reassignments among these tickets. Channel and region show no clear difference.

## Solution
These are suggestions based on patterns in the data. They haven’t been tested, and the dataset is synthetic practice data.

- Make handoffs smoother
Tickets that get passed from agent to agent are much more likely to escalate. A short handoff note (what the problem is and what has already been tried) would stop the next agent from starting from scratch. If a ticket has already been passed along twice, send it straight to a senior agent or specialist team instead of letting it keep moving.

- Support newer agents
Tickets handled by agents who are new to the job escalate far more often. Pair them with a mentor, give them simple guides for common problems, and make it easy to ask a senior colleague for help without handing the whole ticket over.

- Send Billing and Account Access tickets to the right people
These two issue types escalate most. They probably need permissions or approvals that first-level agents don’t have. Either route them straight to a specialist team, or give first-level agents clear authority to handle the common cases themselves.

- Give urgent tickets to experienced agents from the start
Urgent tickets escalate more often than low-priority ones. Sending them to experienced agents at the beginning avoids a second handoff later.

5. Help Free-tier developers get it right the first time
Free-tier developers escalate more often, possibly because their tickets get passed around more. Clearer help articles and a ticket form that collects the key details up front could mean fewer handoffs.

6. Leave channel and region alone
Neither made a clear difference, so there’s no need to change anything there. Time is better spent on the areas above.

### ![Dashboard](<img width="1366" height="768" alt="ticket dashboard pdf - Personal - Microsoft​ Edge 11_4_2026 4_46_41 PM" src="https://github.com/user-attachments/assets/ed2ae2eb-9cfe-433c-8167-7aa776b63f49" />)

### ![Dashboard](<img width="1366" height="768" alt="ticket dashboard pdf - Personal - Microsoft​ Edge 11_4_2026 4_46_53 PM" src="https://github.com/user-attachments/assets/73afee2d-ff64-431d-b5ff-f8271ad025e1" />)
