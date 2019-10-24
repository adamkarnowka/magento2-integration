Installing the Module
------------------------

While you're free to manually install the MentionMe Magento2 module (the use of the app/code folder structure supports this), we recommend using Magento's PHP 
Composer integration for the cleanest installation option. A Magento2 project should have an associated composer.json file, and this file is how developers 
and merchants get new modules in and out of their system.

**Installing the module via Composer (recommended)**

- Add this GitHub repository to your project's composer.json as a composer repository:
```
    composer config repositories.mentionme vcs https://github.com/mention-me/magento2-integration
```

- Add the mentionme/module-mention-me composer dependency to your project's composer.json as a required dependency:
```
    composer require mentionme/module-mention-me --no-update`
```

- Update your project's composer dependencies:
```
    composer update mentionme/module-mention-me
```

- Install the downloaded module via Magento's standard command line tool:
```
    php bin/magento module:enable MentionMe_MentionMe`
    php bin/magento setup:upgrade
```

**Installing the module manually via FTP**

- Click "clone or download" above and select "Download ZIP".

- Copy the "app" folder from the downloaded zip archive in to your Magento root directory.

- Install the downloaded module via Magento's standard command line tool:
```
    php bin/magento module:enable MentionMe_MentionMe
    php bin/magento setup:upgrade
```

After completing the above steps for Composer or manual installation the MentionMe module will be installed ready for configuration. Please note, if you are
running PHP OPcache on your server and have configured it not to clear automatically then you will need to clear the OPcache in order for the new module to become 
available after the above steps.

Configuring the Module
----------------------

The module's configuration can be found in the Magento admin panel under Stores > Configuration > MentionMe.

You will first need to add you unique account code in the Genral section of the configuration. Once this is added, the MentionMe integrations will be enabled on 
your storefront. Depending on where the module is installed you will need to select either the Demo or Live API Mode configuration. To globally disable all of the 
integrations at any time change the General setting for "Enabled" to the "Disabled" value.

Each seperate integration then has its own section of configuration, allowing you to enable or disable each integration individually.

The Referee and Conversion Message integrations have an additional configuration to select where on the page the MentionMe content will display. The dropdown of options
is based on the available layout containers for your theme. This allows you to select an existing container from the base theme or add a new container in your theme especially 
for placing the MentionMe content. Alternatively you may want to add the MentionMe placeholder html directly in to your theme's templates, to do this select the 
"I will manually add the tag" option, which will prevent the module from automatically adding the content.

Upgrading the Module
--------------------

**Upgrading the module via Composer (recommended)**

- Update the mentionme/module-mention-me composer dependency to the latest stable release in your project's composer.json
    composer require mentionme/module-mention-me --no-update

- Update your project's composer dependencies
    composer update mentionme/module-mention-me

- Install the updated module via Magento's standard command line tool
    php bin/magento setup:upgrade

**Upgrading the module manually via FTP**

- Click "clone or download" above and select "Download ZIP".
- Ensure you completely remove the exisiting app/code/MentionMe directory
- Copy the new "app" folder from the downloaded zip archive in to your Magento root directory.

- Install the updated module via Magento's standard command line tool
    php bin/magento setup:upgrade

**Support**

*Important: As with installing any new software on your system, don't forget to take appropriate backup steps, and to test your release in a 
development or staging environment before deploying to production.*

If you have any concerns or questions, please send an email to clientsuccess@mention-me.com with all the relevant details that are needed to investigate or resolve the issue.
