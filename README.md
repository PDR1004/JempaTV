# JempaTV 📺

JempaTV is a web application developed using Angular and the ABP Framework, designed to be a personalized streaming platform. It allows users to discover, manage, and rate series and movies, providing a rich and interactive viewing experience.

## 🚀 Features

*   **Series Discovery:** Browse and search for series using IMDB IDs, with details fetched from external APIs.
*   **Watchlist Management:** Add series to a personal watchlist, track viewing status, and remove them.
*   **Personalized Recommendations:** Receive series recommendations based on user activity and ratings.
*   **User Authentication & Authorization:** Secure user accounts with login, registration, and role-based access control (Admin). 
*   **API Statistics Dashboard:** Monitor API usage, errors, and response times.
*   **User Profile Management:** Update user profile information, including profile pictures and email preferences.
*   **Notifications:** Receive in-app notifications for relevant events.
*   **Multi-language Support:** The application supports multiple languages, including English and Spanish.
*   **Admin Panel:** Access to administrative functionalities for managing the application.

## 🛠️ Tech Stack

*   **Frontend:** Angular, TypeScript, HTML, CSS, SCSS
*   **Backend:** .NET (ABP Framework)
*   **Databases:** Entity Framework Core (implied by migrations)
*   **Styling:** Bootstrap, Custom SCSS
*   **Libraries:** Swiper.js (carousels), Chart.js (data visualization), Ngx-Datatable
*   **Containerization:** Docker

## 📦 Installation

### Prerequisites

*   [.NET 8.0+ SDK](https://dotnet.microsoft.com/download/dotnet)
*   [Node.js v18 or v20](https://nodejs.org/en)
*   [Yarn](https://yarnpkg.com/)
*   [Docker](https://www.docker.com/get-started)

### Backend Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/PDR1004/JempaTV.git
    cd JempaTV
    ```

2.  **Install client-side dependencies (if you cloned the repo):**
    ```bash
    cd angular
    yarn install
    ```

3.  **Run the database migrator:**
    ```bash
    cd ../src/JempaTV.DbMigrator
    dotnet run
    ```
    This will create the initial database and seed initial data.

4.  **Generate a signing certificate (for production):**
    ```bash
    dotnet dev-certs https -v -ep openiddict.pfx -p 86402479-7d42-49ac-a3f0-e8dc50579021
    ```
    Replace the password (`86402479-7d42-49ac-a3f0-e8dc50579021`) as needed.

5.  **Configure connection strings:**
    Update `appsettings.json` and `appsettings.Development.json` in `src/JempaTV.HttpApi.Host` with your database connection details.

### Frontend Setup

1.  **Navigate to the Angular project:**
    ```bash
    cd angular
    ```

2.  **Install dependencies:**
    ```bash
    yarn install
    ```

3.  **Run the development server:**
    ```bash
    ng serve
    ```
    The application will be accessible at `http://localhost:4200/`.

### Docker Setup

*   The project includes `Dockerfile` configurations for both the Angular frontend and the .NET backend services.
*   Refer to the respective `Dockerfile`s for build and run instructions.

## ▶️ Usage

### Development

*   **Start the Angular development server:**
    ```bash
    cd angular
    ng serve
    ```
    Navigate to `http://localhost:4200/`.

*   **Run the backend services:**
    Refer to the `src/JempaTV.HttpApi.Host/Dockerfile` and `src/JempaTV.DbMigrator/Dockerfile` for instructions.

### Key Functionalities

*   **Home Page:**
    *   For logged-out users, displays introductory content and a login prompt.
    *   For logged-in users, showcases featured series with a carousel and a top 10 series carousel.
*   **Series:** Search for series by title, view details, and add them to your watchlist.
*   **Watchlist:** View your saved series, rate them, add comments, and remove them.
*   **API Management:** An admin-only section to view API statistics, errors, and user activity.
*   **Notifications:** Access your personal notifications.
*   **Settings:** Manage your profile picture, email preferences, and application language.

## 📚 Table of Contents

*   [Features](#-features)
*   [Tech Stack](#️-tech-stack)
*   [Installation](#-installation)
*   [Usage](#-usage)
*   [Project Structure](#-project-structure)
*   [Contributing](#-contributing)
*   [License](#-license)
*   [Important Links](#-important-links)
*   [Footer](#-footer)

## 🏗️ Project Structure

The project follows a layered architecture typical of ABP Framework applications:

*   `angular/`: Frontend application built with Angular.
*   `src/JempaTV.Application/`
*   `src/JempaTV.Application.Contracts/`
*   `src/JempaTV.Domain/`
*   `src/JempaTV.Domain.Shared/`
*   `src/JempaTV.EntityFrameworkCore/`
*   `src/JempaTV.HttpApi/`
*   `src/JempaTV.HttpApi.Host/`
*   `src/JempaTV.DbMigrator/`
*   `test/`: Unit and integration tests.

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

1.  **Fork the repository.**
2.  **Create a new branch** for your feature or bug fix.
3.  **Make your changes** and ensure they are well-tested.
4.  **Submit a Pull Request** with a clear description of your changes.

## 📜 License

This project is not licensed. (Based on repository information)

## 🔗 Important Links

*   **Repository:** [https://github.com/PDR1004/JempaTV](https://github.com/PDR1004/JempaTV)
*   **ABP Framework:** [https://abp.io/](https://abp.io/)

## 📝 Footer

© 2025 JempaTV

This project is maintained by [PDR1004](https://github.com/PDR1004).

[Fork on GitHub](https://github.com/PDR1004/JempaTV/fork)


---
**<p align="center">Generated by [ReadmeCodeGen](https://www.readmecodegen.com/)</p>**