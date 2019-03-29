# CollaborateSyncQuote

This project allows you to automatically update a CPQ Quote record to "Primary" and "Accepted" if the page is accepted in a Collaborate document. This can also be generalized to other objects used with Collaborate's page-level acceptance and repeatable pages functionality. It uses Apex and Collaborate's REST API to do this.

1. Trigger when Octiv Document record updated AND Status = Accepted (can also add more filters here)
2. Apex class fired from Trigger
   - reaches out to Collaborate API to get pages in the particular document based on Collaborate Document Id
   - loops through pages to see 1) repeated object and 2) page status
   - stores Salesforce record Id from metadata of accepted page
   - updates the Salesforce record to Primary and Accepted
3. CPQ should auto-sync this quote to Oppty, however, GDO required me to rebuild this functionality in a Flow and Proces Builder.

**You'll need to create a Remote Site for your Collaborate account site URL**
For example, adding "https://companyname.octiv.com"

**You'll need to add your user API key in the appropriate place in your Apex code (ideally I'll just create a Custom Setting for this)**
