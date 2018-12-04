# Adding a service to the GDPR Tracker database

We use [Github Flow](https://guides.github.com/introduction/flow/index.html), so all code changes happen through pull requests
are the best way to propose changes to the codebase (we use [Github Flow](https://guides.github.com/introduction/flow/index.html)). We actively welcome your pull requests:

- Fork the repo and create your branch with the name of the service you want to add from `master`.
- Add a file with the service name to the data folder.
- Make sure your data follows the following [schema](https://github.com/privacyradius/gdpr-tracker/blob/master/schema.json). Please look into the following [example](https://github.com/privacyradius/gdpr-tracker/blob/master/example.json) for more info
- If you're unsure about certain data points leave them out or check with the company offering the service.
-  Use [signed commits](https://help.github.com/articles/signing-commits-with-gpg/). We enforce signed commits to verify the identity of contributors.
- Ensure the test suite passes.
- Issue that pull request!

## Example

```
{
  "id": "acme",
  "name": "Acme",
  "description": "CRM & Customer platform for SMBs",
  "categories": [
    "CRM", 
    "Customer Support"
  ],
  "iconUrl": "https://pbs.twimg.com/profile_images/922908923207839744/5EZID3tH_400x400.jpg",
  "website": "https://www.acmesaas.com",
  "applicationUrl": "https://app.acmesaas.com",    
  "twitter": "acme",
  "countryHQ": "US",
  "gdprReadyStatus": "inProgress",
  "privacyUrl": "https://www.acmesaas.com/privacy",
  "dsarUrl": "https://bs.gdprform.io",
  "dpaUrl": "https://www.acmesaas.com/dpa",
  "subprocessorsUrl": "https://www.acmesaas.com/subprocessors",
  "dataCenters": [
    "EU"
  ],
  "hostingProviders": [
    "AWS", 
    "Digital Ocean"
  ],
  "contacts": [
    {
      "type": "DPO",
      "name": "John Doe",
      "email": "john@dpo.com",
      "region": "EU"
    }, 
    {
      "type": "DPO",
      "name": "Tim Doe",
      "email": "tim@dpo.com",
      "region": "US"
    }
  ],
  "certifications": [
    "ISO 27001", 
    "HIPAA"
  ],
  "dataBreaches": [
    {
      "date": "10/12/2017",
      "url": "https://www.beatswtich.com/breach"
    }
  ],
  "articles": [
    {
      "date": "02/12/2018",
      "url": "https://www.beatswtich.com/gdpr"
    }
  ],
  "bugBountyProgramUrl": "https://www.beatswtich.com/bounty-program",
  "statusUrl": "https://www.beatswtich.com/status",
  "statusTwitter": "beatswitchstatus",
  "gdprUrl": "https://www.acmesaas.com/gdpr",
  "verified": true
}
```

## Don’t use Github?

If you're not able to add a service Github through you can use [the following form](https://docs.google.com/forms/d/e/1FAIpQLScVfEdJE1rg_9D3f_S4AiELNm71n5QNV4i5ne9LHuaLeaFASw/viewform) to add a service. 

## We Develop with Github

We use github to host our data, code, to track issues and feature requests, as well as accept pull requests.

## Any contributions you make will be under the MIT License

In short, when you submit code changes, your submissions are understood to be under the same [MIT License](http://choosealicense.com/licenses/mit/) that covers the project. Feel free to contact the maintainers if that's a concern.

## Report bugs using Github's [issues](https://github.com/privacyradius/gdpr-tracker/issues)

We use GitHub issues to track public bugs. Report a bug by [opening a new issue](https://github.com/privacyradius/gdpr-tracker/issues); it's that easy!

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

## References

This document was adapted from the open-source contribution guidelines for [Facebook's Draft](https://github.com/facebook/draft-js/blob/a9316a723f9e918afde44dea68b5f9f39b7d9b00/CONTRIBUTING.md).
