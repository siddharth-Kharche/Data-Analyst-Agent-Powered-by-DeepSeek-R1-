# Data Analyst Agent - Powered by DeepSeek-R1 LLM Model

## Overview
The **Data Analyst Agent** is a Streamlit-based application that combines the analytical power of **GroqChat** with the versatility of **DuckDbAgent**. This tool allows users to upload datasets in CSV or Excel format, analyze them using natural language queries, and generate SQL queries for data exploration. The app is designed for data analysts, providing an intuitive interface for data querying and visualization.

---

## Key Features
- **File Upload**: Supports CSV and Excel file uploads for data analysis.
- **Natural Language Querying**: Users can ask questions about their data in plain English.
- **SQL Query Generation**: Automatically generates SQL queries to address user queries.
- **GroqChat Integration**: Powered by the **deepseek-r1-distill-llama-70b** model for advanced conversational capabilities.
- **Interactive Data Table**: Displays uploaded datasets in an interactive table.
- **Streamlit UI**: Simple, user-friendly interface with sidebar API key configuration.

---

## Installation

### Prerequisites
Ensure you have Python 3.8 or higher installed.

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/data-analyst-agent.git
   cd data-analyst-agent
   ```

2. Install the required Python libraries:
   ```bash
   pip install phi streamlit pandas groq
   ```

3. Set up the Groq API key:
   - Open the app in Streamlit and enter your Groq API key in the sidebar.

---

## Usage

1. **Run the Application**:
   ```bash
   streamlit run app.py
   ```

2. **Interface**:
   - Upload a CSV or Excel file using the file uploader.
   - Enter your query about the uploaded data in plain English.
   - Click **Submit Query** to get the SQL query and the final result.

---

## Technical Details

### Key Components
- **GroqChat**: Provides conversational AI capabilities.
- **DuckDbAgent**: Generates SQL queries based on user input and executes them on the uploaded dataset.
- **PandasTools**: Enhances interaction with the dataset.

### Workflow
1. Users upload a dataset (CSV/Excel).
2. The app preprocesses the file and displays it in a table format.
3. Users submit a query about the data.
4. **DuckDbAgent** generates a corresponding SQL query and retrieves the result.
5. Results are displayed in the Streamlit interface.

### Example Query
- **User Input**: "What is the average sales amount for each region?"
- **Output**:
  - SQL query enclosed in ` ```sql ``` `.
  - Final answer presented as a table or summary.

---

## Screenshots
### Example Workflow
1. **File Upload**: Upload a sample dataset (e.g., sales.csv).
2. **Query Input**: "Show total sales by month."
3. **Generated SQL**: 
   ```sql
   SELECT MONTH(sale_date), SUM(sales_amount) AS total_sales
   FROM uploaded_data
   GROUP BY MONTH(sale_date)
   ORDER BY MONTH(sale_date);
   ```
4. **Result**: A table showing monthly sales totals.

---

## Notes
- Ensure the uploaded dataset is clean and well-formatted.
- For large datasets, consider optimizing preprocessing steps for faster queries.
- All session data, including uploaded files and generated queries, is stored temporarily for the session duration.

---

## Future Enhancements
- Add support for additional file formats (e.g., JSON, Parquet).
- Enable multi-agent collaboration for advanced analytics.
- Include visualization tools for data insights (e.g., charts, graphs).

---

## License
This project is licensed under the **MIT License**.

---

## Contact
For queries or contributions, feel free to reach out:
- **Author**: Siddharth Kharche
- **Email**: siddukharche04@gmail.com
- **GitHub**: [siddharth-Kharche](https://github.com/siddharth-Kharche)
