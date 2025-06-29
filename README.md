# Postman API Automation Integration with Github Actions #

This repository is demonstration for POC for integrating postman tests with github actions. The Tests are written in Postman and they are executed on the VM with the help of newman and newman-reported-htmlextra.
Github actions will trigger the project execution on every push to the main branch.You can also execute the project manually using workflow_dispatch.The Projects runs on a schedule time with the help of cron job.

The HTML report is archived and kept in the artifact section for the team to download it.Along with that they can view the report directly from github page : https://ashlesha868.github.io/Phoenix-Inwarranty-Flow/.
The latest report is mailed to the team members using GMAIL SMTP.


# Testing Coverage #
1.Happy Flow Testing

2.Negative Testing and Edge Case Testing

3.Token Testing

4.Data driven testing with CSV

5.Schema Validation

6.Secrets Management with GitHub secrets


# Tech Stack #

1.Postman

2.Nodejs 22v

3.Newman

4.Newman-Reported-Htmlextra

5.Github Actions

6.Gmail SMTP

7.Github Pages

8.CSV for Data Driven testing

9.AWS EC2 instance for Self Hosted github runner.


# Github Pages #

You can directly view the latest test report of the Postman test at the Github Page link : https://ashlesha868.github.io/Phoenix-Inwarranty-Flow/.

# HTML Report #
The report will be created in the newman folder 
![Postman Report](https://github.com/Ashlesha868/Phoenix-Inwarranty-Flow/blob/static-content/newman%20report%20screenshot.png)

# Project Structure #


```
Phoenix Inwarranty Flow
├─ Inwarranty-Flow Collection.postman_collection.json  # Collection file
├─ QA.postman_environment.json # Environment File
└─ testData.csv # TestData File

```

# How to run the project? #
You can run the project on your local system
1.Clone the project on Local system : https://github.com/Ashlesha868/Phoenix-Inwarranty-Flow.git

2.Install Nodejs and NPM from https://nodejs.org/en

3.Install Newman using ```npm install -g newman```

4.Install Newman-reporter-htmlextra using  ```npm install -g newman-reporter-htmlextra```

5.Run the newman command : 
```
              newman run 'Inwarranty-Flow Collection.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testData.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
```

             









