# a-config-setup-django-3.1.2

This repo is geared towards team building across multiple stages of the SDLC. It is a starting point for building AqauTech's web interface for their technicians. See requirements.txt for modules that are being used in the project.

## todo-list.md

A readme for organizing the next set of prioritized steps.

## post-mordems.md

A positive means to document the learning process moving forward. 

## Recreate the project

Make sure we are using a conda environment with correct python version.

```zsh

python -m venv venv
pip install -r requirements.txt

```

### Adjust settings as necessary

Basic dev work will need to address settings_local.py and how we run the dev server with flags. Define staging and CI/CD promotion. Adjust directory structure as needed.

#### Further Reading

[Configuring Django Settings: Best Practices](https://djangostars.com/blog/configuring-django-settings-best-practices/)

