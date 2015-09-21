# hi9-deployment-workflow
*Deployment Workflow for Hi9*

##Workflow

Github Issue and Trello Card with :T being on the Github Issue when it is in Trello. 

Branch the Github repo with the identifier Issue No
Push and Sync Branch with repo on that issue number
Make sure you commit and push at least every hour

Test Locally on that branch
Create Demo
Deploy to Testing Server using Firebase Deploy
Inform Wo
Move onto next card and issue

QA
Wo then takes over. 
Wo Tests and creates Ghost Inspector for the demo of the element so a demo has to be created
Merge Master
Deploy to Dev
Test
Deploy to Live
Move Card and Close Issue

##Version Control

Wo will be doing the deployment, QA and Version control to the Live site.

I will QA for now until we create an automated flow. I will tag according to Semantic Versioning so we have MAJOR RELEASE.FEATURE RELEASE.PATCH 1.1.1. I will tag and annotate the commits to Master after it has been merged and after I have done some basic tests on the Testing Server which will be on the Dev Branch.
I will put that up on Slack with #QA so we have a story we can go back to. Once we know more about what tests we need we can then start automating. Very MVP of us. If any one has anyway to improve this in the short term then please comment. This way we don't get bogged down in testing and integration right now but learn what we are looking for. We have found issues with cloud based testing suites and using Google Oauth due to security. We will most probably have to use something like a Rasberry PI and Seliunium with Phantomjs to get round the Google Oauth issue in the medium term.
Then when we add more ways to login into the system with more conventional Username and Password we can go back to Cloud based systems that can handle that. Again if anyone has better short term solution then please comment

##Live Server
Firebase App address for the Live Server is

[https://hi9site.firebaseio.com/](https://hi9site.firebaseio.com/)

##Testing Server
Firebase App address for the Testing Server is

[https://hi9-testing.firebaseio.com/](https://hi9-testing.firebaseio.com/)

###Work on dev branch

```firebase deploy``` will deploy to https://hi9-testing.firebaseio.com/ on dev branch

