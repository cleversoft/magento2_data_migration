<h3>Supported versions</h3>
We support the following versions for migration:
- Magento Community Edition (CE) versions: 1.6.x, 1.7.x, 1.8.x, CE 1.9.x
- Magento 2 version 0.74.0 beta x

<h3>To use this migration tool, follow the steps below:</h3>

<h4># Step1: Install Magento 2</h4>
- Download the latest version of Magento2 from Github
- Follow our <a href="http://www.ubertheme.com/magento-news/magento-2-0-installation-guide/">Installation guide</a> to Install Magento 2

<h4># Step2: Install & Configure the tool</h4>
- Make a folder named "migrate_data_tool" in your web root. (For example: PATH_TO_YOUR_WEB_ROOT_FOLDER\migrate-data-tool)
- Download the latest version of this tool at https://github.com/ubertheme/magento2_data_migration/releases
- Extract all source code from downloaded file to the folder you have just created (migrate_data_tool).
<div class="center">
<p align="center"><img src="http://joomlart.s3.amazonaws.com/images/userguide/jm_tips/migrationData/migrate.jpg" alt="Magento 2 Migration Data Tool" /></p>
</div>

- Make writeable permission for folders at:
    - <strong>PATH_TO_YOUR_WEB_ROOT_FOLDER\migrate-data-tool\assets </strong>
    - <strong>PATH_TO_YOUR_WEB_ROOT_FOLDER\migrate-data-tool\protected\runtime </strong>
- Make writeable permission for config file at:
    - <strong>PATH_TO_YOUR_WEB_ROOT_FOLDER\migrate-data-tool\protected\config\config.php </strong>

<h4># Step 3: Run this tool in your browser to migrate your data</h4>
- Open your browser and type in the url to run this tool.
For example: go to http://localhost/migrate-data-tool/ and press Enter key.
- Follow step by step to migrate needed Data from Magento 1 website to Magento2 website.

Some step screenshots will go here...

<h4># Step 4: Complete the tasks below to finish the data migration process.</h4>
- Re-save all the Attribute Sets (Stores/Attributes/Product Template) migrated in the back-end of your Magento 2 website. (Open the attribute set, edit it if needed and click the save button)
- Reindex all data:
    - In Linux: Run command line: php -f PATH_TO_YOUR_WEB_ROOT_FOLDER\your_magento2_folder\dev\shell\indexer.php --reindexall
    - In Window: Open the command line window and go to the folder: <strong> PATH_TO_YOUR_WEB_ROOT_FOLDER\your_magento2_folder\dev\shell </strong>
    and type in the command line: php indexer.php reindexall
    then press enter key to re-index all data in your Magento 2 website.
    - Note: If you are using <strong> Magento 2 version 0.74.0 - beta 9 or later</strong>: To reindex all data, run following command line:
    <strong> php -f PATH_TO_YOUR_WEB_ROOT_FOLDER\your_magento2_folder\bin\magento indexer:reindex </strong
<div class="center">
<p align="center"><img src="http://joomlart.s3.amazonaws.com/images/userguide/jm_tips/migrationData/img-2.jpg?v=20150401144700" alt="Magento 2 Migration Data Tool" /></p>
</div>

- Copy media files to complete migration:<br/>
  - Copy the folder at PATH_TO_YOUR_WEB_ROOT_FOLDER\your_magento1_folder\media\catalog and paste replace to PATH_TO_YOUR_WEB_ROOT_FOLDER\your_magento2_folder\pub\media\
  - Copy the folder at PATH_TO_YOUR_WEB_ROOT_FOLDER\your_magento1_folder\media\downloadable and paste replace to PATH_TO_YOUR_WEB_ROOT_FOLDER\your_magento2_folder\pub\media\

<h4># Step 5: Now you can test the data which have been migrated into your Magento 2 website from the browser.</h4>
