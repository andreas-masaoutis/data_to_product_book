
**********************
A concrete example
**********************

============================
The project's Vision 
============================

Every project starts with an idea and some background. Let's take a look.

-----------------------------
The three R's of good science
-----------------------------

Good science should be, at least, repeatable, replicable, and reproducible. The `Association for Computing Machinery`_ has adopted the following definitions (August 2020).

.. _Association for Computing Machinery: https://www.acm.org/publications/policies/artifact-review-and-badging-current


Repeatability (Same team, same experimental setup):

    The measurement can be obtained with stated precision by the same team using the same measurement procedure, the same measuring system, under the same operating conditions, in the same location on multiple trials. For computational experiments, this means that a researcher can reliably repeat her own computation.

Reproducibility (Different team, same experimental setup):

    The measurement can be obtained with stated precision by a different team using the same measurement procedure, the same measuring system, under the same operating conditions, in the same or a different location on multiple trials. For computational experiments, this means that an independent group can obtain the same result using the author’s own artifacts.

Replicability (Different team, different experimental setup):

    The measurement can be obtained with stated precision by a different team, a different measuring system, in a different location on multiple trials. For computational experiments, this means that an independent group can obtain the same result using artifacts which they develop completely independently.


Since since a significant part of scientific work revolves around data and computations, the way we treat the data sources becomes important.

----------------------------------------------------------
The case of football betting data and academic research
----------------------------------------------------------

In financial economics, economists assume a reverse relation between the expected return of an asset and its associated risk, measured by the variance of the expected return. A risky asset is expected to have a higher expected return but also more variability, compared to a less risky one.  




^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Using betting data for hypothesis testing
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The site `Football-Data`_ has a large collection of data on football matches from more than 30 leagues, spanning more than 20 years, along with the corresponding data from bookmakers on bets for the HomeWin, Draw, and AwayWin. This collection of data is used extensively [#footnote_google_scholar]_ in academic research that aims at analysing market outcomes, including the validity of the efficient-market hypothesis [#footnote_emh]_.

.. _Football-Data: https://www.football-data.co.uk/


The data found on Football-Data is in spreadsheet or csv format, divided across leagues and seasons. That means that every researcher that wants to use this dataset has to get through the whole process of collecting the data, bringing it together, cleaning it, creating the desired 'features' for the analysis, etc. This data preparation process is first of all time consuming, but can also be error-prone.


----------------------------------------------------------
Our Vision
----------------------------------------------------------

For the academic researchers

Who use the Football-Data collection  

The (the name of the site) provides a service

That will save time on data preparation and reduce errors

Unlike manual process of doing this over and over again

By providing a standard API for downloading relevant data, and an interface for pre-prepared visualisations of it.



.. rubric:: Footnotes

.. [#footnote_google_scholar] As of March 2022 a Google Scholar search with the Football-Data link returned more than 500 results

.. [#footnote_emh] The efficient-market hypothesis (EMH) assumes that asset prices reflect all available information. If they didn't it would be possible for an investor to apply a trading strategy, that would accrue profits above the market rate, for a given level of risk. What this means is that it is impossible to "beat the market" on the long-run, if all market participants have the same level of information. For example, suppose that the piece of information in question says that a financial crisis is likely to come soon. Investors typically do not like to hold stocks during a financial crisis, and thus investors may sell stocks until the price drops enough so that the expected return compensates for this risk.


