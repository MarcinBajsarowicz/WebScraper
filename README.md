# WebScraper
## Project implementation steps
### Stages 1-3
1. Provide url of the product's opinions page
2. Send request to provided url
3. Fetch product name
4. Fetch opinions from the webpage
5. Parse opinions to extra required data
6. Check if there is a next oage with opinions
7. Repeat steps 4-6 for all pages with opinons about product
8. save acquired opinions
## Project inputs
### Products codes
-179676915
-9415447
-90558892
-51052425
### Opinion structure
| component|name|selector|
|----------|----|--------|
|opinion ID|opinion_id|[data-entry-id]|
|opinion’s author|author|.user-post__author-name|
|author’s recommendation|recomenadiotn|span.user-post__author-recomendation > em|
|score expressed in number of stars|score|span.user-post__score-count|
|opinion’s content|content|div.user-post__text|
|list of product advantages|pros|div.review-feature__item--positive|
|list of product disadvantages|cons|div.review-feature__item--negative|
|how many users think that opinion was helpful|helpful|button.vote-yes > yes|
|how many users think that opinion was unhelpful|unhelpful|button.vote-yes > no|
|publishing date|publish_date|span.user-post__published > time:nth-of-type(1)[datetime]|
|purchase date|purchase_date|span.user-post__published > time:nth-of-type(2)[datetime]|    