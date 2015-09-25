# Codeigniter +Twig + extensions 

# Install

## Purpose ##
        If  you are trying to use twig with Codeigniter.

# Supports 
  - Custome Extensions 
  - Assets folder
  - vardump and Raw ( php ) Extensions

### Usage
###### 1 way Using Composer Autoloader 
*  Copy Config file in  'src/libraries/config/config/php' to 'Application/config' folder and Update.
*  In you controller  Plase Place this Line   
```
    requrie_once(APPATH.'Vendor/autoload.php');
    $this->twig = new Iddigital\Twigextensions\libraries\Twig(); 
```
*  You can load a view like  this - 
	    

	    $data = array();
		$data['foo'] = 'This is cool!';
		$data['bar'] = 'Twig + CodeIgniter rocks!';

        //$this->load->view('home');
	 	//Invoke the template passing the filename, relative to the application/views directory
	    $this->twig->load('home.twig', $data);
 
###### 2 way Using as Codeigniter Libiary 
*  copy  vendor/twig folder into application/third_party folder 
*  Copy Config file in  'src/libraries/config/config.php' to 'Application/config' folder and Update.
*  Copy Config file in  'src/libraries/twig.php' to 'Application/libraries' folder.
*  Plese remove/Comment below line from libraries/twig.php

                //namespace Iddigital\Twigextensions\libraries;
* In your controller  you can now load it as 
*           
            $this->load->library('twig');
        	$data = array();
    		$data['foo'] = 'This is cool!';
    		$data['bar'] = 'Twig + CodeIgniter rocks!';
    	 	//Invoke the template passing the filename, relative to the application/views directory
    	    $this->twig->load('home.twig', $data);

This package is just  an extension of Bennets with Bit more Example usage.

### Version
1.0.0

### Development

Want to contribute? Great! send me a Pull Request.

### Todos

 - Write Tests
 - Marcos
 - Extended Includes 

# About  Twig 
Twig, the flexible, fast, and secure template language for PHP
====
###### Note : Dependency Twig main package - Please  see the below  Documentation 

Twig is a template language for PHP, released under the new BSD license (code
and documentation).

Twig uses a syntax similar to the Django and Jinja template languages which
inspired the Twig runtime environment.

More Information
----------------

Read the `documentation`_ for more information.

.. _documentation: http://twig.sensiolabs.org/documentation

## AUTHORS 

###### Author : Bennet Matschullat <hello@bennet-matschullat.com> 
###### Extended by : kora.jayaram@gmail.com.

License
----

MIT


**Free Software, Hell Yeah!**


