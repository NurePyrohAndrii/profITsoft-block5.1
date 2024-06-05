## Follow steps to successfully run the project

- Open docker
- Clone projects (clone current repo and [this](https://github.com/NurePyrohAndrii/profITsoft-block2))
- Open the terminal and execute the following command: "docker network create flights-block5_1_external"
- Open the folder containing docker-compose.yaml file and edit .env file with your own settings (How to get settings, watch below)
- Open both projects in the terminal within the folder containing docker-compose.yaml file and execute the following command: "docker-compose up -d"
- After previous action, it will take some time to elastic search to start and service to be up and running as well, so you should wait and ensure that all services are up and running


## How to get settings

- If you want to use your email for sending notifications, you should follow steps described there in a topic, [link](https://stackoverflow.com/questions/72577189/gmail-smtp-server-stopped-working-as-it-no-longer-support-less-secure-apps)
- Also, you can create your own .env file with the following settings and put it in the root of the project of email-service
  ```properties
  MAIL_HOST=smtp.gmail.com
  MAIL_PORT=587
  MAIL_USERNAME={your_email}
  MAIL_PASSWORD={your_app_password}
  MAIL_SMTP_AUTH=true
  MAIL_SMTP_STARTTLS_ENABLE=true
  MAIL_DEFAULT_RECIPIENT={recipient_email}
    ```

Also,
you can find a "postman" collection
to interact with the API
by following README.md instructions in another [project](https://github.com/NurePyrohAndrii/profITsoft-block2).