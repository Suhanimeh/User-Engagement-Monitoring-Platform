# GA4 User Engagement Analytics Dashboard

**Exploring User Behavior Through Google Analytics 4 Data**

## Overview

The GA4 User Engagement Analytics Dashboard is a data analytics project designed to explore and visualize website engagement metrics from Google Analytics 4 (GA4) data.

The application transforms structured analytics data into key performance indicators (KPIs), charts, and summary tables. It helps users examine event activity, compare engagement metrics, and explore changes in website interactions over time.

Built with Python and Streamlit, the dashboard brings data processing and interactive visualization together in one interface. It also includes CSV export functionality for further analysis using tools such as Excel, Python, or Power BI.

The project demonstrates practical skills in data analysis, exploratory data analysis (EDA), data visualization, metric interpretation, dashboard development, and technical documentation.

## Live Demo

**(https://user-engagement-monitoring-platform-xshdgbhagkcnmtnqrzj8m3.streamlit.app/)**

## Project Objectives

The main objectives of this project are to:

- Analyze website engagement data exported from Google Analytics 4.
- Transform raw analytics data into meaningful metrics.
- Visualize event distributions and engagement trends.
- Explore relationships between user activity and engagement indicators.
- Present analytical results through an interactive dashboard.
- Enable users to export processed data for further investigation.
- Apply data analysis and visualization concepts to a practical project.
- Develop skills in application deployment, documentation, and project organization.

## Key Features

### 1. KPI Dashboard

Provides a summary of website activity through key metrics, depending on the available dataset and implementation.

- Total users
- Total event count
- Engagement rate
- Most frequently recorded events

These indicators provide an overview of user activity and help identify areas for further investigation.

### 2. Time-Series Analytics

Visualizes engagement trends over a 30-day period, where date-level data is available.

Time-series analysis helps users explore changes in recorded activity, identify potential patterns, and compare engagement across the reporting period.

### 3. Event Distribution Analysis

Displays the distribution of recorded events to show which interactions account for a larger proportion of website activity.

For example, page views and scroll events can be compared to explore how users interact with website content.

### 4. User Activity Analysis

Examines event frequency relative to active users using the metrics available in the dataset.

This helps distinguish overall event volume from user-normalized activity. However, event frequency alone does not explain the reasons behind user behavior.

### 5. Engagement Scatter Plot

Visualizes selected user reach and engagement measures to help explore possible relationships, clusters, and unusual observations.

These relationships are exploratory and should not be interpreted as proof of causation.

### 6. Data Insights Table

Presents processed analytics in a structured tabular format for easier inspection and comparison.

Where implemented, engagement scoring and sorting can help users examine differences between events and identify areas for further analysis.

### 7. CSV Export

Allows users to download processed analytics data for:

- Further analysis in Excel or Python.
- Preparing reports and summaries.
- Sharing data with collaborators.
- Importing compatible datasets into business intelligence tools.

### 8. Interactive Dashboard

Combines KPI summaries, charts, and tabular data in a single interface using Streamlit and the visualization tools implemented in the application.

## Dashboard Preview

The live application provides an interactive way to explore the dashboard's available analytics.

For a more informative GitHub presentation, screenshots can be added to the repository to demonstrate the dashboard overview, event distribution, and engagement trends.

Example Markdown for adding a screenshot:

```markdown
![Dashboard Overview](screenshots/dashboard-1.png)

![Engagement Analytics](screenshots/dashboard-2.png)

![Event Distribution](screenshots/dashboard-3.png)
```

Place the actual screenshots in the `screenshots/` directory and update the filenames if necessary.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Application logic and analytics processing |
| Streamlit | Interactive dashboard interface |
| Pandas | Data loading, transformation, aggregation, and analysis |
| NumPy | Numerical calculations and data operations |
| Matplotlib | Data visualization, where implemented |
| Seaborn | Statistical visualization, where implemented |
| Chart.js | Interactive charts, if integrated into the application |
| Tailwind CSS | Interface styling, if integrated into the application |
| JavaScript | Client-side interactions, where implemented |
| Git and GitHub | Version control and source code management |
| Streamlit Community Cloud | Application hosting |

*The technology list should reflect the actual implementation and dependencies in the repository. Remove optional technologies that are not used by the current application.*

## Project Architecture

The application follows a data-processing and visualization workflow.

```text
Google Analytics 4 Data
          |
          v
      CSV Input
          |
          v
    Data Processing
        Pandas
          |
          v
 Metric Calculation
   and Aggregation
          |
          v
 Interactive Dashboard
       Streamlit
          |
          v
  KPIs, Charts and Tables
          |
          v
      CSV Export
```

### Main Components

**Data Input**

Loads analytics records from a GA4 CSV export or another supported data source.

**Analytics Engine**

Processes the input data, performs aggregations, and calculates the metrics used by the dashboard.

**Visualization Layer**

Presents summary indicators, event distributions, engagement trends, and other analytical views.

**Export Functionality**

Makes processed data available for additional analysis and reporting outside the application.

Separating data processing from presentation logic, where implemented, helps improve maintainability and makes future enhancements easier to manage.

## Dataset and Data Processing

The dashboard is designed to work with structured Google Analytics 4 data.

An illustrative example of the expected CSV format is shown below.

| Event name | Event count | Total users | Event count per active user | Total revenue |
|---|---:|---:|---:|---:|
| scroll | 903 | 5 | 180.6 | 0 |
| page_view | 463 | 10 | 46.3 | 0 |

*These values are illustrative examples, not verified results from the live application.*

Depending on the input format, the data-processing workflow may include:

1. Loading CSV data into a Pandas DataFrame.
2. Checking required columns and data types.
3. Identifying missing or invalid values.
4. Aggregating event and user metrics.
5. Calculating summary indicators.
6. Preparing processed data for charts and tables.

The exact processing and validation steps depend on the implementation in the analytics engine.

### Understanding the Metrics

| Metric | Description |
|---|---|
| Event count | Number of times an event was recorded. |
| Total users | Number of users attributed to the relevant metric and reporting scope. |
| Event count per active user | Event frequency normalized by active users, as defined in the source data. |
| Engagement rate | GA4 engagement metric calculated using the relevant session data or an appropriately prepared export. |
| Total revenue | Revenue attributed to the selected reporting scope, when available. |

GA4 metrics have different definitions and aggregation rules. Event counts should not be treated as unique users, and high event volume alone does not establish strong engagement or successful website performance.

## Analytical Approach

The project uses descriptive analytics to summarize recorded interactions and explore engagement patterns.

### Activity Analysis

Examines frequently recorded events and compares their contribution to overall event volume.

### Trend Analysis

Uses time-based data to explore changes in activity over the selected reporting period.

### Engagement Comparison

Compares selected user and engagement measures to identify possible relationships and differences in activity.

These analyses help transform raw tracking data into more interpretable summaries. Further investigation is required to understand the causes and business significance of any identified patterns.

## Installation and Setup

### Prerequisites

Before running the application, ensure you have:

- Python 3.10 or a version compatible with the project dependencies.
- pip for installing Python packages.
- Git for cloning the repository.
- A compatible GA4 CSV export or the sample dataset provided with the project.

### 1. Clone the Repository

Replace the example repository URL with your actual GitHub repository URL.

```bash
git clone https://github.com/YOUR_USERNAME/ga4-dashboard.git
cd ga4-dashboard
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment on Windows:

```powershell
venv\Scripts\activate
```

On macOS or Linux:

```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Application

```bash
streamlit run app.py
```

Open the local URL displayed in your terminal. By default, Streamlit usually runs at:

`http://localhost:8501`

## Deployment

The application is available through Streamlit Community Cloud.

**Live application:** https://user-engagement-monitoring-platform-xshdgbhagkcnmtnqrzj8m3.streamlit.app/)

To deploy an updated version from GitHub:

1. Push the application code and `requirements.txt` to your repository.
2. Open [Streamlit Community Cloud](https://share.streamlit.io/).
3. Connect the GitHub repository.
4. Select the appropriate branch and `app.py` entry point.
5. Deploy the application.
6. Test the deployed dashboard and verify its data-processing and export functionality.

If the application requires external services or private credentials, configure them through the hosting platform's secrets management rather than committing them to GitHub.

## Data Export

The dashboard includes CSV export functionality for processed analytics data.

Exported files can be used for:

- Additional analysis in Excel or Python.
- Preparing reports and analytical summaries.
- Sharing relevant datasets with collaborators.
- Importing compatible data into Power BI or other business intelligence tools.

The exported fields depend on the application's implementation. A CSV export should not be assumed to contain every available GA4 dimension or metric.

## Limitations and Future Improvements

Potential improvements include:

- Integrating the official GA4 Data API for automated data retrieval.
- Adding date-range and event-category filters.
- Comparing new and returning users when the required data is available.
- Improving input validation and error handling.
- Adding automated tests for data transformations and metric calculations.
- Documenting metric definitions and aggregation assumptions.
- Providing downloadable analytical summaries.
- Exploring predictive analytics using appropriately prepared historical data.
- Improving accessibility and responsive layout behavior.

An official GA4 API integration would require suitable Google Cloud configuration, permissions, and authentication. It should be considered a future enhancement unless it is already implemented.

## Skills Demonstrated

This project demonstrates practical experience with:

- Python-based data analysis.
- Data cleaning and transformation using Pandas.
- Exploratory data analysis and metric interpretation.
- Data visualization and dashboard development.
- Interactive application development with Streamlit.
- Analytics workflow organization.
- Exporting processed datasets for further analysis.
- Application deployment using Streamlit Community Cloud.
- Technical documentation and project organization.


## Author

GitHub: @Suhanimeh



