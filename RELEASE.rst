Release Notes
=============

Version 0.6.0
-------------

- adding version number so this will work with our release-script
- Fixed test failure issues on sga (#146)
- Removed import in __init__
- Center modal and fix scrolling
- Installed bower with URI.js, require.js, underscore, jquery
- Add actions cell to assignments table header.
- Added basic developer notes.
- Added sorting plugin to header table, Now you can sort each column by clicking header
- Handle file not found error, Fixed error messages, set error code to 404
- Allow not only english language file uploads
- Implement support for multiply SGA elements at one vertical
- fixed all posible pylint issues
- fix jshint indentified issue for all studio and edx_sga file
- merge base and fixed error message display under button error and loaded max file size from settings
- Added log.info in all locations where sga.py is chaning state of StudentModule
- added display name on sga lms and grade submission dialog
- Changed enter grade link style to make it look like button and added some spaces in css attributes
- Added weight validations and test cases, split long length test into sub funtions
- Design changes in sga settings page, added a settings tab and style in css file, added some classes

Migrations
----------

0.5.0 uses the edX Submissions API to submit grades. If you are upgrading from an 
version before 0.4.0 and you have student submissions and grades that need to be migrated, 
you should run the migration script. 

.. code-block:: bash

  python manage.py lms --settings=aws sga_migrate_submissions DevOps/0.001/2015_Summer
  
NOTE: After applying this update, you may need to change max_score on SGA 
problems to an integer.   

Additions
---------

- Validates max_score and grades to ensure they are non-negative integers
- Works with split mongo
- Added Staff Debug

Fixes
-----

no fixes in this release
