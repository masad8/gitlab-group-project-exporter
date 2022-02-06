# gitlab-group-project-exporter

This project can be used to export GitLab groups and projects inside a main group. This repo can be used for regularly backing up content from the Gitlab.com server to private storage.

## Install

Download and install directly from PyPi using ```pip install gitlab-group-project-exporter``` or download the source from this git and install using ```sudo python3 setup.py install```.

## Usage

The main script to be run for exporting groups and projects is ```bin/main.py```. The parameters to be configured in this script are:

| Parameter | Explanation |
| :---: | :---: |
| MAIN_GROUP_ID | The ID of the main group. The main group, as well as, all the subgroups and projects inside this group will be backed up. |
| GITLAB_PRIVATE_KEY | GitLab private key/personal token with API access. Can be created after logging into your account at https://gitlab.com/-/profile/personal_access_tokens. |
| GITLAB_URL | The URL where GitLab instance is installed. For the GitLab main installation, it should be ```https://gitlab.com```. |
| EXPORT_TIME_GROUP | Maximum amount in seconds till a group export is awaited to be prepared. |
| EXPORT_TIMEOUT_PROJECT | Maximum amount in seconds till a project export is awaited to be prepared. |
| EXPORT_PATH_GROUP | The path where backup of the main group and all subgroups inside the main group will be exported. |
| EXPORT_PATH_PROJECT | The path where all projects inside the main group will be exported. |
