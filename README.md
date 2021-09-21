# CodeSee Maps Documentation
This is the documentation website repo for CodeSee, a tool to help you visually understand your codebase.

CodeSee's goal is to help you understand complex codebases quickly and share that understanding with your teammates easily.

## Documentation quickstart
This section shows you how to build the docs locally. This allows you to preview them while editing.

You need Python 3 installed on your machine (these instructions were tested with 3.9)

Clone the repo:
`git clone https://github.com/Codesee-io/docs.git codesee-docs`

Navigate into codesee-doc, and create a virtual environment:
`python -m venv venv`

If you name your virtual environment something other than `venv` or `env`, add it to the .gitignore.

Activate your virtual environment: run the appropriate script for your system from /venv/Scripts/.

### Install requirements:
`pip install -r` requirements.txt
You can now preview the docs locally with mkdocs serve, or build them with mkdocs build.

## Getting help
If you need support with CodeSee, please contact support@codesee.io.
