# Job-Postings-Analysis-Using-Python
This project analyzes job postings data to identify the demand for various programming languages and technologies.  
The notebook processes a dataset containing job details and extracts insights such as the number of job postings for each skill.

## 📌 Objectives
- Load and explore a job posting dataset.
- Analyze the *Key Skills* column to find how many jobs require each technology.
- Use a custom function to count job postings per technology.
- Export results to an Excel file.
- Upload the completed Jupyter Notebook to GitHub.

## 📂 Files Included
- *Job_Postings_Analysis.ipynb* – Main notebook containing all code, outputs, and analysis.  

## 🧠 Key Function Used
The main function used to count job postings for each technology:

```python
def get_number_of_jobs_T(technology):
    number_of_jobs = df[df['Key Skills'].str.contains(technology, case=False, na=False)].shape[0]
    return technology, number_of_jobs
