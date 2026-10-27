# Crop Harvest Record Management System

A full-stack agricultural management application designed to digitize farm operations, streamline crop lifecycle tracking, manage harvest records, and generate meaningful yield analytics. Built with Python, Flask, SQLite, HTML, CSS, and JavaScript, the system provides farmers and administrators with a centralized platform for efficient agricultural recordkeeping and data-driven decision-making.

**Live Demo:** https://crop-harvest-project.vercel.app/

**GitHub Repository:** https://github.com/SRI-VIGNESH-WORKS/Crop-Harvest-Record-Management-System

---

## Project Overview

The Crop Harvest Record Management System is a web-based application developed to simplify agricultural recordkeeping and improve harvest management.

Traditional farming records are often maintained using paper documents or spreadsheets, making it difficult to track crop growth, organize farm information, calculate yields, and generate accurate reports.

This application addresses these challenges by providing a centralized system for managing farms, fields, crops, and harvest records. It automatically standardizes different measurement units into kilogram equivalents and provides interactive dashboards, analytical charts, and downloadable reports.

The system is designed for farmers, farm managers, and agricultural administrators who need an organized and efficient way to manage agricultural operations.

## Key Features

### 1. Dashboard and Analytics

* View summarized statistics for farms, fields, active crops, and harvest records.
* Monitor total harvest yields using standardized kilogram equivalents.
* Visualize crop-wise yield distribution through interactive bar charts.
* Analyze harvest trends using line and area charts.
* Access important agricultural information through a centralized dashboard.

### 2. Farm and Field Management

* Create and manage multiple farms.
* Record farm locations, land areas, and descriptions.
* Organize individual fields within farms.
* Maintain field information, including soil types and irrigation systems.
* Manage relationships between farms and their associated fields.

### 3. Crop Lifecycle Management

* Register crops and their varieties.
* Record planting dates and expected harvest dates.
* Track crop growth through different lifecycle stages.
* Monitor crop statuses, including Planned, Planted, Growing, Ready for Harvest, Harvested, and Completed.
* Maintain crop information for effective agricultural planning.

### 4. Harvest Record Management

* Record harvest quantities, dates, quality grades, and storage locations.
* Automatically populate associated farm and field information when selecting a crop.
* Support multiple measurement units, including kilograms, tonnes, grams, bags, and crates.
* Search and filter harvest records using different criteria.
* Maintain organized harvest histories for agricultural analysis.

### 5. Automated Unit Conversion

* Convert harvest quantities into standardized kilogram equivalents.
* Support consistent calculations across different measurement units.
* Reduce manual calculation errors.
* Generate comparable yield summaries across crops, farms, and fields.

### 6. Reports and Data Export

* Generate reports for predefined and custom date ranges.
* Analyze harvest yields by crop, farm, and field.
* Filter records according to relevant criteria.
* Export filtered harvest records as CSV files.
* Print formatted reports for documentation and recordkeeping.

### 7. Authentication and User Management

* Provide session-based user authentication.
* Support role-based access for farmers and administrators.
* Allow farmers to manage their own agricultural records.
* Enable administrators to manage user accounts and oversee system-wide records.
* Protect passwords using secure hashing mechanisms.
* Apply user-level data isolation and authorization controls.

### 8. User Interface

* Responsive web application interface.
* Light and dark theme support.
* Interactive forms, modal dialogs, and notification messages.
* Custom SVG-based charts for lightweight data visualization.
* Dynamic frontend interactions without relying on a large frontend framework.

## Technology Stack

| Component          | Technology                     |
| ------------------ | ------------------------------ |
| Frontend           | HTML5, CSS3, JavaScript (ES6+) |
| Backend            | Python                         |
| Backend Framework  | Flask                          |
| Database           | SQLite                         |
| API Architecture   | REST API                       |
| Authentication     | Flask Sessions, Werkzeug       |
| Data Visualization | Custom SVG Charting Engine     |
| Data Export        | CSV                            |
| Testing            | Pytest                         |
| Deployment         | Vercel                         |

## System Architecture

The application follows a client-server architecture in which the frontend communicates with Flask REST API endpoints to manage and retrieve agricultural data.

```text
                 User
                   |
                   v
           Frontend Interface
          HTML, CSS, JavaScript
                   |
                   v
              REST API
             Flask Backend
                   |
                   v
              SQLite DB
                   |
                   v
        Data Processing and Analysis
                   |
                   v
       Dashboard, Charts and Reports
                   |
                   v
            CSV Data Export
```

## Supported Measurement Units

The system supports multiple measurement units and converts them into kilogram equivalents for consistent yield calculations.

| Measurement Unit | Conversion         |
| ---------------- | ------------------ |
| Tonne            | 1 tonne = 1,000 kg |
| Kilogram         | 1 kg = 1 kg        |
| Gram             | 1 g = 0.001 kg     |
| Bag              | 1 bag = 50 kg      |
| Crate            | 1 crate = 20 kg    |

Bag and crate conversions use predefined values within the application.

## User Roles

### Farmer

Farmers can:

* Manage their farms and associated fields.
* Register crops and track crop growth.
* Create, view, edit, and delete their harvest records.
* Access personal dashboard statistics and visual charts.
* Generate yield reports and export harvest data.
* Manage personal profile details and application preferences.

### Administrator

Administrators can:

* Access the functionality available to farmers.
* View agricultural records across the system.
* Manage farm ownership.
* Create and update user accounts.
* Assign user roles and manage account access.
* Delete user accounts, subject to application restrictions.

## How the Application Works

1. Users authenticate and access the application according to their assigned roles.
2. Farmers create farms and organize their fields.
3. Crops are registered with planting information and expected harvest dates.
4. Harvest records are created with quantities, measurement units, dates, and quality information.
5. The backend validates incoming data and stores records in the database.
6. Harvest quantities are converted into kilogram equivalents for standardized analysis.
7. Dashboard statistics and interactive charts summarize agricultural performance.
8. Users generate filtered reports and export harvest records as CSV files.

## Getting Started

Follow these steps to run the project locally.

### Prerequisites

Ensure the following are installed on your system:

* Python
* pip package manager
* Git
* A modern web browser
* A code editor such as Visual Studio Code

### Installation

**Step 1: Clone the repository**

```bash
git clone https://github.com/SRI-VIGNESH-WORKS/Crop-Harvest-Record-Management-System.git
```

**Step 2: Navigate to the project directory**

```bash
cd Crop-Harvest-Record-Management-System
```

**Step 3: Create a virtual environment**

```bash
python -m venv venv
```

**Step 4: Activate the virtual environment**

For Windows:

```bash
venv\Scripts\activate
```

For macOS or Linux:

```bash
source venv/bin/activate
```

**Step 5: Install dependencies**

If the repository contains a `requirements.txt` file, install the required packages using:

```bash
pip install -r requirements.txt
```

**Step 6: Configure environment variables**

Create a `.env` file if required by the application and configure the necessary environment variables.

Keep secret keys, passwords, and other sensitive credentials out of version control.

**Step 7: Start the application**

If `app.py` is the Flask application entry point, run:

```bash
python app.py
```

Open the local address displayed by the application in your browser. The documented development configuration uses port `5000`.

The exact setup procedure depends on the files and configuration included in the repository.

## Testing

The project uses Pytest for automated testing.

Run the test suite with:

```bash
pytest
```

The documented testing scope includes API functionality, authentication, data isolation, and data exports.

## Security Considerations

The application incorporates several security measures:

* Password hashing using Werkzeug.
* HTTP-only session cookies.
* Role-based access control.
* Parameterized SQL queries.
* User-scoped data access.
* Database foreign key constraints.
* Automated database timestamp updates.

For production use, the application should also be configured with appropriate environment variables, secure session settings, and reliable persistent database storage.

## Benefits

* **Digitized Recordkeeping:** Replaces fragmented paper-based records with a centralized agricultural management system.
* **Improved Data Consistency:** Standardizes harvest measurements for accurate yield calculations.
* **Efficient Harvest Logging:** Simplifies data entry through automatic farm and field population.
* **Better Visibility:** Provides crop lifecycle tracking and centralized dashboard statistics.
* **Data-Driven Decisions:** Helps users analyze harvest performance across crops, farms, and fields.
* **Simplified Reporting:** Supports filtered reports, CSV exports, and print-friendly records.
* **Role-Based Management:** Separates farmer access from administrative capabilities.

## Future Enhancements

Potential improvements include:

* Integration with a production-grade persistent database.
* Email-based password recovery.
* Advanced agricultural analytics and forecasting.
* Weather information and crop planning integration.
* Enhanced mobile responsiveness.
* Additional reporting formats.
* Expanded automated testing and deployment workflows.

## Author

**SRI VIGNESH**

GitHub Profile: https://github.com/SRI-VIGNESH-WORKS

## Live Application

Explore the deployed project:

https://crop-harvest-project.vercel.app/

## Repository

Explore the source code:

https://github.com/SRI-VIGNESH-WORKS/Crop-Harvest-Record-Management-System
