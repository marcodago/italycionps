Net Promoter Score
====================================

### Italy EOSD NPS tool
This application is intended to support the NPS metric process. It ahs been developed in Bluemix,
using the Node-Red starter boilerplate.  

### How does this work?
When you open the webpage, you are requested to evaluate EOSD department services in a scale
from 0 to 10.

![NPS Score Screenshot](nps_score.png)

When you press the submit button, score is then registered, as a record, in Cloudant DB.

The second webpage, show you the overall NPS score for EOSD department.

![NPS Gauge Screenshot](nps_gauge.png)

### Customising Node-RED
This repository is here to be cloned, modified and re-used to allow anyone create
their own Node-RED based application that can be quickly deployed to Bluemix.

The default flows are stored in the `defaults` directory in the file called `flow.json`.
When the application is first started, this flow is copied to the attached Cloudant
instance. When a change is deployed from the editor, the version in cloudant will
be updated - not this file.

The web content you get when you go to the application's URL is stored under the
`public` directory.

If you do clone this repository, make sure you update this `README.md` file to point
the `Deploy to Bluemix` button at your repository.

If you want to change the name of the Cloudant instance that gets created, the memory
allocated to the application or other deploy-time options, have a look in `manifest.yml`.
