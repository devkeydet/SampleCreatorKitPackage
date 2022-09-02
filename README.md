# Sample Creator Kit Package Deployer Package

> [!WARNING]
> This is a proof of concept.  Do not use this for your own deployment of the creator kit.  It is not maintained with current releases of the kit.  Current releases are available at https://github.com/microsoft/powercat-creator-kit.

Example of how we might automate Creator Kit Deployment to make it easier to install.  This is the tech App Source uses to enable one to perform environment configurration changes before solution import, deploy multiple solutions, deploy data after solution import, etc.

The sample does the following:

- Enables PCF for canvas in the target environment
- Imports the three solutions into the target environment

## Installation

1. Install the Power Apps CLI

    ```
     winget install Microsoft.PowerAppsCLI
    ```

1. Download the zip file from the release page
1. Make sure you have a pac authentication proflie setup for your environment.

   ```
    # use the following pac commands to list, select, or create a profile
    pac auth list
    pac auth select
    pac auth create
    ```

1. Run the following command deploy the creator kit

    ```
    pac package deploy --package SampleCreatorKitPackage.zip
    ```
