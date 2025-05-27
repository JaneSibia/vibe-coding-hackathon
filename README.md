# MediSync Follow-Up Reminder System

## Overview
A human-centered healthtech app that helps clinics and doctors track patient follow-ups and send automated SMS/WhatsApp reminders to patients, reducing missed appointments and improving care adherence.

## Features
- Create follow-up appointments with patient details (name, diagnosis, phone, date)
- Automatic daily reminders sent via Twilio SMS or WhatsApp
- Patients can reschedule or cancel follow-ups easily
- Backend built with Node.js, Express, MongoDB, and node-cron
- Simple, responsive frontend with Bootstrap
- Input validation for all endpoints
- Patient dashboard filters appointments by phone number

## Tech Stack
- Frontend: HTML, CSS, JavaScript
- Backend: Node.js, Express.js
- Database: MongoDB (NoSQL)
- SMS/WhatsApp API: Twilio
- Scheduler: node-cron

## Installation & Setup

### Backend
```bash
git clone https://github.com/JaneSibia/vibe-coding-hackathon.git
cd vibe-coding-hackathon/backend
npm install
```

### Environment Variables

Copy `.env.example` to `.env` and set:

```
MONGO_URI=your_mongodb_connection_string
TWILIO_ACCOUNT_SID=your_twilio_account_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
TWILIO_PHONE_NUMBER=your_twilio_phone_number
```

### Start the Server
```bash
npm start
```

### Frontend
Open `frontend/index.html` in your browser.

## API Endpoints

### Create a New Visit
`POST /api/visits`
```json
{
  "patientName": "Jane Doe",
  "diagnosis": "UTI",
  "followUpDate": "2025-06-15T00:00:00.000Z",
  "phone": "+254712345678"
}
```

### Get All Follow-Ups
`GET /api/followups`

### Update a Follow-Up
`PUT /api/followups/:id`

### Delete a Follow-Up
`DELETE /api/followups/:id`

## Reminder System
Automated cron job sends daily SMS/WhatsApp reminders at 9 AM for upcoming appointments.

## Future Enhancements
- Doctor authentication system
- AI-powered follow-up interval suggestions
- Multi-language reminder support
- Patient health outcome analytics


## Contact
Jane Sibia — [janesibia24@gmail.com](mailto:janesibia24@gmail.com)  
GitHub: [JaneSibia](https://github.com/JaneSibia)
