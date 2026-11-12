# PHP CI Test
The goal is to auto-deploy PHP project by pushing on github without manually uploading the files in the php hosting provider.

### Setup
1. Create a `config/env.config.php` that contains:
    ```php
    <?php

        $SAMPLE_CREDENTIAL = "This is a very sensitive secret!";
    ```
2. Run `php -S localhost:[PORT]`. Choose a port you want to run your project.

### Deployment
- When using github as a source repository, configure the following in github secrets with an environment named `production`:
    - `SAMPLE_CREDENTIAL`
    - `DEPLOY_DIRECTORY`
    - `FTP_SERVER`
    - `FTP_USERNAME`
    - `FTP_PASSWORD`