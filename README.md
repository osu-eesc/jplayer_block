jPlayer Block
=============

Creates blocks using the jPlayer plug-in for viewing video and 
audio using html 5 with a Flash fallback for older browsers.
--------------------------------------------------------------


Requirements
------------

Add this code to the page.tpl.php file BEFORE "print $scripts"
<?php if (module_exists('jplayer_block')): // load newer version of jquery and set noConfict for jplayer ?>
  <script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.6/jquery.min.js"></script>
  
  <script type="text/javascript">
    var nuJQ = jQuery.noConflict();
  </script>
  
  <?php $jplayer_path = $base_path . drupal_get_path('module', 'jplayer_block') . '/js/jquery.jplayer.min.js'; ?>

  <script type="text/javascript" src="<?php print $jplayer_path; ?>"></script>
 
<?php endif; ?>