Data Dictionary

company_info

- `company_info`: an array with the following key and values
- `cik`: Central Index Key, a unique value used by the SEC to identify companies that have filed disclosures
- `ticker`: the ticker symbol used to identify a company on a stock exchange as of Oct. 7, 2026
- `company_name`: the name of the company
- `exchange`: the exchange that the company’s stock is traded on as of Oct. 7, 2026
- `sector`: the general industry the company operates under, made using a combination of designations from Morningstar

ieepa_info

- `ieepa_info`: an array with the following key and values
- `paid`: the amount a company said it paid in IEEPA tariffs
- `expected`: the amount the company said it expected to get back in tariff refunds or the amount it requested from U.S Customs and Border Protection
- `received_or_recognized`: the amount a company has said it received or put on its books so far

Each category (`paid`, `expected`, `received_or_recognized`) has these keys:

- `amount`: the amount for the array, in U.S. dollars
- `quotes`: an array that holds the quote displayed on the company page
- `notes`: one of the following values
- NET_AMOUNT: The amount was disclosed on a net basis, which could mean the total amount was higher
- MIN_RANGE: The minimum of a reported range was taken
- CURRENCY_CONVERTED: The amount was converted to U.S. dollars
- CALCULATION: We calculated this number using figures included in the company’s disclosure
- PART_NET_AMOUNT: The amount was disclosed at least in part on a net basis, meaning the total amount could be higher

Each quote has these keys:

- `full_sentence`: The quote taken from the source document
- `form`: Either an SEC disclosure, an earnings call or a company statement
- `filing_date`: The date the form/earnings call/company statement was filed or made
- `url`: the URL to the form
- `unit_scale`: the multiplier for the numbers in the quote when a filing reports its number in thousand or millions without saying so in the sentence we show
