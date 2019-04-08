# TiFramework
TI Hosting test framework

Adding new model
- create table in mysql (example: servers)
  Available fields with extra addon:
      id - integer
      name - using as echo while connecting two models
      _status - modelname_status with fields: id, name, class (class + badge)
      datetime - default timestamp for every model
      image - upload button + saving image + image display
  Connecting models
      Example: 
         model1 name: servers(plural)
         model2 name: server(singular)_informations
       Now are those two models connected
   Adding plural of model
      Add new line in /functions/functions.php
      function plural
      example: 'server' => 'servers',
      So it has to be 'singular' => 'plural'
  Adding title and description for new model
      Add new lines in /includes/page_manager.php
      Example:
        $page['servers']['title'] = "Servers title";
        $page['servers']['description'] = "Servers description";
  Adding model in admin menu
      Add new entry in array in /includes/config.php in $GLOBALS['admin_models']
      Example: $GLOBALS['admin_models'] = [..., 'servers'];
  That's it. You successfully added new model.

Adding client side custom page
    Create new file in /controllers
        This will be name of your page
         Example: new_page.php
         Add these line in it:
            include("views/add_payment.php");
            
    Create view for this controller
        Create new file in /views
        Example: new_page.php
  
      
