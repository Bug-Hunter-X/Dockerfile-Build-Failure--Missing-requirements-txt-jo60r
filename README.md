This repository demonstrates a common error in Dockerfiles: forgetting to include a `requirements.txt` file when using `pip` to install dependencies.  The original `Dockerfile` attempts to install dependencies from a missing `requirements.txt`. The `Dockerfile_fixed` demonstrates the correct way to include the requirements file and build the image.

**Steps to Reproduce:**
1. Clone this repository.
2. Attempt to build the original `Dockerfile` using `docker build -t my-app .`
3. Observe the build failure.
4. Build the corrected `Dockerfile_fixed` using `docker build -t my-app-fixed .`
5. The corrected Dockerfile should build successfully.