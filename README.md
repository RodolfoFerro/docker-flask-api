# Docker Flask API template 🐳

<!-- Shields -->
![Top language](https://img.shields.io/github/languages/top/RodolfoFerro/docker-flask-api?style=for-the-badge)
![Code size](https://img.shields.io/github/languages/code-size/RodolfoFerro/docker-flask-api?style=for-the-badge)
[![Last commit](https://img.shields.io/github/last-commit/RodolfoFerro/docker-flask-api?style=for-the-badge)](https://github.com/RodolfoFerro/docker-flask-api/commits/master)
[![License](https://img.shields.io/github/license/RodolfoFerro/docker-flask-api?style=for-the-badge)](https://github.com/RodolfoFerro/docker-flask-api/blob/master/LICENSE)
[![Twitter follow](https://img.shields.io/twitter/follow/rodo_ferro?style=for-the-badge)](https://twitter.com/rodo_ferro/)

<!-- Project description -->
This repository aims to be an easy to extend template for building a Python API using Flask and running it with only Python or using Docker.


## Prerequisities

Before you begin, ensure you have met the following requirements:

#### For only-Docker usage:
* You have a _Windows/Linux/Mac_ machine with the latest version of [Docker](https://www.docker.com/) installed.

#### For only-Python usage:
* You have a _Windows/Linux/Mac_ machine running [Python 3.6+](https://www.python.org/).
* You have installed the latest versions of [`pip`](https://pip.pypa.io/en/stable/installing/) and [`virtualenv`](https://virtualenv.pypa.io/en/stable/installation/) or `conda` ([Anaconda](https://www.anaconda.com/distribution/)).

For general purposes, why not installing prerequisites for both cases?


## Install/Run with only Python

If you want to install the dependencies and work locally using only Python, you can simply follow this steps. If you want to directly work using Docker, jump to the "[Install/Run with Docker](https://github.com/RodolfoFerro/docker-flask-api#installrun-with-docker)" section.

Clone the project repository:
```bash
git clone https://github.com/RodolfoFerro/docker-flask-api.git
cd docker-flask-api
```

To create and activate the virtual environment, follow these steps:

Using `conda`:
```bash
$ conda create -n docker-flask python=3.7

# Activate the virtual environment:
$ conda activate docker-flask

# To deactivate:
(docker-flask)$ conda deactivate
```

Using `virtualenv`:
```bash
# In this case I'm supposing that your latest python3 version is +3.6
$ virtualenv docker-flask --python=python3

# Activate the virtual environment:
$ source docker-flask/bin/activate

# To deactivate:
(docker-flask)$ deactivate
```

To install the requirements using `pip`, once the virtual environment is active:
```bash
(docker-flask)$ pip install -r requirements.txt
```

Finally, if you want to run the app locally, simply run:
```bash
$ python app.py
```

Now you should be able to test the API at <http://0.0.0.0:5000/>.

## Install/Run with Docker

If you want to install the dependencies and work using Docker, you can simply follow this steps. If you want to simply work locally using only Python, jump back to the "[Install/Run with only Python](https://github.com/RodolfoFerro/docker-flask-api#installrun-with-only-python)" section.

Clone the project repository:
```bash
git clone https://github.com/RodolfoFerro/docker-flask-api.git
cd docker-flask-api
```

To build the Docker image, simply run:

```bash
$ docker build -t docker-flask-api .
```

To run the Docker image, run the following:
```bash
$ docker run -it -p 5000:5000 -v $(pwd):/app  docker-flask-api
```

Now you should be able to test the API at <http://localhost:5000/>.

To stop the Docker container:
```bash
$ docker ps
$ docker stop <container-id>
```

## Contributing

To contribute to <project_name>, follow these steps:

1. Fork this repository.
2. Create a branch: `git checkout -b <feature_branch_name>`.
3. Make your changes and commit them: `git commit -m '<commit_message>'`
4. Push to the original branch: `git push origin <project_name>/<location>`
5. Create a Pull Request.

Additionally you can see the GitHub documentation on [creating a Pull Request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request).


<!-- ## Contributors

Thanks to the following people who have contributed to this project:

* @RodolfoFerro 📖💻 -->


## Contact

If you want to contact me you can reach me at <rodolfoferroperez@gmail.com>. There, or through any other of my social profiles your can find at: <https://rodolfoferro.glitch.me/>


## License

This project uses an [MIT License](https://github.com/RodolfoFerro/docker-flask-api/blob/master/LICENSE).
