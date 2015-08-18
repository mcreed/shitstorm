ShitStorm Framework
=========

## Production ready! Definitely use on live sites.

Based on the ShitStorm Cloud provisioning service. Everything autoscales 

    #require 'shitstorm-config.php';
    #require 'shitstorm.php';
  
    // Just enter your api token and $amount you want to spend in dollars to keep the site running
    $shitstorm = new ShitStorm('APITOKENHERE', 100.99);
  
    // This could probably load up your file
    $shitstorm->shit('html', '/', function(){
  
      return "<h1>Look, a shitty webpage.</h1>";
    
    });
  
    // When somebody posts data
    $shitstorm->eat('json', '/somedumbfuckingroute', function(){
  
      $thing = new Thing($_POST); // Validates the thing, auth tokens, and other bullshit
      return ($thing->save() ? $thing : 'Shit broke');

    });
  

Development at http://localhost:8000
  
    vagrant up

Staging

    deploy shitstorm_breakallthethings

Deployment

    deploy makethatshitlive
  
    Y/n
