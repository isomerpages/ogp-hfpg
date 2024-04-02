---
title: Pair Search
permalink: /hack-for-public-good-2024/2024-projects/pairsearch/
variant: tiptap
description: ""
third_nav_title: 2024 Projects
---
<h4>Pair Search</h4>
<p></p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/HS_Today.jpg">
</div>
<p>Try it out the prototype <a href="https://search.pair.gov.sg" rel="noopener noreferrer nofollow" target="_blank">here</a> today!</p>
<h4>The bigger picture - Search for Humans and Machines alike</h4>
<p>A good decision is an informed one. Policy officers and a civic society
need information to make decisions and learn about areas of public interest,
improving search will help move us closer to this goal.</p>
<p>But good search isn’t limited to just human usage. Advances in Large Language
Models have led to a proliferation of data-augmented LLM generations, or
more commonly known as Retrieval Augmented Generation (RAG). The heart
of a good RAG system is a good search engine to retrieve the relevant data
chunks for ingestion. Figuring out the inside-outs of how to build a good
search engine is essential to not just our work on the Pair suite of products,
but potentially helpful to other LLM products in government as well.</p>
<h4>Hansard</h4>
<p>Every word that is said in Parliament is recorded and published as the
Official Report of Parliamentary debates or “Hansard”. These reports can
be found as far back as 1955, when Parliament was known as the Legislative
Assembly. This treasure trove of information is used by policy makers,
professionals and members of the public alike.</p>
<p>However searching for relevant Reports is currently difficult and unintuitive.
Results are poor due to being 100% keyword search based, meaning that the
documents that frequently mention a single word in a query are often ranked
more highly, when they should be taking the entire search phrase into account.&nbsp;</p>
<p></p>
<p>For instance, look at this search for “covid 19 rapid testing” in the
<a href="https://sprs.parl.gov.sg/search/#/home" rel="noopener noreferrer nofollow" target="_blank"><u>current Hansard search engine</u> 
</a>:</p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/covid_19_results_hansard.jpg">
</div>
<p></p>
<p>Due to how frequently Covid is mentioned in Parliamentary debates, the
actual results are flooded with reports that are only tangentially related
to the query, if at all. Additionally, only the titles are presented without
any smart text snippets to help a user confirm whether a link is likely
to be useful. Compare that to the results from <a href="https://search.pair.gov.sg/search?query=covid%2019%20rapid%20testing" rel="noopener noreferrer nofollow" target="_blank"><u>searching the same query in Pair Search</u></a>:</p>
<p></p>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/covid_19_results_pair_search.jpg">
</div>
<h4>Search smarter, not harder</h4>
<p>Current public and enterprise search experiences are generally low quality,
expensive and slow. We believe that this does not have to be the case.
Information should and can be readily accessible at everyone’s fingertips.</p>
<p>Pair Search was prototyped during OGP’s Hack for Public Good 2024 Hackathon,
under the guiding principles of proving search that should be:</p>
<ul data-tight="true" class="tight">
<li>
<p><strong>State of the Art (SOTA)</strong> - Search should leverage on all
the recent advances in search technology</p>
</li>
<li>
<p><strong>Fast</strong> - The complexity of the search algorithms should
no impact the latency of a search</p>
</li>
<li>
<p><strong>Simple, Intuitive and Effective</strong>
</p>
<ul data-tight="true" class="tight">
<li>
<p>Usage of the app should be intuitive</p>
</li>
<li>
<p>Information should be immediately presented in as useful a format as possible,
to aid users in deciding which results are worth further investigating</p>
</li>
</ul>
</li>
</ul>
<p>The site is <a href="https://search.pair.gov.sg/" rel="noopener noreferrer nofollow" target="_blank"><u>currently live</u></a>,
and indexed on the full Hansard Database from 1955 - January 2024, spanning
over 30,000 reports. Already we are seeing dramatic improvements in search
results using Pair Search.</p>
<h4>Search that actually works</h4>
<div class="iframe-wrapper">
<iframe height="315" width="100%" allowfullscreen="true" frameborder="0" src="https://www.youtube.com/embed/Eal6EvYeXUk?si=rMXQDT37wqVAtnOc"></iframe>
</div>
<p>Pair Search leverages <a href="http://Vespa.ai" rel="noopener noreferrer nofollow" target="_blank">Vespa.ai</a>, a highly versatile and scalable open-source
big data serving engine, to offer state-of-the-art search capabilities.
We leverage on their extensive text-search capabilities, as well as continuous
integration of state of the art techniques and models (e.g. the e5/m3 models
and ColbertV2 reranking)</p>
<p>*Note, the above video showcases a "Magic Summary" feature that automatically
generates a summary of the best results in a chronological timeline. However,
we are rolling Pair Search out without it first to focus on the core search
experience.</p>
<h4>The Data</h4>
<p>We undertook the challenging task of scraping and parsing the extensive
Hansard database. This site contains over 30,000 reports starting from
1955. Given the evolving data formats over the decades, standardizing this
diverse information for search purposes presented significant hurdles.
Nonetheless, these were successfully navigated to create a uniform format
conducive to efficient search operations.</p>
<h4>The Engine</h4>
<div class="isomer-image-wrapper">
<img style="width: 100%" height="auto" width="100%" alt="" src="/images/pair_search_tech.png">
</div>
<p>The search process in Pair Search is meticulously divided into <strong>three phases</strong>:&nbsp;</p>
<ol>
<li>
<p><strong>Document-Processing:</strong>&nbsp;</p>
</li>
</ol>
<p>This initial phase involved the challenging task of scraping and parsing
the extensive Hansard database, which contains records starting from 1955.
Given the evolving data formats over the decades, standardizing this diverse
information for search purposes presented significant hurdles. Nonetheless,
these were successfully navigated to create a uniform format conducive
to efficient search operations.</p>
<ol start="2">
<li>
<p><strong>Retrieval:&nbsp;</strong>
</p>
</li>
</ol>
<p>The retrieval mechanism combines keyword-based and semantic search strategies.
The keyword-based search utilizes Vespa's weakAnd operator alongside nativeRank
and BM25 text matching algorithms to efficiently sift through vast amounts
of data.&nbsp;</p>
<p>On the semantic front, Pair Search incorporates e5 embeddings, which offer
a balance of speed, cost-effectiveness, and enhanced performance compared
to alternatives like OpenAI's ada embeddings model.</p>
<p>This dual approach ensures a robust and nuanced search process that captures
both the intent behind user queries as well as the actual textual content.</p>
<ol start="3">
<li>
<p><strong>Re-ranking:&nbsp;</strong>
</p>
</li>
</ol>
<p>To keep results speedy despite our usage of complex re-ranking algorithms,
we utilize a three phase approach to iteratively refine the search results.</p>
<p><strong>Phase 1:</strong> each content node employs cost-effective algorithms
to narrow down the initial set of results.&nbsp;</p>
<p><strong>Phase 2: </strong>a more resource-intensive re-ranking is performed
using the ColbertV2 model, ensuring that the most relevant documents are
prioritized.&nbsp;</p>
<p><strong>Phase 3 (global phase): </strong>The final phase amalgamates the
top results from all content nodes, creating a hybrid score that integrates
semantic, keyword-based, and ColbertV2 scores. Utilizing a hybrid score
gives us significantly better performance than relying on just one metric,
which tend to be overly biased towards one dimension of result quality</p>
<h4>What's happening</h4>
<p>We have currently soft-launched the Pair Search (Hansard) prototype with
AGC, and a selection of users who frequently utilize Hansard Search, including
Ministry of Law legal policy officers, Comm Ops officers at MCI and PMO,
COS coordinators among others. We are averaging ~150 daily users and ~200
daily searches in the early days of our soft launch, and initial user feedback
has been positive:</p>
<p><strong><em>"This will improve productivity by a few folds. Hansard search was the most painful thing previously"</em></strong><em> - MCI Policy Officer</em>
</p>
<p><strong><em>"Wah useful. Returns results much faster than the current one"</em></strong><em> - MHA Policy Officer #1</em> 
<br>
<br><strong><em>"Wow this is really impressive!"</em></strong><em> - MHA Policer Officer #2</em>
</p>
<p>The product was also mentioned in <a href="https://sprs.parl.gov.sg/search/#/sprs3topic?reportid=motion-2318#" rel="noopener noreferrer nofollow" target="_blank">Parliament</a>:</p>
<p><strong><em>"The Hansard is an open book. We can all refer to it readily, and soon, we will be able to do a generative AI search on it."</em></strong><em> - Prime Minister Lee Hsien Loong</em>
</p>
<p>We have also seen interest from multiple agencies as well looking to leverage
our core Search Engine on their own data.</p>
<h4>What's next</h4>
<p><strong>Expanding our Data Sources</strong>
</p>
<p>Hansard is not the only useful public corpus of data with a less-than-ideal
search experience. For instance, even the search for a simple query such
as "Covid 19" on the <a href="https://www.sgpc.gov.sg/" rel="noopener noreferrer nofollow" target="_blank">SG Press Centre page</a> yields zero results
(you have to search for "covid-19" with a dash for it to return some documents.</p>
<div class="isomer-image-wrapper">
<img style="width: 75%;" height="auto" width="100%" alt="" src="/images/singapore_press_center_search_covid.jpg">
</div>
<p>One of our immediate goals is hence to expand the number of data corpuses
we make available for search. We are currently in the midst of working
with Judiciary to incorporate the case judgements from the High Court and
Court of Appeal (to go hand-in-hand with the current Hansard dataset for
any legal research use-cases).</p>
<p><strong>Going from Search to Recommendations</strong>
</p>
<p>The next goal for our search engine is to fully leverage the search index
we've built for not just direct queries, but also for enhancing discovery
and recommendations. By analyzing search patterns, user interactions, and
content relationships within our index, we can proactively surface relevant
content and personalized suggestions.</p>
<p>This approach will transform the search experience from being purely query-driven
to becoming a dynamic platform for content discovery, tailored to meet
individual user needs and preferences, thereby enriching user engagement
and satisfaction.</p>
<p><strong>Increasing the Search Performance</strong>
</p>
<p>We also constantly aim to better our search performance, which we chart
through metrics such as the average rank of results that are clicked, or
the number of pages a user has to go through before finding results they
want. These metrics can be used to tune our hybrid algorithm and/or weights
to improve both the accuracy and relevance of the results generated.</p>
<p>Another thing we are exploring now is the integration of LLMs to augment
the search performance via i) enriching the search index, via automated
tagging and potential-question generation and ii) enhancing the retrieval
/ ranking process through query expansion (appending additional related
terms and phrases to a query to increase the chance of retrieving a relevant
hit)</p>
<p><strong>Broadening the Applications of Our Search Engine</strong>
</p>
<p>As a search engine, we’ve designed it to work out of the box as the retrieval
stack for a Retrieval Augmented Generation system as well, such as the
one we have been trialing with the Assistants feature in Pair Chat. By
providing an API to both the base search functionality and the RAG retrieval
functionality, we hope to have our base engine serving multiple applications
and use-cases.</p>
<p>If you're currently using a search that doesn't quite work, or are interested
in collaborating, reach out to us <a href="https://go.gov.sg/pair-search-feedback" rel="noopener noreferrer nofollow" target="_blank">here</a>!</p>
<h4>Meet the team</h4>
<p>The prototype was developed by the following team.</p>
<div class="isomer-image-wrapper">
<img style="width: 50%;" height="auto" width="100%" alt="" src="/images/pairSearchTeamPhoto.jpg">
</div>
<p></p>
<p></p>
<p></p>