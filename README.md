#  AI Email Reply Generator

An AI-powered Email Reply Generator built using **Spring Boot** and **Groq LLM API**. The application generates professional email replies in different tones based on the original email content.

---

#  Features

-  AI-generated email replies
-  Multiple reply tones
- Professional
- Friendly
- Formal
- Casual
-  Fast response using Groq LLM
-  REST API built with Spring Boot
-  Environment variable support for API keys
-  JSON-based request and response


# Tech Stack

- Java 21
- Spring Boot 3
- Spring Web
- Spring WebFlux (WebClient)
- Maven
- Groq API (Llama 3.3 70B)
- Jackson
- Lombok



# Project Structure


email-writer-sb
│
├── controller
├── service
├── model
├── resources
│   └── application.properties
├── pom.xml
└── README.md




# API Endpoint

# Generate Email Reply

*POST*


http://localhost:8080/api/email/generate


# Request Body

```json
{
  "emailContent": "Can we schedule a meeting tomorrow?",
  "tone": "Professional"
}
```

# Sample Response

```text
Dear Sir/Madam,

Thank you for your email.

Tomorrow works perfectly for me. I look forward to our meeting.

Best Regards,
```

---

# Configuration

Configure your API credentials in `application.properties`.

```properties
groq.api.url=https://api.groq.com/openai/v1/chat/completions
groq.api.key=${GROQ_API_KEY}
groq.model=llama-3.3-70b-versatile
```

Set your environment variable:

```
GROQ_API_KEY=your_api_key_here
```

---

## ▶️ Run the Project

Clone the repository

```bash
git clone https://github.com/yourusername/email-writer-sb.git
```

Go inside the project

```bash
cd email-writer-sb
```

Run

```bash
mvn spring-boot:run
```

The application will start at

```
http://localhost:8080
```

---

## 🧪 Testing

Use Postman

```
POST http://localhost:8080/api/email/generate
```

Body

```json
{
    "emailContent":"Can we meet tomorrow?",
    "tone":"Professional"
}
```

## 👨‍💻 Author

**Abhishek**

GitHub:https://github.com/Abhii8521
