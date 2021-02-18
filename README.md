# digital-names-api-read

Digital Names Overview

A Digital Name is a phonetic identifier allowing a user to tie multiple crypto wallet public keys to a single access point. This allows for an ease of use that is currently not available in the crypto space. Users are enabled, through our Read API, to search the active ledger of names to determine which are taken, and through our Write API to generate new names through 2 different avenues of access: Direct Purchase of a single name or, Credit Exchange which allows the user to bookmark name generation in order to mass generate new names for resale purposes.

Direction of access to buy a name (Direct Purchase):

Create an account on Digitalnames.IO
Purchase a digital name from the checkout system 
Using the Digital Address Book, you may tie this name to any number of address keys, thereby centralizing your wallet addresses for easy access.

Direction of access to generate new names (Credit Exchange)

Create an account on Digitalnames.IO
Purchase access to the Write API 
Utilizing the Commands within the API create layers of security with designated IP access functionality. Find out what access key owns specific names in order to make private purchases. 

*Note - (The full process of buying and using a Digital Name can be clearly viewed on reference Flowchart_DN at the following location: https://go.gliffy.com/go/publish/13399349?fbclid=IwAR1noStcCAXsCOOY-1fd6_-lI7g7L_7Mkg6EzksfBa0xvE59JMq0J7V_U9U)

Digital Names API Utility:

I) Read API Commands: Commands in this section of the API are designed specifically for easy access to real time data within the ledger, but do not allow the user to generate new phonetic Identifiers within it.

1 - Digital Name Lookup - Allows retail resellers/private users to see if a name they want is already active within the database. The api command lines are as follows:

Command: namelookup * required attribute DigitalName
http://usa.tnsapi.cloud/call.cfm?apikey=b8g2d5t5&command=namelookup&DigitalName=

 Command consists of the API url reference, which tells the server where in the registry to locate the phonetic identifier. Continuing, the command line function performs a query utilizing a ColdFusion reserved keyword that verifies the users API key against the server ledger. Finally a secondary ColdFusion reserved keyword queries the database for a match of the existing phonetic identifier. The required attribute for this command is the “DigitalName”.
 
2 - Public Key Lookup - Allows for the search of Public keys to show what names are attached to them. Creating an open user market similar to that of the domain name space.

Command: keylookup * required attribute DigitalName.symbol 
http://usa.tnsapi.cloud/call.cfm?apikey=b8g2d5t5&command=keylookup&DigitalName=


Command consists of the API url reference which tells the server where in the registry to locate the phonetic identifier. Additionally, the command line function performs a query utilizing a ColdFusion reserved keyword that verifies the users Public Key, which has been assigned to the phonetic identifier. The required attribute is “DigitalName.symbol”.
