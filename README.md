# BetFullX

## API Consumption and BigQuery Integration

This project is responsible for consuming data from an API and integrating it with Google BigQuery. It includes functionalities for data extraction, processing, and incremental loading, using Python and libraries such as `requests`, `pandas`, and `google-cloud-bigquery`.

## System Requirements

- Python 3.8+
- Google Cloud Platform (GCP) account
- `google-cloud-bigquery` library
- `requests` library
- `pandas` library
- `python-dotenv` library
- GCP JSON key file for authentication

## Setup

1. **Clone the repository**:

   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```

2. **Install dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

3. **Configure environment variables**:  
   Create a `.env` file in the root directory with the following variables:

   ```env
   API_KEY=<your-api-key>
   API_URL=<api-url>
   PROJECT_ID=<gcp-project-id>
   DATASET_NAME=<dataset-name>
   FULL_LOAD_DATE=2023-01-01
   LEAGUE=<league-id>
   SEASON=<season>
   ```

4. **Set up the GCP service key**:  
   Place the JSON key file in the `key/` directory and adjust the path in the code:
   ```python
   key_path = "./key/your-service-key-file.json"
   ```

## Project Structure

- **`main.py`**: Main file for executing the project.
- **`requirements.txt`**: Project dependencies list.
- **`key/`**: Directory for the GCP JSON key file.
- **`.env`**: File for environment variables.

## Key Features

### 1. API Consumption

- Data is extracted from configured endpoints, including:
  - Past fixtures (`past_fixtures`)
  - Future fixtures (`future_fixtures`)
  - Player data (`players`)

### 2. Data Processing

- Uses `pandas` for normalizing and processing JSON data.
- Supports nested fields and repeated entries.

### 3. BigQuery Integration

- Checks for the existence of datasets and tables before loading.
- Supports different write modes:
  - `WRITE_APPEND`
  - `WRITE_TRUNCATE`

### 4. Incremental Loading

- Updates based on the last recorded load date.
- Logs updates in BigQuery.

## Execution

To run the project, use the following command:

```bash
python main.py
```

## 🙂 Feedback

If you have any feedback, please send it to me at ricardodev10@yahoo.com

## 💛 Author

<img align="left" src="https://www.github.com/ricardodev10.png?size=115">

### Made with ♥ by [Ricardo Junior](https://www.linkedin.com/in/ricardodev10/) :wave:

Learning is continuous and there will always be a next level.

<a href="https://www.linkedin.com/in/ricardodev10" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge" height="25"></a>&nbsp;<a href="mailto:ricardodev10@yahoo.com" target="_blank"><img src="https://img.shields.io/badge/Email-FFFFFF?style=for-the-badge&logo=yahoo&logoColor=red" alt="Yahoo Badge" height="25"></a>&nbsp;<a href="https://api.whatsapp.com/send/?phone=%2B5531986161040&text&app_absent=0"><img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="Discord Badge" height="25"></a>&nbsp;<a href="https://www.github.com/ricardodev10" target="_blank"><img src="https://img.shields.io/badge/github-171717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Badge" height="25"></a>&nbsp;

<br clear="left"/>

<a href='#top'>

:arrow_up: Back to top

</a>
