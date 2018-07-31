---
layout: layout.pug
navigationTitle:  Command Reference
title: Command Reference
menuWeight: 60
excerpt: Commands used in the DC/OS Spinnaker Service
featureMaturity:
enterprise: false
---

Here is the cpmplete list of DC/OS Spinnaker Commands Available:

usage: dcos spinnaker
  


Flags:

  -h, --help               Show context-sensitive help.
  
  -v, --verbose            Enable extra logging of requests/responses
  
      --name="spinnaker"  Name of the service instance to query

Commands:

  help 
    [<command> ...]
      Show help.

  1. List IDs of all available configurations
  
       config list

  2. Display a specified configuration
  
       config show <config_id>
    

  3. Display the target configuration
       
       config target
    
  4. List ID of the target configuration

       config target_id

  5. List IDs of all available configurations

       debug config list
    
  6. Display a specified configuration 

       debug config show <config_id>
    
  7. Display the target configuration
    
       debug config target
    
  8. List ID of the target configuration 

       debug config target_id
    
  9. Display the Mesos framework ID 

       debug state framework_id
    
  10. List names of all custom properties

       debug state properties
    
  11. Display the content of a specified property

       debug state property <name>
    
  12. Refresh the state cache, used for debugging

       debug state refresh_cache
    
  13. Pauses a pod's tasks for debugging

       debug pod pause <flags> <pod>
       -t, --tasks=TASKS ...  List of specific tasks to be paused, otherwise the entire pod   
    
  14. Resumes a pod's normal execution following a pause command
    
       debug pod resume <flags> <pod>
       -t, --tasks=TASKS ...  List of specific tasks to be resumed, otherwise the entire pod
    
  15. View the configuration for this service
       
       describe
    
  16. View client endpoints

       endpoints <name>
    
  17. Show all plans for this service
 
       plan list
    
  18. Display the status of the plan with the provided plan name

       plan status <flags> <plan>
       --json  Show raw JSON response instead of user-friendly tree
    
  19. Start the plan with the provided name and any optional plan arguments

       plan start <flags> <plan>
       -p, --params=PARAMS ...  Envvar definition in VAR=value form; can be repeated for multiple variables


  20. Stop the running plan with the provided name
       
       plan stop <plan>

  21. Pause the plan, or a specific phase in that plan with the provided phase name (or UUID)
   
       plan pause <plan> <phase>
    
  21. Resume the plan, or a specific phase in that plan with the provided phase name (or UUID)

       plan resume <plan> <phase>
    
    
  23. Restart the plan with the provided name, or a specific phase in the plan with the provided name, or a specificstep               in a phase of the plan with the provided step name.

       plan force-restart <plan> <phase> <step>
    
  24. Force complete a specific step in the provided phase. Example uses include the following: Abort a sidecar operation due to observed failure or known required manual preparation that was not performed

       plan force-complete <plan> <phase> <step>
    
  25. Display the list of known pod instances

       pod list
    
  26. Display the status for tasks in one pod or all pods

       pod status <flags> <pod>
       --json  Show raw JSON response instead of user-friendly tree

  27. Display the full state information for tasks in a pod
        
       pod info <pod>
    
    
  28. Restarts a given pod without moving it to a new agent

       pod restart <pod>
    
  29. Destroys a given pod and moves it to a new agent

       pod replace <pod>
    
  30. Display the Mesos framework ID
   
       state framework_id
   
    
  31. List names of all custom properties

       state properties 
       
  32. Display the content of a specified property 
  
       state property <name>
  
  33. Refresh the state cache, used for debugging

       state refresh_cache 

  34. Launches an update operation

       update start <flags>
       --options=OPTIONS  Path to a JSON file that contains customized package installation options
       --package-version=PACKAGE-VERSION  
                          The desired package version
       --replace          Replace the existing configuration in whole. Otherwise,the existing configuration and options are merged.

  35. Force complete a specific step in the provided phase
      
       update force-complete <phase> <step>
           
  36. Restart update plan, or specific step in the provided phase
 
       update force-restart <phase> <step>
         
  37. View a list of available package versions to downgrade or upgrade to
 
       update package-version
    
  38. Pause update plan
 
       update pause 
     
  39. Resume update plan 

       update resume
    
  40. View status of a running update
 
       update status <flags>
       --json  Show raw JSON response instead of user-friendly tree
