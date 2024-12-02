Healthcare Data Analysis Project

    This project analyzes a healthcare dataset to gain insights into patient demographics, medical conditions, and associated billing data. The project includes data extraction, querying, and analysis using Groovy and MongoDB to explore trends such as cost distribution by condition, emergency admission rates, and hospital resource usage.

Project Structure
*/ src/: Contains source code for Groovy scripts and MongoDB queries.
*/ data/: Includes the original healthcare dataset in .xlsx format.
*/ README.md: Project overview and instructions.
*/ output/: Contains result files from data analysis, which can be used for further review and visualization.

Requirements
*/ Java: Version 8 or higher
*/ Groovy: Version 3.0
*/ MongoDB: Atlas or local installation for cloud-based queries
*/ Dependencies: MongoDB Java Driver (available in build.gradle)

Setup Instructions
*/ Install dependencies and set up MongoDB credentials if using MongoDB Atlas.
*/ Ensure you have MongoDB running locally or set up your cloud environment.
*/ Run the Groovy scripts from the src/ directory:

    groovy src/StandaloneQuery.groovy
    groovy src/CloudQueryMongoDB.groovy


Usage
Standalone Analysis
    To analyze the data locally (on your machine), run StandaloneQuery.groovy. This script filters and aggregates data based on conditions like admission type and medical conditions.
        
        groovy src/StandaloneQuery.groovy

Cloud Analysis with MongoDB
    To analyze the data using MongoDB in a cloud environment, run CloudQueryMongoDB.groovy. This script connects to MongoDB Atlas, and performs data retrieval, filtering, and aggregation similar to the standalone query.
        groovy src/CloudQueryMongoDB.groovy

Queries Implemented
    Selection: Retrieves all patient records.
    Projection: Selects relevant columns such as medical condition, admission type, and billing.
    Filtering: Filters records for emergency admissions or specific medical conditions (e.g., "Cancer").
    Grouping and Aggregation: Groups data by medical condition and calculates average billing, emergency admission rate, etc.

Results

Results from each query are stored in the output/ folder in CSV or JSON format, depending on the analysis. These files can be reviewed and further visualized.