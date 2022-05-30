# Group-Project-Q1-2022

![GitHub issues](https://img.shields.io/github/issues-raw/After-Dark-Communications/Group-Project-Q1-2022)
![GitHub closed issues](https://img.shields.io/github/issues-closed-raw/After-Dark-Communications/Group-Project-Q1-2022)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![License: CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/80x15.png)](https://creativecommons.org/licenses/by-sa/4.0/)
***

[Todo list of things to do](https://github.com/orgs/After-Dark-Communications/projects/1/views/5)


---

### Submodules

most git desktop applications will automatically clone the submodules repositories when this repository is cloned.

If the submodule folders are empty (folders titled Q1-2022-...), open git in the repository folder and use the following command:
```bash
    git clone --recurse-submodules
```
this will clone the repositories where those submodules are from.

To update the submodules, making them up-to-date with the latest commits, use the following command:
```bash
    git submodule update --remote
```
This will get the latest commits on their respective branches

---

### How to Run
use "docker-compose up -d" to run the application in detached mode. This will run it within the docker environment and not output to the console.

#### How to add new container

- open the "docker-compose.yml" file
- under "services", add a new service in the following structure:
everything between <> will have to be replaced by the value of your choice
```
    <service name>:
      container_name: <container name>
      image: <image tag>
      ports:
      - "<external port to listen to>:<internal exposed port>"
```
the container name has to abide by the docker rules (no spaces and only ascii)

#### How to add container information

- open the "docker-compose.override.yml" file
- under services add the service in the following structure:
```
    <service name>:
      *enivronment:
        - <environment variable>
      *volumes:
        - <volume directory>
```
the *names are examples, they are not mandatory to add
