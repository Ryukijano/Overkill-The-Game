# Overkill-The Game
_*The next-gen, text-based open world thriller.*_

![Overkill: We don't know what's too much](https://github.com/BoltonB07/Overkill-The-Game/blob/master/OK%20Logo%202.jpg)
                                                                                          * working title

**COMING SOON!**

>Powered by Overkill Engine. 

_*For more insights on the Overkill Engine, check out @BoltonB07/Overkill_Engine*_

## GitHub Actions Workflow Setup

To set up GitHub Actions for this project, follow these steps:

1. Create a new directory named `.github/workflows` in the root of your repository.
2. Create a new file named `main.yml` inside the `.github/workflows` directory.
3. Add the following content to the `main.yml` file:

```yaml
name: Java CI

on: [push, pull_request]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - name: Checkout repository
      uses: actions/checkout@v2

    - name: Set up JDK 11
      uses: actions/setup-java@v2
      with:
        java-version: '11'

    - name: Build with Gradle
      run: ./gradlew build

    - name: Run tests
      run: ./gradlew test
```

4. Ensure that your project has a `build.gradle` file in the root directory to define the build and test tasks.
5. Commit and push the changes to your repository. This will trigger the GitHub Actions workflow to run the game and execute the tests.
