# ChatAIAgent Spring Boot 3 GEN AI PoC
Simple generative AI Agent using OpenAPI model

Create account with OpenAPI:
> [https://platform.openai.com/)

Generates the API keys and also create a organization
> [https://platform.openai.com/settings/organization/general)

Replace the API KEY(get it from openai dashboard under your profile) in application.properties file
> openai.api.key=YOUR_OPENAI_API_KEY

Enable the model
> [https://platform.openai.com/settings/organization/general)

Replace the model in application.properties file
> openai.model=gpt-4o-mini

## Run Spring Boot application
```
mvn spring-boot:run
```
## CURL command
```
curl --location 'http://localhost:8080/agent/chat' \
--header 'Content-Type: application/json' \
--data '{
    "message": "What is confidential computing?"
}'

```
