# CLI Cheat Sheet
This file describes some frequently used `oc` commands.

## Getting Help
Command | Description
--------| -----------
oc help | Get help
oc help command [subcommand] | Get specific help on a command with optional resource/subcommand

## Projects
Command | Description
--------| -----------
`oc new-project NAME` | Create a new project with `NAME`
`oc delete project NAME` | Delete the project `NAME`

## Creating an Application
Command | Description
--------| -----------
`oc new-app [--name <NAME>] <DOCKER_IMAGE>\|<GIT_REPO>\|<TEMPLATE>\|...` | Create the resource tree of an _application_ from a docker image, git repo, template, or ...


## Getting information
Command | Description
--------| -----------
`oc status` | Get status of a project.
`oc describe <RESOURCE>` | Describe the Openshift resource `RESOURCE`.
`oc get <RESOURCE>` | Get brief summary information about a resource.
`oc get <RESOURCE> -o json` | Get all information from a resource in JSON format.
`oc get all` | Get summary information of all resources in the project.


## View Logs
Command | Description
--------| -----------
`oc logs <POD>` | View the log of a pod on stdout. Pods can also be indirectly referred to through an owning resource, like a BuildConfiguration.

## Creating Resources
Command | Description
--------| -----------
`oc create <TYPE> <NAME> ...` | Create a resource of type `<TYPE>` with the name `<NAME>`.

## Deleting Resources
Command | Description
--------| -----------
`oc delete <RESOURCE>` | Delete a resource
`oc delete --all all` | Delete all (most) resources in the current project.
`oc delete all -lapp=my-app` | Delete all (most) resources with the label `my-app` in the current project.

## Managing Routes
Command | Description
--------| -----------
`oc expose svc <SVC>` | Create a route to the service `<SVC`.
`oc get route` | List all routes in the current project. 

## Managing Environment Variables
Command | Description
--------| -----------
`oc set env <RESOURCE>`... | Setenv. variables in `<RESOURCE>`. Resource is most conveniently a DeploymentConfig, but can also be more finegrained, like replication controller or pods.

## Managing Propes
Command | Description
--------| -----------
`oc set probe dc/<APP> --readiness|--liveness --get-url=...` | Set a HTTP probe on the deployment config of `APP`.

## Managing Builds
Command | Description
--------| -----------
`oc start-build <BC>` | Start a build of build configuration `<BC>` manually.

