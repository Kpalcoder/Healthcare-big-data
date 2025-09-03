

<p align="center">
  <img src="https://www.ctpop.org/sites/ctpop/files/2021-07/CT-200x200-logo.png" />

</p>

## Data Extraction from ClinicalTrials.gov

This project provides a streamlined interface to extract and interact with the vast repository of clinical trial data from ClinicalTrials.gov, a service of the U.S. National Institutes of Health.[[1](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQFCGZpk47cF73bNDyaEXuKiJ-IpmJEgR3szCIcy_2a3CM7bFZlGAJV9YE5dqfBag4vCrzMWl4amXkaTiMR480m_b17cszQ7s49JKRqHZOOXjhyxuLyKHPjS26F4QsxmUpSmIxLA-1NED6AzTw%3D%3D)]

Harnessing the power of the official open-source API, this tool is designed for researchers, data scientists, and anyone interested in the landscape of clinical studies worldwide.

---

### 🎯 About The Project

ClinicalTrials.gov is a database of privately and publicly funded clinical studies conducted around the world.[[1](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQFCGZpk47cF73bNDyaEXuKiJ-IpmJEgR3szCIcy_2a3CM7bFZlGAJV9YE5dqfBag4vCrzMWl4amXkaTiMR480m_b17cszQ7s49JKRqHZOOXjhyxuLyKHPjS26F4QsxmUpSmIxLA-1NED6AzTw%3D%3D)] This project simplifies the process of programmatically accessing this data. Whether you're conducting a meta-analysis, tracking the progress of trials in a specific therapeutic area, or building applications that leverage clinical trial information, this tool is for you.

A new version of the ClinicalTrials.gov API (v2.0) has been released, offering a more modern and standardized way to access the data.[[2](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEyalRYkQQ9CCTOEuHkzsvrUOmCVw9SzSEJRYAlvYXZs38KCxr6wsKQLJ4hsspG-bthXO8rGPTm0xr7GSGabybGV8SgLH-Jq1IMsztj8qqitJpVGQhZeNXDQ6ruJjC7qdNfJll5JmHp5w1A8vmN7FyYMgyV9A0aV9bpOFqUwcDQ673E)] This project is built to utilize the latest features of this new API.

### ✨ Key Features

*   **Simple & Intuitive**: Easy-to-use functions to search and retrieve clinical trial data.
*   **Structured Data**: Fetches data in a clean and organized format (primarily JSON).[[2](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEyalRYkQQ9CCTOEuHkzsvrUOmCVw9SzSEJRYAlvYXZs38KCxr6wsKQLJ4hsspG-bthXO8rGPTm0xr7GSGabybGV8SgLH-Jq1IMsztj8qqitJpVGQhZeNXDQ6ruJjC7qdNfJll5JmHp5w1A8vmN7FyYMgyV9A0aV9bpOFqUwcDQ673E)]
*   **Customizable Queries**: Flexibility to search for trials based on various criteria such as condition, intervention, location, and more.
*   **Up-to-Date Information**: Access to data that is refreshed daily on weekdays.[[3](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQFrsHT6B3dqkrsVWfmiePn_36hDHkZIKnqHDxsMAUn0CS0Y21Vm-qiX0KaCASp_PX91tLMBmxEMIh1NGSt969vm372q4_e7ztUFqZTNCY3gUMD8m3em37hy)]

### 🚀 Getting Started

To get a local copy up and running, follow these simple steps.

#### Prerequisites

Ensure you have Python 3.x installed on your system.

#### Installation

1.  Clone the repo
    ```sh
    git clone https://github.com/your_username/your_project_name.git
    ```
2.  Install required packages
    ```sh
    pip install -r requirements.txt
    ```

### ⚙️ Usage

Here’s a basic example of how you can use this tool to find clinical trials related to Diabetes:

```python
from clinical_trials_extractor import ClinicalTrials

# Initialize the client
ct = ClinicalTrials()

# Search for studies with the condition "Diabetes"
diabetes_studies = ct.search(query="Diabetes", max_studies=50)

# Print the NCT ID and brief title of each study
for study in diabetes_studies:
    nct_id = study['protocolSection']['identificationModule'].get('nctId', 'N/A')
    brief_title = study['protocolSection']['identificationModule'].get('briefTitle', 'N/A')
    print(f"{nct_id}: {brief_title}")

```

For more advanced queries and data fields, please refer to the [official API documentation](https://clinicaltrials.gov/api/v2/guides/getting-started).

### 📊 Data

The data extracted through this tool comes directly from the ClinicalTrials.gov database. The data structure is based on the JSON format provided by the API and includes a wide range of information for each study, such as:

*   Study identifiers (NCT ID)
*   Study status (recruiting, completed, etc.)
*   Conditions and interventions
*   Eligibility criteria
*   Locations and contact information
*   Study results (if available)

### 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

### 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

### 🙏 Acknowledgments

*   **ClinicalTrials.gov** for providing the comprehensive and open API.
*   The **U.S. National Library of Medicine (NLM)** for maintaining this invaluable resource.
