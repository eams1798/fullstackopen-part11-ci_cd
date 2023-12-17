I have an app that can automate the process for making quotes for an event hall.  This way, they can be delivered to customers more quickly.  It has the following stack:
 - Frontend: React + Typescript
 - Backend: Python + Flask
 - Database: MySQL

 The following are suitable tools to cover some Continuous Integration (CI) steps:
 - Linting: ESlint can be used for the frontend, powered by specific React and TS plugins.  Additionally, the tsconfig.json file can be configured to further restrict loose details when writing code.  For the backend, PyLint is recommended, which allows you to follow the best practices of the PEP8 convention.
 - Testing: For the frontend you can use Jest, fully supported by Javascript, and enhance it with the React Testing Library to validate the behavior of each component.  In the backend it is enough to use pytest, but if you are looking for something more specific, there is the pytest-flask module
 - Building: Webpack offers simple and common solutions for the entire JavaScript environment, including React, Typescript, Node, among others.  In the case of the backend, there are a whole series of tools that must be used together to build the application safely.  A simple option is to use the build and flaskr modules, and then serve the content in production with waitress.

 All of these steps can be configured simultaneously in specialized CI applications like Jenkins or Github Actions.  There are also other applications, less common but also very useful, such as Gitlab CI/CD, CircleCI, Travis CI or Atlassian Bamboo.

 This quotes app is for a relatively small business, so it is expected that it will not consume too many resources.  Thus, the configuration for the development environment does not need to be very complex.  Therefore, I think a cloud-based environment could be used, which also offers a good level of security for handling sensitive data.
