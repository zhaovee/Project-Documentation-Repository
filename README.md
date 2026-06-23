# Lab and Equipment Booking System Documentation

## Project Description

The Lab and Equipment Booking System is a web-based platform developed to manage laboratory and equipment booking requests at Universiti Teknologi Malaysia Kuala Lumpur. The system replaces manual booking processes such as Google Forms, email communication, and manual staff verification with a centralized workflow.

This documentation repository contains project documents, diagrams, database design, UAT files, screenshots, and related project links for the Lab and Equipment Booking System.

## Main Features

- User registration, login, and password reset
- Role-based access for Student/Staff, PIC, Unit Leader, and PPMU
- Lab and equipment browsing
- Equipment booking request submission
- PIC token generation and verification
- Unit Leader recommendation workflow
- PPMU final approval workflow
- Equipment price and availability management
- Booking record tracking
- Receipt and quotation PDF generation
- Email notifications for booking updates

## Members

| Name | Role |
|---|---|
| Muhammad Usman | Project Manager |
| Zhao Wei | Team Member |
| Abdulrahman Siad | Team Member |
| Syafi | Team Member |
| Adam Iskandar | Team Member |

## Related Links

| Item | Link |
|---|---|
| Code Repository | https://github.com/KaifHalak/AD-Project |


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
│   │   ├── PPMU/
│   │   ├── register/
│   │   ├── reset-password/
│   │   ├── token-verification/
│   │   └── unit-leader/
│   ├── components/
│   └── lib/
├── supabase/
│   └── migrations/
├── tools/
├── package.json
└── README.md
```
