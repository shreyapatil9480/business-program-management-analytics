# Business Program Management Analysis

This project provides a complete, out‑of‑the‑box example of how a **business analyst**, **program manager** or **data analyst** can leverage data to uncover insights and build predictive models. It includes a synthetic dataset reflecting common patterns in project and program management, a Jupyter notebook with exploratory data analysis and machine learning models, a list of required Python dependencies, and clear instructions for getting started.

The repository is designed to be approachable for beginners while still containing enough complexity for more advanced users to demonstrate their skills. You are encouraged to extend the analyses, try different modelling approaches and customise the dataset generator to match your own interests or industry domain.

## Contents

| File | Description |
|---|---|
| **`business_program_management_dataset.csv`** | Synthetic dataset containing 1,000 projects with fields such as budget, schedule, risk, complexity, manager experience, scope changes, ROI, customer satisfaction and a success flag. |
| **`analysis.ipynb`** | Jupyter notebook that loads the dataset, performs exploratory data analysis (EDA), visualises distributions and relationships, builds classification models to predict project success, builds regression models to estimate return on investment (ROI), and discusses conclusions and next steps. |
| **`requirements.txt`** | List of Python packages required to run the notebook. |
| **`build_dataset_and_notebook.py`** | (Optional) Script used to generate the synthetic dataset and notebook programmatically. You do not need to run this script to use the project. |

## Dataset Overview

Each row in `business_program_management_dataset.csv` corresponds to a single project. The fields include:

| Column | Type | Description |
|---|---|---|
| `project_id` | string | Unique identifier for the project. |
| `start_date` / `end_date` | date | Planned start and end dates of the project. |
| `planned_duration` | integer | Planned duration (in days). |
| `planned_budget` / `actual_budget` | float | Budget amounts in dollars. |
| `budget_overrun_pct` | float | Percentage by which actual budget exceeds or falls below the plan. |
| `team_size` | integer | Number of team members assigned to the project. |
| `priority` | categorical | Project priority (`High`, `Medium`, `Low`). |
| `department` | categorical | Department responsible for the project (IT, Marketing, Finance, Operations, HR). |
| `program_type` | categorical | Type of program (e.g., New Product Launch, Process Improvement). |
| `risk_level` / `complexity` | float | Ratings on a 1–10 scale. |
| `manager_experience` | integer | Manager’s experience in years. |
| `scope_changes` | integer | Number of scope change requests. |
| `delayed_tasks` | integer | Number of tasks behind schedule. |
| `resource_utilization_pct` | float | Resource utilisation percentage (may exceed 100 if overloaded). |
| `schedule_overrun_pct` | float | Percentage by which the schedule is delayed or ahead of plan. |
| `success` | binary | Target variable indicating whether the project was successful (1) or not (0). |
| `ROI` | float | Return on investment. Positive values indicate profit; negative values indicate loss. |
| `customer_satisfaction` | float | Satisfaction rating on a 1–5 scale. |

These variables were generated using plausible relationships: high risk or complexity and significant overruns negatively affect success; experienced managers and high‑priority initiatives increase success; ROI and satisfaction depend on many of the same drivers.

## Using the Notebook

The notebook `analysis.ipynb` walks through the following steps:

1. **Load and inspect the data** – view the first few rows, data types and summary statistics.
2. **Perform exploratory data analysis (EDA)** – visualise distributions, compare successful vs unsuccessful projects, and explore correlations.
3. **Prepare data for modelling** – one‑hot encode categorical variables and separate features from targets.
4. **Classification modelling** – build logistic regression and random forest classifiers to predict `success` and evaluate them using accuracy, ROC AUC and confusion matrices.
5. **Regression modelling** – build linear regression and random forest regressors to predict `ROI` and evaluate them using RMSE and R².
6. **Conclude and suggest next steps** – reflect on the results and propose extensions such as hyperparameter tuning or feature importance analysis.

You can run the notebook step by step to follow along or jump directly to the modelling sections. All code is annotated and ready to run.

## Getting Started

To explore the project on your local machine:

1. **Clone the repository** (or download it as a ZIP and extract):

   ```bash
   git clone https://github.com/<your-username>/<your-repository>.git
   cd <your-repository>
   ```

2. **Create a Python environment** (optional but recommended) and activate it. For example, using `venv`:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install the required packages**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Launch JupyterLab or Jupyter Notebook** and open `analysis.ipynb`:

   ```bash
   jupyter notebook
   ```

5. **Run the notebook** cell by cell. Feel free to modify the analysis, add charts or models, and iterate on the findings.

## Contributing

Feel free to fork this repository and adapt it to your own needs. You might consider:

* Expanding the dataset generator with additional features or more nuanced relationships.
* Performing clustering or segmentation analyses to identify patterns among projects.
* Implementing hyperparameter tuning for the models using cross‑validation.
* Integrating time series analysis if you have data on progress over time.

Contributions and feedback are welcome!

## License

This project is provided under the MIT License. See the `LICENSE` file for details.