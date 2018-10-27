# pipenv-dockerfiles

This image includes Python 3.6 with pipenv.

Pipenv will automatically install the dependencies on build.
The Pipfile and Pipfile.lock have to be in the same directory as the docker file.


## Example

    FROM dr1s/pipenv-alpine:3.8-python3.6

    COPY main.py /app

    EXPOSE 9311

    ENTRYPOINT python3 main.py
