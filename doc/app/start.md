fhc-start(1)
============
## SYNOPSIS

 fhc app start --app=<app> --env=<env>

## EXAMPLES

  fhc version                                                                                                
  fhc app act --app=1a2b3c --fn=<serverside Function> --data=<data to send> --env=<environment>              Performs an act request on app with id 1a2b3c
  fhc app cloud --app=1a2b3c --path=<serverside path from root> --data=<Data to send> --env=<environment>    Performs a cloud request on app with id 1a2b3c
  fhc app create --project=1a2b3c --title=My New App --type=cloud_nodejs                                     Creates a new hybrid app
  fhc app delete --project=1a --app=2b                                                                       Deletes app with id 2b under project with id 1a
  fhc app endpoints --app=1a2b --env=dev                                                                     Lists all endpoints exposed by app with guid 1a2b in the dev environment
  fhc app list --project=1a2b3c                                                                              Passing project using a flag
  fhc app list 1a2b3c                                                                                        Passing project as an argument
  fhc stage --app=<appGuid> --env=<environmentName>                                                          
  fhc start --app=<appGuid> --env=<environmentName>                                                          


## OPTIONS

  --data         Request body to send thru                                                                                                             [required]
  --fn           Cloud function name to call                                                                                                           [required]
  --path         Path of the cloud request                                                                                                             [required]
  --title, -t    A title for your app                                                                                                                
  --type, -y     Type of your app - e.g. client_hybrid, client_native_ios, client_native_android, cloud_nodejs                                         [default: "client_hybrid"]
  --runtime, -r  The Node.js runtime of your application, e.g. node06 or node08 or node010                                                           
  --clean, -c    Do a full, clean stage. Cleans out all old application log files, removes cached node modules and does an 'npm install' from scratch

## DESCRIPTION

starts a cloud application. This command will only work if the app has previously been deployed
