---
title: Roster Monster
permalink: /hack-for-public-good-2024/2024-projects/rostermonster/
variant: tiptap
description: ""
third_nav_title: 2024 Projects
---
<h3>Roster Monster</h3>
<h4>Problem</h4>
<p>Overworked healthcare professionals, including doctors, spend enormous
amounts of time monthly to plan complex rosters, taking precious time away
from their core duties. This one-month long process is tedious and time
consuming for three reasons:&nbsp;</p>
<ol data-tight="true" class="tight">
<li>
<p>Roster planning is mostly done manually using Excel, taking at least 5
hours monthly to finally generate the roster.</p>
</li>
</ol>
<p>In addition to creating the roster, roster planners gather leave and shift
requests from colleagues through various means such as emails, texts, or
verbal communication. These requests are manually compiled as constraints
in Excel during roster generation. Any last-minute amendments or requests
necessitate a manual regeneration of the roster, which can extend the time
required beyond the initial 5 hours.</p>
<ol start="2">
<li>
<p>Roster planners typically spend a minimum of 2 days adjusting system-generated
rosters due to existing system constraints, despite the availability of
automatic solutions.</p>
</li>
</ol>
<p>We interviewed users from public sector entities, as well as several public
health institutions, regarding rostering solutions. These interviews revealed
a desire for rostering solutions to have the abilities to be reconfigured
easily, change existing constraints and their weightage, and to accommodate
colleagues' requests. Some of the interviews also revealed pain points
with existing internal processes and the roster solutions users had previously
worked with.</p>
<ol start="3">
<li>
<p>Roster planning demands mental agility as planners balance numerous constraints
to ensure fair shift allocation.</p>
</li>
</ol>
<p>They must accommodate individual preferences while meeting mandatory shift
requirements, such as avoiding intense duties or weekend work. This entails
not only creating new rosters but also monitoring past shift allocations
to maintain fairness. Doing roster manually aggravates the complexity of
rostering in general.&nbsp;&nbsp;</p>
<h4>Opportunity</h4>
<p>Rostering is an essential task within the public sector.&nbsp;</p>
<p>Currently, we are starting off with the healthcare sector, targeting doctors
first. Doctors alone have wasted over 1,000* hours at least across all
public acute hospitals in Singapore. This excluded time spent by other
healthcare professionals such as nurses, medical social workers, pharmacists
and other allied healthcare partners. If we sum it all up, the healthcare
sector could have wasted over 4000 hours on manual rostering instead of
their core work – patient care.&nbsp;</p>
<p><em>* This calculation assumes an average of 53 departments based on <a href="https://www.moh.gov.sg/resources-statistics/singapore-health-facts/health-facilities" rel="noopener noreferrer nofollow" target="_blank"><u>10 public acute hospitals as of 2022</u></a> (excluding nursing and allied health services) and 2 doctor rosters per department because there is usually more than 1 type of roster to be planned monthly.&nbsp;</em>
</p>
<p>Apart from the healthcare sector, there is also possibility to explore
the extent of the rostering issue in the following sectors:</p>
<table>
<tbody>
<tr>
<td rowspan="1" colspan="1">
<p><strong>Sectors</strong>
</p>
</td>
<td rowspan="1" colspan="1">
<p><strong>Possibilities</strong>
</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Healthcare</p>
</td>
<td rowspan="1" colspan="1">
<p>Hospitals, clinics, and emergency medical services require rostering to
ensure round-the-clock coverage of medical staff.</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Emergency Services</p>
</td>
<td rowspan="1" colspan="1">
<p>Police, fire departments, and paramedics need rostering to maintain 24/7
emergency response capabilities.</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Transportation</p>
<p></p>
</td>
<td rowspan="1" colspan="1">
<p>Public transportation systems, including buses, trains, and subways, require
rostering to schedule drivers and operators for shifts.</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Education</p>
</td>
<td rowspan="1" colspan="1">
<p>Schools, colleges, and universities use rostering to schedule teachers,
professors, and other staff members.</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Military</p>
</td>
<td rowspan="1" colspan="1">
<p>Armed forces use rostering to schedule deployments, training exercises,
and operational duties.</p>
</td>
</tr>
<tr>
<td rowspan="1" colspan="1">
<p>Public Utilities</p>
</td>
<td rowspan="1" colspan="1">
<p>Essential services like water treatment plants, power stations, and waste
management facilities rely on rostering to ensure continuous operation.</p>
</td>
</tr>
</tbody>
</table>
<h4>Solution</h4>
<p>Roster Monster (RoMo) is a self-serve platform that allows roster planners
to generate their rosters automatically whenever needed, and set constraints
flexibly to meet their needs. We have validated the concept with users
through interviews with 10 doctors across 4 hospitals, and overall received
positive feedback.&nbsp;</p>
<p>In our very first release of the Minimum Viable Product (MVP), we want
to address the key pain points highlighted by public acute hospital doctors
on rostering. This includes having to:</p>
<ul>
<li>
<p>(For those using Excel) Manually re-generating rosters to accommodate
new requests or rules&nbsp;</p>
</li>
<li>
<p>(For those who are using commercial solutions apart from Excel) Inability
to change existing rules&nbsp;</p>
</li>
<li>
<p>Single view of all the blocked out dates and shift requests from all staff</p>
</li>
</ul>
<p><strong>Automatic roster generation</strong>
</p>
<ul>
<li>
<p>Re-generate the roster in seconds whenever there are changes to the original
rules</p>
</li>
<li>
<p>Powered by a constraint satisfaction problem (CSP) solver in the backend</p>
</li>
</ul>
<p><strong>Rule management</strong>
</p>
<ul>
<li>
<p>Bridge the gap between human-readable roster requirements and technical
CSP constraints by splitting rules into 4 categories</p>
<ul>
<li>
<p>Quota rules: Minimum/Maximum shifts staff must do</p>
</li>
<li>
<p>Pattern rules: Shifts that must be done in specific orders</p>
</li>
<li>
<p>Rolling window rules: Minimum/Maximum shifts over a fixed length of time</p>
</li>
<li>
<p>Soft rules: Whether to minimise/maximise number of shifts</p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/rule_selection.png">
</div>
</li>
</ul>
</li>
</ul>
<ul>
<li>
<p>Within each category, configuration is done by constructing a sentence
that describes what the rule is enforcing</p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/rule_ex.png">
</div>
</li>
</ul>
<p><strong>Staff management</strong>
</p>
<ul data-tight="true" class="tight">
<li>
<p>See all staff’s blocked out dates for scheduling and preferred shift slots
all in one view, during the entire roster period</p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/staff.png">
</div>
</li>
<li>
<p>Group staff members into any number of arbitrary groups that can then
be used during rule creation to make the rule target only specific staff
groups</p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/group_ex.png">
</div>
</li>
</ul>
<p>To access the prototype, click <a href="https://go.gov.sg/romo-trial-h4pg" rel="noopener noreferrer nofollow" target="_blank"><u>here.</u></a>
</p>
<h4>Traction</h4>
<p>As of 20 Feb 2024, we have received 70 sign-ups from interested partners
from H4PG and two email blasts.</p>
<p>81% of the sign-ups were in the healthcare sector from both public and
private acute hospitals e.g. Singapore General Hospital (SGH), Tan Tock
Seng Hospital (TTSH), and Nobel Medical Group while the remaining 19% were
from other sectors such as CPF Board, ICA Singapore and People Association
(PA) through organic sharing.</p>
<p>In particular, TTSH nursing and Sport Singapore have both reached out
to us beyond H4PG and expressed interest to discuss potential pilots within
their departments. An existing contact in the SGH Emergency Department
(ED) is also willing to run a pilot with us with minimal feature improvements.</p>
<p>The team has just sent out the MVP to all interested parties and is in
the process of scheduling user testing sessions with them.</p>
<h4>Team</h4>
<p>During H4PG, our team comprised of four members:</p>
<ul data-tight="true" class="tight">
<li>
<p><strong>[Sufyan] 1 Designer:</strong> Sufyan was the team’s anchor for
user research and design. The problems that Roster Monster are looking
to solve are deeply rooted in current work process and user behaviour.
Sufyan drove user interviews by diving deep and picking apart how rostering
works. He then translated that into an intuitive product for average roster
planners. Good design is particularly important in building an intuitive
rule-creation experience and bridging the gap between user and constraint
solver.</p>
</li>
<li>
<p><strong>[Latasha &amp; EnYi] 2 Engineers:</strong> Latasha was the engineer
in charge of the webapp. Her work included setting up the project infrastructure,
designing the database schema, as well as writing the core frontend components.
EnYi built out the constraint solver, translating commonly requested rules
into coded constraints. He designed the API contract between the webapp
and the solver by identifying opportunities to group constraints into categories.
Both engineers worked closely with Sufyan to design the rule-generation
user experience.</p>
</li>
<li>
<p><strong>[Limin - SNG] 1 ProdManagement/ProdOps:</strong> During H4PG, Limin
took on both product management and product operations roles. She was the
team’s main point of contact with external parties, and helped to secure
user interviews with doctors through her outreach efforts. She conducted
problem sizing exercises and identified opportunities for RoMo to tackle,
working closely with Sufyan to prioritise features for the prototype. She
also developed the main RoMo pitch for demo day, which the rest of the
team helped to execute.</p>
</li>
</ul>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/Roster_Monster_Poster1.jpg">
</div>
<p></p>