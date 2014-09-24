ShitStorm Framework
=========

Based on the ShitStorm Cloud provisioning service.

    #require 'shitstorm-config.php';
    #require 'shitstorm.php';
  
    $shitstorm = new ShitStorm();
  
    // This could probably load up your file
    $shitstorm->shit('html', '/', function(){
  
      $s = "<h1>Apparently this shit works</h1>";
    
    });
  
    // When somebody posts data
    $shitstorm->eat('json', '/somedumbfuckingroute', function(){
  
      $thing = new Thing($_POST); // Validates the thing, auth tokens, and other bullshit
      if($thing->save()) {
        return $thing;
      } else {
        return 'Shit broke';
      }
    
    });
  

Development at http://localhost:8000
  
    vagrant up

Staging

    deploy shitstorm_breakallthethings

Deployment

    deploy makethatshitlive
  
    Y/n
