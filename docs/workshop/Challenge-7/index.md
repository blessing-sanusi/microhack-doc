# Evaluation

## Content Safety Evaluation

This notebook demonstrates how to evaluate content safety using Azure AI's evaluation tools. It includes steps to:
- Simulate content safety and grounded scenarios.
- Evaluate content for safety metrics such as violence, sexual content, hate/unfairness, and self-harm.
- Generate evaluation reports in JSON format.

### Prerequisites
- Azure AI project credentials.
- [Python 3.9+](https://www.python.org/downloads/)
- Python environment with required libraries installed (`azure-ai-evaluation`, `pandas`, etc.).
- Access to the Azure API endpoint.

Follow the steps below to set up your virtual environment and run the notebook. 
1. Navigate to the `Challenge-7` folder in your local repository. 
2. In the terminal run the following commands 

* Create a virtual environment
```shell
python -m venv venv
```
* Activate the virtual environment
```shell
.venv\Scripts\activate
```
* Install the requirements
```shell
pip install -r requirements.txt
```
3. Open the [Content_safety_evaluation notebook](./Content_safety_evaluation.ipynb) and follow the steps to perform content safety evaluations and generate detailed reports.

