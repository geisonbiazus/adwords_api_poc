# Google Adwords API

To use the API we need an AdWords manager account with an aproved develper token. See [Sign up documentation](https://developers.google.com/adwords/api/docs/guides/signup) for more information.

Google Adwords has a [Required Minimum Functionality](https://developers.google.com/adwords/api/docs/requirements). If an AdWords API Client provides any functionality related to TargetingIdeaService or TrafficEstimatorService, it must fully implement the required Creation Functionality, Management Functionality and Reporting Functionality marked "Required" in [the table](https://developers.google.com/adwords/api/docs/requirements#feature-implementation).

The corresponding feature to Keywords Planner on API is [Targeting Idea Service](https://developers.google.com/adwords/api/docs/guides/targeting-idea-service). See [API doc](https://developers.google.com/adwords/api/docs/reference/v201607/TargetingIdeaService) for more information

The TargetingIdeaService and TrafficEstimatorService return dummy data to test accounts. Source: [
Managing Accounts](https://developers.google.com/adwords/api/docs/guides/accounts-overview#test_accounts)

# Running the example]

To run the example you will need an [Adwords Manager Account](https://developers.google.com/adwords/api/docs/guides/signup) and an [Adwords Test Account](https://developers.google.com/adwords/api/docs/guides/accounts-overview#test_accounts)

On the **Manager Account** request a **developer token** on `Account Settings/AdWords API Center`

On https://console.developers.google.com/ create an App to get the OAuth2 **client_id** and **client_secret**. Choose the type **other** when requested.

On the **Test Account** get your **Customer ID** on the top of the page.

Edit the file `adwords_api.yml` and add the following information:

- oauth2_client_id
- oauth2_client_secret
- developer_token
- client_customer_id

Run the following command to authenticate your app:

```
ruby setup_oauth2.rb
```

When requested to update `adwords_api.yml` file, type **y** and confirm it.

Finally run the example with the command:

```
ruby keyword_ideas.rb
```
