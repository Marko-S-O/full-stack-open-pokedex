I'm choosing enterprise Java. The choise of tools depends wether we are doing platform agnostic development or want to commit ourselves to a cloud provider in a way that is not easy to reverse. I chooce the first option even if it's not very fashionable.

First, we need to choose a tool for the CI/CD platform: Jenkins. It's usually safe to pick an industry standard solution unless there is no clear reasoning to choose something else.

The components for linting, building, testing, packaking and deployment would follow the principle:

    Linting: SonarQube, a static code analyze tool can be configured to do this
    Building: Maven
    Testing: JUnit for unit testing, Robot Framework for end-to-end testing.
    Packaking: Maven again
    Deployment: Docker if containers would be allowed in production environments

I don't really know much about alternatives for Jenkins. If we exclude tools dedicated to certain cloud platform, there seem to be at least TeamCity and Bamboo. TeamCity benefits seem to be high configurability and extensibility and Bamboo integrates well with the Atlassian environment (Jira, Confluence etc.) which many large corporations use for IT project and requirements management.

For the last question, we should define what we mean by cloud based environment. If we just use the cloud as deployment platform, the configuration is obviously fine. If our startegy is to get full benefit from cloud by cloud native solutions, we should use the services that are native to and promoted by the particular cloud environment. This would probably mean re-planning the CI/CD stack.
