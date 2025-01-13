---
title: Scribe
permalink: /hack-for-public-good-2024/2024-projects/scribe/
variant: tiptap
description: ""
third_nav_title: 2024 Projects
---
<h3>Scribe</h3>
<h4>Problem</h4>
<p>Medical Social Workers (MSWs) meet needy patients daily to understand
their personal backgrounds, financial circumstances, and social / medical
issues, so as to provide an overall psycho-social assessment of the patient
and to apply for financial assistance on their behalf.</p>
<p>These meetings are typically 1 hour long, after which MSWs must spend
time documenting and consolidating their notes on the patient. Writing
these case notes can take between 30 mins to 2 hours, depending on the
case complexity and the experience of the MSW. The average MSW may see
between 3 to 8 patients in a day, depending on seniority and specialty.
There were about <a href="https://www.moh.gov.sg/news-highlights/details/number-and-ratio-of-medical-social-workers-and-aic-care-co-ordinators-to-population-of-care-recipients-over-age-65" rel="noopener noreferrer nofollow" target="_blank"><u>600 Medical Social Workers in Singapore in 2019</u></a> and
their numbers have only increased since then.</p>
<h4>Solution</h4>
<p>We built <strong>Scribe </strong>to help Medical Social Workers (MSWs)
synthesise MSW-Patient conversations into structured progress notes.&nbsp;</p>
<p>Scribe allows MSWs to record their conversations with patients, after
which a multi-lingual transcript (with support for English, Malay, Chinese,
and Singlish) is generated using state-of-the-art speech recognition models.&nbsp;</p>
<p>Using this transcript, MSWs can then generate a summary of the transcript
with a chosen output type, such as actionables in bullet points or a summary
with section headings. A large language model (LLM) processes and summarises
this transcript with the desired output type.</p>
<p>Both the speech recognition model and LLM are open-source models running
on our infrastructure and we rely on no external APIs for Scribe, so sensitive
patient data and conversations never leave our system.</p>
<p>The generated summary can then be exported directly to Care360 as a draft
case note. (Care360 is a patient management system used by MSWs and is
the key driver for their daily workflows.) On Care360, MSWs can further
edit the case note to their satisfaction. By transcribing and summarising
MSW-patient conversations and providing MSWs with a solid foundation to
swiftly compose their notes, Scribe speeds up the note-writing process
and enables MSWs to prioritise what truly matters—fostering meaningful
connections and enhancing patient care.</p>
<h4>User Testing and Feedback</h4>
<p>We tested Scribe in a mock setting (i.e. simulated patient-MSW conversations)
with MSWs from CGH, SGH, and SACH, as well as with Social Work students
from NUS.&nbsp;</p>
<div class="isomer-image-wrapper">
<img style="margin-left:0px;margin-top:0px;" height="231" width="308" src="https://lh7-us.googleusercontent.com/nAeX2utYsRH8V__blPPK2XvztNADm0HMCR2hgU9akHE7w3Nc1DjrkX3su2tfegvhI9qcyHmgwlLUii--1Oa_89-iMomTIvqs2LIC0LtJPDUFQqoqAbng5INgiQtVtI03HhZJZWqqj02BeolzfQYjPUI">
</div>
<p>For the transcription, it was suggested dialect support be added given
that many needy patients are elderly. The transcription also did not always
indicate which speaker made which utterance, which made it less readable.
However, all participants agreed the lack of readability of the transcription
was not a concern as long as the quality of the generated summary was high.
As one remarked, “If summarised well, I won’t even refer to the transcript”.</p>
<p>Most MSWs were impressed by the quality of the summaries. One MSW remarked
that they were “quite close to what we would write”, and another wondered
if automatically generated summaries might result in MSWs not thinking
for themselves. There was some surprise about the variable nature of summary
generation, i.e. that the output generated would be slightly different
every time. The summary was occasionally too verbose at times or had minor
errors. Overall, they were quite forgiving of errors and pleased that Scribe
provided a comprehensive summary that they could quickly refine / shorten
to their needs.</p>
<p>The main concern with Scribe is whether patients would be less forthcoming
in their conversations when recorded. It may not be appropriate to use
Scribe when interacting with patients with more sensitive personal situations.
Most participants agreed that they would only use the tool for patients
they had more rapport with or if its usage was more normalised in their
institution / cluster.</p>
<div class="isomer-image-wrapper">
<img style="margin-left:0px;margin-top:0px;" height="405" width="540" src="https://lh7-us.googleusercontent.com/7ftGVa0DVZoumOUX7ct99TJETlYbbd384udht0vjbT_4PY01uIaXLHzM40aVcK9uHJx5Wmww1r2b1xxaDD2b5VvioB-59JEQDIA4mvIQZhE0j61Ya0SlYTNUWc7PJNB1ne_-MHRh0aRhVWnyF15lJfo">
</div>
<p>Starting from Mar 2024, we will be working with the healthcare clusters
to pilot test Scribe with actual patients.</p>
<h4>Team</h4>
<p>Scribe was built by a multidisciplinary team of engineers, designers,
and product managers.</p>
<div class="isomer-image-wrapper">
<img style="margin-left:0px;margin-top:0px;" height="183" width="624" src="https://lh7-us.googleusercontent.com/Vs-tRj595CbBe3yo4l9MEHhIRS1qLj_Aq8hCw-PyL4CexuyHo6ESEV3jiX3o8hLQGBjRfs16Lvzg8uHwhO-CqgDMASsHUk7Dpm3rx1_Ok3hRcMRRTt_pmHKYVHxk6nKI2JSOt0OJaQ4C0OATkpkjFhE">
</div>
<hr>
<p>If you would like to use Scribe in your organisation, please email <strong>team@scribe.gov.sg</strong>.</p>
<p>For more details on the Scribe prototype, please refer to our deck below.</p>
<div class="iframe-wrapper">
<iframe height="569" width="960" allowfullscreen="true" frameborder="0" src="https://docs.google.com/presentation/d/e/2PACX-1vT-TrTHwUCHwbeBttNu-UOthOhYMDbmINuHIKV7DL8sTvPW3LeU8M7neSBv7HCMn9_cWSEc6YyFf3S1/embed?start=false&amp;loop=false&amp;delayms=3000"></iframe>
</div>
<p></p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/A2_Poster_page_0001.jpeg">
</div>
<p></p>
<p></p>