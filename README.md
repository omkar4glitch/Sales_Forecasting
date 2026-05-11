QSR Sales Forecasting using Prophet
A Python-based sales forecasting pipeline for QSR (Quick Service Restaurant) businesses using Prophet and pandas.
This project forecasts future daily sales for multiple stores using historical sales data from Excel files.
________________________________________
Features
•	Upload Excel sales data
•	Forecast sales for multiple stores automatically
•	Daily sales forecasting using Prophet
•	Weekly seasonality support
•	US holiday effects included
•	Export forecast results to Excel
•	Runs easily in Google Colab
________________________________________
Technologies Used
•	Python
•	Prophet
•	Pandas
•	Google Colab
________________________________________
Forecasting Capabilities
The forecasting model currently includes:
•	Weekly seasonality
•	Yearly seasonality
•	US holiday calendar support
This makes the model suitable for:
•	QSR businesses
•	Retail forecasting
•	Multi-store sales prediction
•	Restaurant demand forecasting
________________________________________
Input File Format
The input Excel file should follow this structure:
Date	Store_A	Store_B	Store_C
2024-01-01	120	95	200
2024-01-02	135	110	210
Requirements
•	First column must be named Date
•	Store names should be separate columns
•	Data should contain daily sales values
•	Missing values should be minimized
________________________________________
Installation
Install required libraries:
pip install pandas prophet openpyxl
________________________________________
Running the Script
Run the script inside Google Colab or locally.
Google Colab
Upload the Excel file when prompted.
from google.colab import files
uploaded = files.upload()
________________________________________
Forecast Configuration
Current forecast settings:
forecast_start = "2026-05-04"
forecast_end = "2026-05-10"
Modify these dates as needed.
________________________________________
Model Configuration
Current Prophet model configuration:
model = Prophet(
    weekly_seasonality=True,
    yearly_seasonality=True
)

model.add_country_holidays(country_name='US')
________________________________________
Output
The script generates:
Prophet_Forecast_Wide.xlsx
Example output:
Date	Store_A	Store_B
2026-05-04	145	210
2026-05-05	150	225
________________________________________
How It Works
Upload Excel File
        ↓
Load Historical Sales Data
        ↓
Convert Data into Long Format
        ↓
Train Prophet Model Per Store
        ↓
Generate Future Forecast
        ↓
Combine Forecasts
        ↓
Export Forecast Excel File
________________________________________
Seasonality Used
Weekly Seasonality
Captures:
•	Weekend spikes
•	Weekday behavior
•	QSR traffic patterns
Yearly Seasonality
Captures:
•	Holiday demand
•	Annual sales cycles
•	Seasonal restaurant behavior
US Holidays
Includes:
•	Thanksgiving
•	Christmas
•	New Year
•	Independence Day
•	Labor Day
•	Other US federal holidays
________________________________________
Example Use Cases
•	QSR sales forecasting
•	Restaurant demand prediction
•	Store-level forecasting
•	Franchise analytics
•	Retail demand planning
________________________________________
Future Improvements
Potential enhancements:
•	Weather regressors
•	Promotion/event regressors
•	Super Bowl event forecasting
•	Monthly seasonality
•	Hyperparameter tuning
•	Automated retraining
•	Visualization dashboards
________________________________________
Example Forecast Workflow
Historical Daily Sales
          ↓
Prophet Learns:
- Trend
- Weekly Patterns
- Yearly Patterns
- Holiday Effects
          ↓
Future Sales Forecast
 
