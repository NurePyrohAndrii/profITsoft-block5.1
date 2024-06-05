## Follow steps to successfully run the project

- Open docker
- Clone projects (clone current repo and [this](https://github.com/NurePyrohAndrii/profITsoft-block2))
- Open the terminal and execute the following command: "docker network create flights-block5_1_external"
- Open the folder containing docker-compose.yaml file and edit .env file with your own settings (How to get settings,
  watch below)
- Open both projects in the terminal within the folder containing docker-compose.yaml file and execute the following
  command: "docker-compose up -d"
- After previous action, it will take some time to elastic search to start and service to be up and running as well, so
  you should wait and ensure that all services are up and running

## How to get settings

You can create your own .env file with the following settings and put it in the root of the project of
email-service

```properties
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME={your_email}
MAIL_PASSWORD={your_app_password}
MAIL_SMTP_AUTH=true
MAIL_SMTP_STARTTLS_ENABLE=true
MAIL_DEFAULT_RECIPIENT={recipient_email}
```

By default, we use port 587 for sending emails which is by SMTP protocol.  
Ensure you put your email instead of {your_email} and recipient email instead of {recipient_email} in the .env file.
To get an app password for your email, follow the steps below:

1. Login to your gmail
2. Go to Security setting and Enable 2-factor authentication
3. After enabling this, you can see an app passwords option. Click [here](https://myaccount.google.com/apppasswords)!
4. And then, from Your app passwords tab, select Another option and put your app name and click GENERATE button to get new app password.
5. Finally, copy digit 16 of password and click done.
   Now use this password instead of {your_app_password} in the .env file.

Also,
you can find a "postman" collection
to interact with the API
by following README.md instructions in another [project](https://github.com/NurePyrohAndrii/profITsoft-block2).