# Stackmix.io
Stackmix is a pastebin for your technology stack. Build out applications, share dependencies, demonstrate what goes into your pipeline, and more!

This is the foundation for the website Stackmix.io. It consists of a React frontend and Python Flask backend. Supported databases will be MySQL/MariaDB.

This is a self-hosted application that you can run on your own server via Docker or Docker Compose. 

Planned features:
- Automatic searching of Docker, pip, npm, wordpress plugins, etc to pull descriptions and references to github. Types: Application / Library / Module or Plugin
- Visual display of the technology stack to show what all goes into a software development project
- User accounts to be able to go back and edit a stack
- Public, Unlisted, and Private stacks
- Application templates for mobile, web, pipelines, steim, and more.
- voting on a stack: useful/not useful
- stack hashing to generate a unique hash based on what is in a stack. Works in multiple parts to identify based on software name and major versions.
- ability to parse a github and pull in subdependencies from package / requirements files.
- Convert a Dockerfile into a stack
- Convert docker-compose into a stack
- Choose stack depth, where docker would be level 1, python or nodejs applications 2, the dependencies 3, further dependencies 4, etc.. All the way down to c/c++ libraries and apt repositories. The max stack depth of the self-hosted application will be 2-3, starting from 1 which is a template. 
- Versioning of a stack, allowing edits
- Ability to nest a stack within another stack snapped im via a template (stack must use a template)

This project is intended to capture data on what projects are often used together, for instance:
- x% of uses of jQuery also used jQuery UI
- React is most commonly used with Y database backend

It is also intended to be able to use machine learning to identify components of a stack, such as databases, and their purpose, based on descriptions and inclusion. This is to help identify trends in the industry. For example, the template for a pipeline may include a preprocessor for images that didn't exist prior. This slight alteration in a common stack will allow product recommendations. When designing a stack allowing you to look into libraries and packages further. For example, when using mysql, redis may be recommended to cache queries.

It is also intended to note applications which are commonly not used together, due to overlapping functionality or for whatever reason. For example: mysql and postgresql

Package update timelines is also something of interest

I would like to be able to scale this out to be able to generate missing dependencies for an operating system

Example templates:

- Docker file - conaists of a docker container and any packages used withim the docker file. Excluding wget, so apt, pip, npm
- High level mobile application - consists of a frontend template and a backend template
- Frontend template - consists of GUI packages, plugins, and libraries
- Backend template - Consists of edge, file server, database, cache database, etc.. 
