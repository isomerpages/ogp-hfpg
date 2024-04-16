---
title: People Association CRM
permalink: /hack-for-public-good-2024/2024-projects/peopleassociationcrm/
variant: tiptap
description: ""
third_nav_title: 2024 Projects
---
<h3>People Association CRM</h3>
<h4>Problem</h4>
<p>The People's Association (PA) is assisting a lot of residents with their
financial difficulties through the use of multiple funds. Currently, the
routing and approval seeking are manually done by the community officer
(CO) at different community centers. The problems with the current approach
are:</p>
<ul>
<li>
<p>An arduous administrative process carried out by our COs using physical
forms and manually carrying forms around for signatures. Right now it usually
takes <strong>3 weeks</strong> for each approval, which induces a lot of
unnecessary stress and anxiety for the family who might be living paycheck
to paycheck</p>
</li>
<li>
<p>Lack of consistency between different community centers about this process</p>
</li>
<li>
<p>Data are not being digitally collected for better policy-making</p>
</li>
</ul>
<h4>Solution</h4>
<p>We use our <a href="https://plumber.gov.sg" rel="noopener noreferrer nofollow" target="_blank">Plumber</a> product
(for workflow automation) in combination with Zendesk (for remote communication
and approval seeking) and M365 (for data storage and possible analysis)</p>
<p>In our design, we have 2 Plumber workflows:</p>
<ul>
<li>
<p>Application creation workflow:</p>
<ul>
<li>
<p>Starts with a FormSG that residents and COs and raise a case</p>
</li>
<li>
<p>The workflow, upon receiving the submission, will create a Zendesk ticket
and assign it to the CO</p>
</li>
<li>
<p>The workflow will also persist the case inside a shared M365 excel sheet
for tracking</p>
</li>
</ul>
</li>
<li>
<p>Approval workflow:</p>
<ul>
<li>
<p>CO will gather any extra information from resident (if needed) to add
to the case before forwarding to the relevant parties (also on Zendesk)
for explicit approval</p>
</li>
<li>
<p>Upon approval / rejection on Zendesk, the Plumber workflow will update
the case status to the tracking M365 sheet</p>
</li>
<li>
<p>The M365 sheet can be used to chart data and draw insights to make better
policies</p>
</li>
</ul>
</li>
</ul>
<p>Read more <a href="https://docs.google.com/presentation/d/1T5Crw7liZkdnR6Oa7U9365BV-I-66pstFv9g5xQz-zc/edit#slide=id.p" rel="noopener noreferrer nofollow" target="_blank">here</a>.</p>
<h4>Impact and Potential Growth</h4>
<p>With our automation, approval time can be cut down to within the one day.</p>
<h4>Team Members</h4>
<ul data-tight="true" class="tight">
<li>
<p>Yuanruo</p>
</li>
<li>
<p>Malcolm</p>
</li>
<li>
<p>Stanley</p>
</li>
</ul>
<p></p>