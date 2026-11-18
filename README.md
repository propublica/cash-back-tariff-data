# Download the Data Behind ProPublica’s “Cash Back” Tool 

After President Donald Trump’s “emergency” tariffs were overturned by the Supreme Court in February 2026, the government began processing billions in refunds to importers, including many recognizable public companies.

The Trump administration has not publicly detailed which companies are getting roughly \$170 billion in refunds or how much they’ve asked for. So our reporters found another way: analyzing the financial disclosures of thousands of publicly traded companies.

ProPublica published [“Cash Back,” a database of figures on refunds for tariffs](https://projects.propublica.org/trump-tariff-refund-ieepa/) paid under the International Emergency Economic Powers Act. 

We are also making the information in the Cash Back database available for download [here](https://github.com/propublica/cash-back-tariff-data/blob/main/data.jsonl).

## How should I credit this information?

We ask that you credit “ProPublica analysis of financial disclosures” and link to [this tracker](https://projects.propublica.org/trump-tariff-refund-ieepa/).

If you make something with the data, we’d like to hear about it! Reach us at [tariffs@propublica.org](mailto:tariffs@propublica.org).

## What’s included in the database?

The [Supreme Court ruled](https://www.supremecourt.gov/opinions/25pdf/24-1287_4gcj.pdf) on Feb. 20, 2026, that the International Emergency Economic Powers Act doesn’t authorize the president to impose tariffs. The U.S. Court of International Trade ordered U.S. Customs and Border Protection to refund the duties it had collected. 

This tracker covers refunds on those tariffs disclosed by publicly traded companies. Public companies must disclose events that affect their finances, such as tariff payments and refunds, on earnings calls and in regular reports filed with the Securities and Exchange Commission. We collected information from these public sources through Oct. 7, 2026\. 

Before publishing, we contacted all companies shown here to check the accuracy of the numbers we had found.

We grouped companies by industry using a combination of [designations from Morningstar](https://www.morningstar.com/sectors).

We are publishing data for companies if we know how much they paid in tariffs, expect to get back or how much they have already received or recognized. The downloadable JSON data includes one row for each company. It includes company IDs (CIK numbers and stock tickers), as well as the amounts ProPublica was able to determine. The data also includes source information for each data point. 

## How did we determine refund amounts? 

ProPublica searched through securities filings and earnings calls using key phrases to isolate companies that mentioned tariff refunds. For each company, we created a document that included the extracted text around each phrase. For SEC filings, that included parsed Extensible Business Reporting Language when available.

We then used an open-weight artificial intelligence model for a first pass at identifying refund amounts. ProPublica reporters reviewed each company by hand to make sure our database is accurate and contacted all companies to confirm the amounts.

Companies normally record tariff refunds in their financial statements under two accounting models:

* Gain contingency: when the refund has been received or recovery is essentially certain.  
* Loss recovery: when the refund is probable and can be reasonably estimated.

To determine a company’s recovered refund, we added up the amounts it recorded that were essentially certain or probable (sometimes known as “receivable”), plus the amounts it disclosed as having been received. 

The government is required to pay interest on tariff amounts it is returning, at rates [determined by the IRS](https://www.federalregister.gov/documents/2026/01/22/2026-01175/quarterly-irs-interest-rates-used-in-calculating-interest-on-overdue-accounts-and-refunds-of-customs) on a quarterly basis. Companies disclosed that interest in different ways. Some reported the refund and the interest separately, while others reported a single amount that included both. When a company reported them separately, we added the interest to the refund to capture the full amount of money that a company was receiving from the government. 

Some companies reported only their net refund instead of the full amount received. For example, a company might report only what was left of the tariff refund after reinvesting into its business or after passing part of the refund onto customers. In these cases, we reported the net amount. When companies reported a range, we used the lower end. In both cases, we noted that information on the company page. 

The specific security filings reviewed were: 8-K, 10-Q, 10-K, 8-K/A, 10-Q/A, 10-K/A, 6-K, 6-K/A, 20-F, 20-F/A, 40-F, 40-F/A and any associated exhibits. 

## How do I report incorrect information? 

If you see information that may be incorrect, please email [tariffs@propublica.org](mailto:tariffs@propublica.org). 

We will periodically update our database by pulling information from newer filings, as well as correcting or adding new information when companies reach out to us.

## Do you have information you can share about how a company is using tariff refunds?

ProPublica’s investigative journalists are reporting on tariff refunds and how, or if, companies are giving money back to consumers. You can reach [our tip line](https://www.propublica.org/tips/) or contact us on Signal at 917-512-0201. Please be as specific, detailed and clear as you can.

## Licensing

We are releasing this data under a [Creative Commons BY-NC 4.0 license](https://creativecommons.org/licenses/by-nc/4.0/), meaning you may use it for noncommercial purposes as long as you attribute ProPublica and link back to [this tracker](https://projects.propublica.org/trump-tariff-refund-ieepa/)