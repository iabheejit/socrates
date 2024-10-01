# AI-Powered Course Generation System

This project implements an AI-powered system for generating and managing educational courses. It leverages OpenAI's GPT models to create personalized learning content and interacts with Airtable for data storage and management.

## Key Components

1. **OpenAI Integration**: Utilizes OpenAI's API to generate course content and module details.
2. **Airtable Integration**: Creates and populates tables in Airtable with course information.
3. **Course Generation**: Orchestrates the process of creating a complete course structure.
4. **Module Generation**: Produces detailed content for individual course modules.

## Main Functions

### `ask(courseName, language)`
Generates a 3-day lesson plan for a given course topic using OpenAI's GPT-4 model.

### `createTableFields(courseName, moduleNumber)`
Creates a table in Airtable with fields for each day and module of the course.

### `iterateThroughModule(courseOutline, goal, style, language)`
Processes the course outline to generate detailed content for each module.

### `generateCourse(courseName, goal, style, language)`
Orchestrates the entire course creation process, including table creation, content generation, and data population.

### `populateFields(moduleNumber, moduleDetails, courseName)`
Populates the Airtable with generated course content.

### `moduleGen(moduleTopic, goal, style, language)`
Generates content for individual modules using OpenAI's GPT-4 model.

## Setup

1. Install required dependencies:
   ```
   npm install dotenv openai
   ```

2. Set up environment variables in a `.env` file:
   ```
   OPENAI_API_KEY=your_openai_api_key
   OPENAI_ORG_KEY=your_openai_org_key
   ```

3. Ensure Airtable integration is properly configured (not shown in the provided code snippet).

## Usage

To generate a course:

```javascript
generateCourse("Data Structures", "Understand basic data structures", "Beginner", "English");
```

This will create a course on Data Structures, generate a lesson plan, create detailed module content, and populate an Airtable with the results.

## Error Handling

The system includes comprehensive error handling and logging throughout the process, ensuring robustness and easier debugging.
