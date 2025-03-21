## SysAid DevOps Assessment

This is a Flask application that returns `"Hello world!"` when accessed in a browser. 

---

## Steps Taken

1. Created a basic Python Flask app in a file called `app.py`.
2. Created a `requirements.txt` file to define the needed Python dependencies.
3. Installed Flask locally to verify the app worked before Dockerizing it.
4. Wrote a `Dockerfile` that:
   - Uses `python:3.12-slim` as a base image.
   - Sets a working directory.
   - Installs dependencies via `requirements.txt`.
   - Copies the application files.
   - Exposes port 5000.
   - Runs the app using `python app.py`.
5. Built the Docker image using the `docker build` command.
6. Ran the image using the `docker run` command with port mapping.
7. Tested that the app worked by opening `http://localhost:5000` in a browser.
8. Documented the project in this README file.
9. Uploaded the project to GitHub and committed all changes.

## Challenges:
- Originally named the file flask-app.py, but Python had trouble with the dash (-). I renamed it to app.py.
- I named it requierments.txt by accident, which caused pip to fail. I corrected the spelling.
- Forgot to add -d when running the Docker container, so the terminal locked up. Adding -d solved it.

---

## How to Build the Docker Image

Open a terminal in the project directory and run:

```bash
docker build -t sysaid-flask-app .
