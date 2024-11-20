# X00191395_CA2 - DevOps CA2 To-Do List

## Table of Contents
1. [Overview](#overview)
2. [Technologies Used](#technologies-used)
3. [Local Development Setup](#local-development-setup)
4. [Application Features](#application-features)
5. [CI Pipeline Implementation](#ci-pipeline-implementation)
6. [Branch Policies and Protection](#branch-policies-and-protection)
7. [Testing Strategy](#testing-strategy)
8. [Troubleshooting Guide](#troubleshooting-guide)
9. [Azure DevOps Pipeline](#Azure DevOps Pipeline)
10. [License](#license)
11. [Contact](#contact)

## Overview
This is a simple to-do list application developed as part of the DevOps CA2 assignment. The application allows users to add tasks, view tasks, mark them as complete or incomplete, and delete them. The project includes a CI/CD pipeline implemented with Azure DevOps to automate testing and integration processes.

## Technologies Used
- Python
- Flask
- Azure DevOps
- Visual Studio Code

## Local Development Setup
Follow these steps to set up the project locally:

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   ```
   _Screenshot: Cloning the repository to Visual Studio Code_
   ![Figure 2: Cloning the repository in Visual Studio Code](https://github.com/ricardodanganan/X00191395_CA2/raw/main/images/figure2_clone_repository_vscode.png)


2. **Navigate to the project directory:**
   ```bash
   cd <project-directory>
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application:**
   ```bash
   python todo.py
   ```

## Application Features
- **Add Task**: Users can add new tasks to the list.
- **View Tasks**: Users can view all tasks along with their status (completed or incomplete).
- **Mark Task Complete/Incomplete**: Users can mark a task as complete or revert it back to incomplete.
- **Delete Task**: Users can delete tasks from the list.

_Screenshot: Expanded functionality of the to-do list_
![Figure 6: Expanded functionality of the to-do list application](https://github.com/ricardodanganan/X00191395_CA2/raw/main/images/figure6_todo_list_expanded_functionality.png)

## CI Pipeline Implementation
The CI pipeline is configured using Azure DevOps, with the following steps:
- **Build Agent**: Uses the `ubuntu-latest` image for the build.
- **Install Dependencies**: Installs dependencies from `requirements.txt`.
- **Run Unit Tests**: Runs unit tests using Python's unittest framework.

_Pipeline YAML Configuration Screenshot:_
![Figure 13: Updated azure-pipelines.yml configuration](https://github.com/ricardodanganan/X00191395_CA2/raw/main/images/figure13_updated_azure_pipeline_config.png)

## Branch Policies and Protection
Two branches were used: `main` and `development`. Changes were initially made in the `development` branch and then merged into the `main` branch through pull requests to ensure code quality and testing.
- **Branch Protection**: A policy was set up to require pull requests and review before merging into `main`.

- **Branch Merge**: Screenshot of merging `development` into `main`:
  ![Figure 16: Commit history merging `development` into `main`](https://github.com/ricardodanganan/X00191395_CA2/raw/main/images/figure16_commit_history_merge.png)

## Testing Strategy
Unit tests were written in `test_todo.py` to verify core functionalities, including:
- **Adding Tasks**
- **Marking Tasks Complete/Incomplete**
- **Deleting Tasks**

The unit tests are automatically executed as part of the CI pipeline to ensure no regressions.
![Figure 12: Terminal showing Git commands to add, commit, and push changes](https://github.com/ricardodanganan/X00191395_CA2/raw/main/images/figure12_git_add_commit_push.png)

**Screenshot of Running Tests:**

## Troubleshooting Guide
During the development of the CI pipeline, a problem with hosted parallelism was encountered. Below are the steps that were followed:
- Submitted a parallelism request to Azure DevOps support.
_Screenshot: Azure DevOps Parallelism Request Form_
![Figure 11: Azure DevOps Parallelism Request](https://github.com/ricardodanganan/X00191395_CA2/raw/main/images/figure11_azure_devops_parallelism_request.png)

- Once approved, the pipeline ran successfully.
 _Screenshot of Successful Pipeline:_
![Figure 14: Successful Azure Pipeline run](https://github.com/ricardodanganan/X00191395_CA2/raw/main/images/figure14_successful_pipeline_summary.png)

## Azure DevOps Pipeline
You can view the Azure DevOps CI/CD pipeline for this project [here](https://dev.azure.com/X00191395/X00191395_CA2).

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
Created by Ricardo Danganan Jnr - feel free to contact me at x00191395@mytudublin.ie for questions or suggestions.


