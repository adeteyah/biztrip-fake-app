# Test Programming: Perjalanan Dinas Management Application

This repository contains the source code for a **Perjalanan Dinas Management Application** designed to manage employee business trips within a company. The application includes functionality for requesting, processing, and approving business trips, along with calculating allowances based on the trip distance.

---

## Features

### 1. User Authentication

- **Admin Role:** Assign roles to users (`PEGAWAI` or `DIVISI-SDM`).
- **Pegawai Role:** Request business trips.
- **SDM Role:** Review and approve business trip requests.

### 2. Business Trip Management

- **For Pegawai:**

  - Submit business trip requests with details:
    - Purpose of the trip.
    - Departure and return dates.
    - Origin and destination cities.
  - Automatic calculation of trip duration.

- **For SDM:**
  - Review and approve business trip requests.
  - View the total allowance to be disbursed for each approved trip.

### 3. Master Data Management

- Manage city data, including:
  - Name, latitude, longitude, province, island, and whether the city is abroad.
  - Example:
    ```json
    {
      "name": "Kota Bandung",
      "latitude": -6.9175,
      "longitude": 107.6191,
      "province": "Jawa Barat",
      "island": "Jawa",
      "is_abroad": false
    }
    ```

### 4. Allowance Calculation

- Based on the distance between origin and destination:
  - 0–60 km: No allowance.
  - > 60 km within the same province: **Rp 200,000/day**.
  - > 60 km to another province on the same island: **Rp 250,000/day**.
  - > 60 km to another island: **Rp 300,000/day**.
  - For international trips: **USD 50/day**.
- Distance is calculated using latitude and longitude.

---

## Requirements

### Technology Stack

You can implement the application using any programming language or framework. However, it is recommended to use:

- **PHP**: Laravel, Yii2, CI4
- **Java**: Spring Boot
- **Mobile**: React Native
- **Node.js**

### Functional Requirements

1. **Runnable Application** with a user interface.
2. User roles: `PEGAWAI`, `DIVISI-SDM`.
3. Business trip approval flow:
   - Request submission by `PEGAWAI`.
   - Approval processing by `DIVISI-SDM`.
4. Distance-based allowance calculation.

---

## Example Screenshots

1. **Login Form**  
   A login page for authentication with `username` and `password`.

2. **Business Trip List (Pegawai)**  
   Displays submitted trips for individual users.

3. **Business Trip Request Form**  
   A form to input trip details:

   - Purpose
   - Dates
   - Origin and destination cities.

4. **SDM - Business Trip List**  
   List of submitted trips for review and approval by SDM.

5. **SDM - Business Trip Approval**  
   Detailed view of a trip request showing the total allowance.

6. **Master Data Management**  
   CRUD interface for city data management.

---

## Getting Started

### Prerequisites

- Install your preferred framework and ensure required dependencies are met.
- Database setup for user, city, and trip data.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/adeteyah/biztrip-fake-app.git
   ```
