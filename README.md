# Findings

Three rounds of searches were conducted (2023-10-12).

1. GitHub Search 1 - Repositories General
   * Folder: `search_1_repository_general`
2. GitHub Search 2
   * Folder: `search_2_repository_ema_mhealth_app`
3. GitHub Search 3
   * Folder: `search_3_readme`

## GitHub Search 1 - Repositories General

Folder: `search_1_repository_general`

Search Term:

* `2021-01-01`: last push after 2021.01.01
* `followers:>=1`: at least one follower

```bash
https://api.github.com/search/repositories?per_page=100&q=$$SEARCH_TERM_URI_ENCODED_STRING+pushed:>2021-01-01+followers:>=1
```

* [Search Terms](./searchterms@search_1_repository_general.txt)
  * `data warehouse analysis language:python`
  * `modular automated data transformation pipeline`
  * `modular automated data transformation pipeline language:python`
  * `modular data pipeline`
  * `modular data pipeline language:python`
  * `modular data pipeline transformation`
  * `pipeline data science language:python`
  * `pipeline data dashboard language:python`
  * `pipeline data dashboard visualization`
  * `pipeline dashboard framework`
  * `pipeline framework language:python`

Evaluation

* *Step_0*: total matches
  * `341` with duplicates
  * `313` without duplicates
* *Step_1*: title & description screening
  * `88` with duplicates
  * `79` without duplicates
* *Step_2*: repo screening
  * `28` with duplicates

Results (no duplicates)

=> `28` final matches

## GitHub Search 2 - Repositories EMA / mhealth / App

Folder `search_2_repository_ema_mhealth_app`.

Search Term:

* `2021-01-01`: last push after 2021.01.01
* `followers:>=1`: at least one follower

```bash
https://api.github.com/search/repositories?per_page=100&q={{SEARCH_TERM_URI_ENCODED_STRING}}+pushed:>2021-01-01+followers:>=1
```

* [Search Terms](./searchterms@search_2_repository_ema_mhealth_app.txt)

Results:

No matching `repositories` were found for the following search terms.
The initial search resulted in just a few hits, which then got filtered out for the reasons: `duplicate`, `only readme`, `unrelated`, `empty repository` and in one case `not a framework`.
Result:
`0` hits for the given queries.

### Search Terms - Ecological Momentary Assessment (EMA)

* `data transformation ecological momentary assessment`
* `data transformation ema`
* `pipeline data ecological momentary assessment`
* `pipeline data ema`
  * [-9-Email-Marketing-Tips-For-Content-Marketers](https://github.com/ZulqarnainZilli/-9-Email-Marketing-Tips-For-Content-Marketers)
    * empty repository
* `pipeline transformation ecological momentary assessment`
* `pipeline transformation ema`
  * [alizaman855/Email-Spam](https://github.com/alizaman855/Email-Spam)
    * unrelated

### Search Terms - Mobile Health (mHealth)

* `data transformation mhealth`
* `data transformation mobile health`
  * [Aryia-Behroziuan/neurons](https://github.com/Aryia-Behroziuan/neurons)
    * just a README
* `pipeline data mhealth`
* `pipeline data mobile health`
* `pipeline transformation mhealth`
* `pipeline transformation mobile health`

### Search Terms - Mobile Application (Mobile App)

* `data transformation mobile app`
* `data transformation mobile application`
  * [Aryia-Behroziuan/neurons](https://github.com/Aryia-Behroziuan/neurons)
  * [jettbrains/-L-](https://github.com/jettbrains/-L-)
* `pipeline data mobile app`
  * [MariamGado0/Starbucks-Capstone-Project-ML-Udacity-aws](https://github.com/MariamGado0/Starbucks-Capstone-Project-ML-Udacity-aws)
    * unrelated
  * [Phamdung2009/xxx](https://github.com/Phamdung2009/xxx)
    * just a README
  * [ZulqarnainZilli/-9-Email-Marketing-Tips-For-Content-Marketers](https://github.com/ZulqarnainZilli/-9-Email-Marketing-Tips-For-Content-Marketers)
    * empty repository
* `pipeline data mobile application`
  * [Aastha2104/Parkinson-Disease-Prediction](https://github.com/Aastha2104/Parkinson-Disease-Prediction)
    * not a framework
    * but ML on mHealth data
  * [AUTOMATE-STATIC-WEBSITE-DEPLOYMENT-FROM-GITHUB-TO-S3-USING-AWS-CODEPIPELINE](https://github.com/shankarsurya035/AUTOMATE-STATIC-WEBSITE-DEPLOYMENT-FROM-GITHUB-TO-S3-USING-AWS-CODEPIPELINE)
    * just a README
  * [Phamdung2009/xxx](https://github.com/Phamdung2009/xxx)
    * duplicate
    * just a README
* `pipeline transformation mobile app`
* `pipeline transformation mobile application`

## GitHub Search 3 - README

The goal here was to find repositories on GitHub that provide *pipeline* (frameworks) for *data* *transformation*/*visualization* in the context of mobile health (mHealth).

Folder: `search_3_readme`

Search Term:

```bash
https://api.github.com/search/repositories?q={{SEARCH_TERM_URI_ENCODED_STRING}}+in:readme+language:python+pushed:>2021-01-01+{{ADDITIONAL_CONDITION}}&type=repository&per_page=100&s
```

* Base URL: `https://api.github.com/search/repositories`
* Query: `q=$$SEARCH_TERM_URI_ENCODED_STRING+in:readme+language:python+pushed:>2021-01-01+{{ADDITIONAL_CONDITION}}&type=repository&per_page=100&s`
  * `{{SEARCH_TERM_URI_ENCODED_STRING}}`: Search terms that have to be found somewhere in the README file (multiple words, all required).
  * `in:readme`: Search in the README file.
  * `language:python`: Programming language is python.
  * `pushed:>2021-01-01`: Repository was pushed after 01.01.2021.
  * `{{ADDITIONAL_CONDITION}}`
    * `stars:>={{MIN_STARS}}`: At least `1`/`10`/`100` stars.
    * `followers:>={{MIN_FOLLOWERS}}`: At least `1`/`10`/`100` followers.

* [searchterms@search_3_readme.txt](./searchterms@search_3_readme.txt)
  * `pipeline data transformation mhealth`
  * `pipeline data transformation mobile health`
  * `pipeline data visualization mhealth`
  * `pipeline data visualization mobile health`

Evaluation

For `stars` and `followers` the same results where found.
Therefore only `stars` will be shown in the following.
Stars indicate the popularity of the repository.

* `{{SEARCH_TERM_URI_ENCODED_STRING}}`
  * *pipeline data transformation mhealth*
    * `>=1`: **`0`**
    * `>=10`: **`0`**
    * `>=100`: **`0`**
  * *pipeline data transformation mobile health*
    * `>=1`: **`34`**
    * `>=10`: **`15`**
    * `>=100`: **`7`**
  * *pipeline data visualization mhealth*
    * `>=1`: **`1`**
    * `>=10`: **`0`**
    * `>=100`: **`0`**
  * *pipeline data visualization mobile health*
    * `>=1`: **`60`**
    * `>=10`: **`26`**
    * `>=100`: **`14`**
* in total (including duplicates)
  * `>=1`: **`95`**
  * `>=10`: **`41`**
  * `>=100`: **`21`**
* in total (no duplicates)
  * `>=1`: **`65`**
  * `>=10`: **`28`**
  * `>=100`: **`15`**

For the above search terms there were in total **`95`**/**`41`**/**`21`** (depending on the `stars` condition) found, including duplicates and **`65`**/**`28`**/**`15`** without duplicates.
