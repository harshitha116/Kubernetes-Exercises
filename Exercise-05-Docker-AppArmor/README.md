# Exercise 5: Docker Security with AppArmor

## Objective
To run a Flask application inside a Docker container and explore AppArmor security profiles.

## Files
- `app.py` — Flask application.
- `Dockerfile` — Docker image configuration.
- `my-apparmor-profile` — Custom AppArmor profile.

## Steps Performed
1. Created the Flask application.
2. Built the Docker image using `docker build -t flask-apparmor .`
3. Started the container with port mapping `5002:5000`.
4. Accessed the Flask application at `http://localhost:5002`.
5. Loaded the custom AppArmor profile in Ubuntu WSL.
6. Checked the Docker container's security configuration.

## Result
The Flask application ran successfully inside the Docker container.

The custom AppArmor profile was loaded in Ubuntu WSL. However, the container process reported `unconfined`, so enforcement of the custom profile inside the container could not be verified in the current Docker Desktop and WSL2 environment.

## Conclusion
The Flask application and Docker setup were completed. Container-level AppArmor enforcement requires further verification in a compatible Linux Docker environment.