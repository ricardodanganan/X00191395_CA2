# X00191395_CA2 - DevOps CA2 To-Do List

## Overview
This is a simple to-do list application developed as part of the DevOps CA2 assignment. The application allows users to add tasks, view tasks, mark them as complete or incomplete, and delete them. The project includes a CI/CD pipeline implemented with Azure DevOps.

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

2. **Navigate to the project directory:**
   ```bash
   cd <project-directory>

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt

4. **Run the application:**
   ```bash
   python todo.py

## CI Pipeline
- The CI pipeline uses Azure DevOps with:
- Build Agent: Ubuntu image (ubuntu-latest)
- Install Dependencies: From requirements.txt
- Run Unit Tests: Using Python’s unittest module
Pipeline is defined in azure-pipelines.yml and runs on commits to the main branch.

## Branch Management
Two branches were used: main and development. Changes were tested in development and merged into main after review via pull requests. Branch protection ensured review before merging to main.

## Testing Strategy
Unit tests were written in test_todo.py to cover:
- Adding tasks
- Marking tasks complete/incomplete
- Deleting tasks
Unit tests are automatically run as part of the CI pipeline.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
Created by [Ricardo Danganan Jnr] - feel free to contact me at x00191395@mytudublin.ie for questions or suggestions.


