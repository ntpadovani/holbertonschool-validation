# Awesome Inc. Website

This repository contains the source code for the Awesome Inc. website built using the GoHugo static site generator and the Ananke theme.

## Prerequisites

To work on this project, you need to have the following tools installed on your system:

1. [GoHugo](https://gohugo.io/getting-started/installing/) version 0.84.0
2. [GNU Make](https://www.gnu.org/software/make/) version 3.81 or 4.0

## Lifecycle

This project follows a simple development lifecycle with three main steps:

1. **Build**: Generate the website from the markdown and configuration files in the `dist/` directory.
2. **Clean**: Clean up the content of the `dist/` directory.
3. **Post**: Create a new blog post using environment variables `POST_TITLE` and `POST_NAME`.

To perform these steps, the project uses a Makefile with the following targets:

### Build

To build the website, run:

make build


This command will generate the website in the `module1_task0/dist/` directory.

### Clean

To clean up the `dist/` directory, run:

make clean

This command will remove the contents of the `module1_task0/dist/` directory.

### Post

To create a new blog post, set the `POST_NAME` and `POST_TITLE` environment variables and run:

make post

This command will create a new blog post with the specified file name and title.

### Help

To display a list of available targets and their usage, run:

make help

This command will show the list of targets and their usage based on the comments in the Makefile.