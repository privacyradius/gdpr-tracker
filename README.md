# [GDPR Tracker](https://www.gdprtracker.io/) 

<img src="https://github.com/privacyradius/gdpr-tracker/blob/master/images/screenshot.png">

[GDPR Tracker](https://www.gdprtracker.io/) is a crowdsourced directory that makes it easier for companies and consumers to keep track of the data handling practices of their subcontractors and cloud services in real-time.

This repository holds all the services displayed in the directory. We strongly believe that data handling practices should be easily available to business & customers. 

## [How to add a service?](https://github.com/privacyradius/gdpr-tracker/blob/master/CONTRIBUTING.md)

You can add a service by following the [contribution guidelines](https://github.com/privacyradius/gdpr-tracker/blob/master/CONTRIBUTING.md).

## Format

We use JSON Schema to validate the data and to maintain a high level of data quality. Please find the schema at the [following location](https://github.com/privacyradius/gdpr-tracker/blob/master/schema.json).

| Field            	| Type   	| Format           	| Required 	| Description                                               	| Options                                                                             	|
|------------------	|--------	|------------------	|----------	|-----------------------------------------------------------	|-------------------------------------------------------------------------------------	|
| id               	| string 	|                  	| *        	| Unique id to identify the company                         	|                                                                                     	|
| name             	| string 	|                  	| *        	| Name of the company                                       	|                                                                                     	|
| description      	| string 	|                  	| *        	| Description of the service                                	|                                                                                     	|
| categories       	| array  	|                  	| *        	| Categories that the service belongs to                    	|                                                                                     	|
| iconUrl          	| string 	| url              	| *        	| URL to the icon of the service (recommended size 400x400) 	|                                                                                     	|
| countryHQ        	| string 	| ISO ALPHA-2 code 	| *        	| Country of HQ                                             	|                                                                                     	|
| gdprReadyStatus  	| enum   	|                  	| *        	| GDPR readiness status of this service                     	| unknown<br> inProgress<br> ready<br> nonCompliant                                   	|
| privacyUrl       	| string 	| url              	|          	| Link to privacy policy                                    	|                                                                                     	|
| dsarFormUrl      	| string 	| url              	|          	| Data Subject Access Rights Form URL                       	|                                                                                     	|
| dpaUrl           	| string 	| url              	|          	| Data Processing Agreement URL                             	|                                                                                     	|
| dataCenters      	| array  	|                  	|          	| Locations where data is hosted                            	|                                                                                     	|
| hostingProviders 	| array  	|                  	|          	| Hosting providers                                         	|                                                                                     	|
| contacts         	| array  	|                  	|          	| Appointed DPOs or privacy officers per region             	|                                                                                     	|
| certifications   	| enum   	|                  	|          	| Certifications                                            	| ISO 27001<br> PCI DSS<br> SOC 2 Type I<br> SOC 2 Type II<br> HIPAA<br> HITECH<br> RESO 	|
| dataBreaches     	| array  	|                  	|          	| Reported data breaches                                    	|                                                                                     	|
| articles         	| array  	|                  	|          	| GDPR & privacy related articles                           	|                                                                                     	|

### [Example](https://github.com/privacyradius/gdpr-tracker/blob/master/schema.json)

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
  "countryHQ": "US",
  "gdprReadyStatus": "inProgress",
  "privacyUrl": "https://www.acmesaas.com/privacy",
  "dsarFormUrl": "https://bs.gdprform.io",
  "dpaUrl": "https://www.acmesaas.com/dpa",
  "dataCenters": [
    "EU"
  ],
  "hostingPartners": [
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
  ]
}
```

## Removal

If you want your service to be removed from the tracker. Send in a pull request with the reason stated.

## License

MIT License. Please see the [license file](https://github.com/privacyradius/gdpr-tracker/blob/master/LICENSE) for more information.

## About

Made in Belgium / Europe

The GDPR Tracker is created by Privacy Radius. Privacy Radius is a European provider of AI-powered data and privacy solutions to help companies create trusted environments to protect consumers' privacy and data rights. 

## Links

* [GDPR Tracker](https://www.gdprtracker.io)
* [GDPR Checklist](https://www.gdprchecklist.io)
* [GDPR Form](https://www.gdprform.io)
* [Twitter](https://twitter.com/privacyradius)
