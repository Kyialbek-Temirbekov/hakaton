# Course Finder API

## Description
This project is a Django-based API for finding university courses based on various criteria such as language proficiency, test scores, and academic requirements. The system integrates with both a DAAD (German Academic Exchange Service) API and OpenAI's GPT to provide course search functionality. Users can search for courses either by specifying criteria directly or by providing natural language text that gets processed by GPT to extract search parameters.

## Features
- User authentication (registration and login)
- Course search with filters (TOEFL, IELTS, GPA, GRE, etc.)
- Natural language processing via GPT to extract search parameters
- Integration with DAAD's course database
- Swagger/Redoc documentation

## Technologies Used
- **Backend**: Django, Django REST Framework
- **Database**: PostgreSQL
- **Authentication**: JWT (JSON Web Tokens)
- **API Documentation**: drf-yasg (Swagger/OpenAPI)
- **Natural Language Processing**: OpenAI GPT-3.5
- **Containerization**: Docker
- **Web Server**: Gunicorn

## Setup and Usage
1. Clone the repository
2. Create a `.env` file with your OpenAI API key: `GPT_API_KEY=your_api_key_here`
3. Run the project using Docker:
   ```bash
   docker-compose up --build
   ```
4. The API will be available at `http://localhost:8000`

## API Endpoints
- Documentation:
  - Swagger UI: `/swagger/`
  - ReDoc: `/redoc/` or `/docs/`
- Authentication:
  - Register: `/users/register/`
  - Login: `/users/login/`
- Course Search:
  - Direct search: `/course/search/`
  - GPT-assisted search: `/course/gpt/`

## Requirements
- Docker
- Docker Compose
- OpenAI API key (for GPT functionality)
