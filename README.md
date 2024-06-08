# Github-Actions
This repository demonstrates the integration of GitHub Actions with a simple Java project.
## Getting Started

### Prerequisites

- Java 8 or higher
- Maven

### Running Locally

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```

2. Build the project:
    ```bash
    mvn clean package
    ```

3. Run the tests:
    ```bash
    mvn test
    ```

## GitHub Actions Workflow

The GitHub Actions workflow is defined in `.github/workflows/java-ci.yml`. This workflow is triggered on every push and pull request to the `main` branch.

### Workflow Steps

1. **Checkout repository**: Uses the `actions/checkout@v2` action to check out the code from the repository.
2. **Set up JDK 11**: Uses the `actions/setup-java@v2` action to set up Java 11.
3. **Build with Maven**: Runs the `mvn -B package --file pom.xml` command to build the project.
4. **Run tests**: Runs the `mvn test` command to execute the tests.
