# AI Meeting Scheduler Assistant

## Project Overview

AI Meeting Scheduler Assistant is a Python-based prototype that parses natural language meeting requests and suggests three possible meeting slots from a mock calendar.

The assistant uses rule-based text processing and regular expressions to understand user preferences such as meeting duration and time preferences.

## Objective

The objective of this project is to build a simple assistant that can:

- Accept scheduling requests in plain text
- Extract meeting details from user input
- Check available slots from a mock calendar
- Suggest three suitable meeting times

## Technologies Used

- Python
- Jupyter Notebook
- Regular Expressions (Regex)
- Date and Time handling
- JSON for mock calendar data

## Project Structure

```
AI_Meeting_Scheduler
│
├── data
│   └── mock_calendar.json
│
├── main.ipynb
│
├── README.md
│
└── requirements.txt
```

## How It Works

1. User enters a meeting request in plain text.
2. The system extracts:
   - Meeting duration
   - Time preference (morning, afternoon, evening)
   - Day preference (if provided)
3. The assistant checks available slots from the mock calendar.
4. It returns three suggested meeting slots.

## Sample Inputs and Outputs

### Example 1

Input:

```
Schedule a meeting Monday afternoon for 30 minutes
```

Output:

```
Suggested Meeting Slots:

1. Monday 14:00 - 14:30
2. Monday 15:00 - 15:30
3. Tuesday 13:00 - 13:30
```

---

### Example 2

Input:

```
I need a meeting Tuesday morning for 1 hour
```

Output:

```
Suggested Meeting Slots:

1. Monday 14:00 - 15:00
2. Monday 15:00 - 16:00
3. Tuesday 13:00 - 14:00
```

## Features

- Plain text meeting request parsing
- Regex-based information extraction
- Supports meeting duration in minutes and hours
- Generates three candidate meeting slots
- Uses mock calendar data instead of a real calendar API

## Assumptions

- The calendar data is sample/mock data.
- The system does not connect to real calendar services.
- User provides meeting duration in the request.
- The first three available slots are suggested.

## Edge Cases Handled

- Meeting duration in minutes:
  - Example: "30 minutes"

- Meeting duration in hours:
  - Example: "1 hour" converted into 60 minutes

- Missing preferences are handled using default availability.

## Future Improvements

- Connect with Google Calendar or Microsoft Outlook API
- Use advanced NLP models for better understanding
- Add a web interface using MERN stack
- Add user authentication and database storage

## Conclusion

This project demonstrates a basic AI scheduling assistant prototype that can understand simple scheduling requests and recommend suitable meeting slots using Python.