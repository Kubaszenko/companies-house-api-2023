# Companies House
An ES6 Node.js library for the [Companies House API](https://developer.company-information.service.gov.uk/)
# Installation instructions
Run `npm install --save companies-house-api-2023`
# Usage
First you will need to create an account on companies house and get an API Key

Then you will need to include the library

~~~js
const CHA = require('companies-house-api-2023');
const cha = new CHA('YOUR_API_KEY');
~~~
Here is an example

~~~js
cha.searchForCompanyById(companyID).then(result => {
	console.log(result);
}).catch(err => {
	console.log(err);
});
~~~

For a full list of response formats please visit [Companies House API Docs](https://developer.company-information.service.gov.uk/)

## Search Methods

~~~js
searchForCompanyById(id)

//These methods can take an optional second argument which 
//is an integer limit of how many results you want back

searchForCompanyByGenericTerm(query)
searchAll(query)
searchForOfficer(query)
searchForDisqualifiedOfficer(query)
~~~
## Profile Methods

~~~js
returnProfileBy(companyNumber)
~~~