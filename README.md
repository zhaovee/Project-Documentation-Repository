# Lab and Equipment Booking System

## Project Overview

The Lab and Equipment Booking System is a web-based platform developed for managing laboratory and equipment booking requests at Universiti Teknologi Malaysia Kuala Lumpur. The system helps replace manual booking processes such as Google Forms, email communication, and manual staff verification with a centralized digital workflow.

The system supports Student/Staff booking requests, PIC token authorization, Unit Leader recommendation, PPMU final approval, equipment management, receipt and quotation PDF generation, and email notifications.

## Main Features

- User registration, login, and password reset
- Role-based access for Student/Staff, PIC, Unit Leader, and PPMU
- Browse labs and equipment
- Search and filter labs or equipment by programme/course
- View lab and equipment details, status, price, staff contact, and schedule
- Create booking requests with multiple equipment items
- Validate booking rules and prevent booking conflicts
- PIC token generation and verification
- Unit Leader recommendation workflow
- PPMU final approval workflow
- Equipment price and availability management
- Booking record tracking
- Booking receipt and quotation PDF download
- Email notifications for booking submission, review, approval, rejection, and quotation availability

## User Roles

| Role | Description |
|---|---|
| Student/Staff | Browse labs and equipment, create booking requests, view booking records, cancel eligible requests, and download documents. |
| PIC | Generate, assign, view, and expire PIC tokens for booking authorization. |
| Unit Leader | Review booking requests and recommend or reject equipment items before PPMU final review. |
| PPMU | Perform final approval, edit final price, manage equipment price and availability, and confirm booking decisions. |

## Technology Stack

| Layer | Technology |
|---|---|
| Frontend | Next.js, React |
| Backend | Next.js API Routes |
| Database | Supabase PostgreSQL |
| PDF Generation | jsPDF |
| Email Notification | Nodemailer / SMTP |
| Styling | Tailwind CSS |

## System Architecture

The system follows a three-tier architecture:

1. **Presentation Tier**  
   Next.js and React frontend pages used by Student/Staff, PIC, Unit Leader, and PPMU.

2. **Application Logic Tier**  
   Next.js API routes handle authentication, booking validation, token verification, review workflow, approval workflow, equipment management, PDF generation, and email notification.

3. **Data Tier**  
   Supabase PostgreSQL stores users, labs, equipment, booking requests, equipment booking items, PIC tokens, review decisions, and quotation records.

## Main API Modules

| Module | Description |
|---|---|
| Authentication APIs | Handle registration, login, password reset, and verification status. |
| Booking APIs | Handle booking creation, booking records, availability checking, cancellation, and quotation download. |
| PIC Token APIs | Handle user search, token generation, token assignment, token verification, and token expiry. |
| Unit Leader APIs | Handle booking request review, recommendation, rejection, and remarks. |
| PPMU APIs | Handle final approval, rejection, final price editing, and request status updates. |
| Equipment APIs | Handle equipment listing, price update, and availability status update. |

## Database Design

The database is managed using Supabase PostgreSQL. The main tables include:

- `users`
- `labs`
- `equipment`
- `bookings`
- `equipment_bookings`
- `pic_tokens`
- `booking_process`
- `booking_quotations`

The database schema and ERD are included in the project documentation.

## Project Structure

```text
AD-Project/
├── public/
├── scripts/
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   ├── auth/
│   │   │   ├── bookings/
│   │   │   ├── pic/
│   │   │   ├── ppmu/
│   │   │   ├── tokens/
│   │   │   ├── unit-leader/
│   │   │   └── users/
│   │   ├── account/
│   │   ├── booking/
│   │   ├── booking-records/
│   │   ├── complete-booking/
│   │   ├── forgot-password/
│   │   ├── unit-leader/
│   │   ├── PPMU/
│   │   ├── register/
│   │   ├── reset-password/
│   │   └── token-verification/
│   ├── components/
│   └── lib/
├── supabase/
│   └── migrations/
├── tools/
├── work_docs/
├── outputs/
├── package.json
└── README.md
```

## Installation and Setup

1. Clone the repository.

```bash
git clone <code-repository-link>
```

2. Install dependencies.

```bash
npm install
```

3. Configure environment variables in `.env`.

```text
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SUPABASE_SERVICE_ROLE_KEY=
SMTP_HOST=
SMTP_PORT=
SMTP_USER=
SMTP_PASS=
```

4. Run the development server.

```bash
npm run dev
```

5. Open the application in the browser.

```text
http://localhost:3000
```

## Related Links

| Item | Link |
|---|---|
| Code Repository | https://github.com/KaifHalak/AD-Project |

## Testing

User Acceptance Testing (UAT) was prepared based on the main system roles:

- Student/Staff
- PIC
- Unit Leader
- PPMU

The UAT document includes test criteria, responsible party, priority, test date, response, and comments for each role.

## Project Status

This project is developed as an academic application development project and prototype for managing lab and equipment booking workflows.
