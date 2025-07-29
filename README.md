# ChatAI Agent PoC

A simple generative AI agent using the OpenAI API model.

## Prerequisites

### 1. Create an OpenAI Account
Create an account with OpenAI:
[https://platform.openai.com/](https://platform.openai.com/)

### 2. Generate API Keys and Create Organization
Generate the API keys and create an organization:
[https://platform.openai.com/settings/organization/general](https://platform.openai.com/settings/organization/general)

### 3. Configure API Key
Replace the API KEY (get it from the OpenAI dashboard under your profile) in the `application.properties` file:
```properties
openai.api.key=YOUR_OPENAI_API_KEY
```

### 4. Enable the Model
Enable the model in your OpenAI organization:
[https://platform.openai.com/settings/organization/general](https://platform.openai.com/settings/organization/general)

### 5. Configure the Model
Replace the model in the `application.properties` file:
```properties
openai.model=gpt-4o-mini
```

## Running the Application

### Start the Spring Boot Application
```bash
mvn spring-boot:run
```

### Test the API

Use the following curl command to test the chat endpoint:

```bash
curl --location 'http://localhost:8080/agent/chat' \
--header 'Content-Type: application/json' \
--data '{
    "message": "Can you write a Hello world for java?"
}'
```

## Sample Response

```json
{
  "response": "Certainly! Here's a simple \"Hello, World!\" program in Java:\n\n```java\npublic class HelloWorld {\n    public static void main(String[] args) {\n        System.out.println(\"Hello, World!\");\n    }\n}\n```\n\n### Explanation:\n- **public class HelloWorld**: This defines a public class named `HelloWorld`.\n- **public static void main(String[] args)**: This is the main method, which is the entry point of any Java application.\n- **System.out.println(\"Hello, World!\");**: This line prints \"Hello, World!\" to the console.\n\n### How to Run:\n1. Save the code in a file named `HelloWorld.java`.\n2. Open a terminal or command prompt and navigate to the directory where the file is saved.\n3. Compile the program with the command:\n   ```bash\n   javac HelloWorld.java\n   ```\n4. Run the compiled program with the command:\n   ```bash\n   java HelloWorld\n   ```\n\nYou should see the output:\n```\nHello, World!\n```"
}
```