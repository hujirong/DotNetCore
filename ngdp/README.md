The purpose of this repo is to demonstrate the ability to on-board an existing repo and dploy a .NET Core 2.1 application using the MGDP

## NGDP Process
After onboarding with the NGDP application, the following files were injected into the application

NGDP Pull Inject Request - 
ngdp-sample-dotnet-api
    Dockerfile
    docker-entrypoint.sh
    ngdp
        ngdp-config.yml
    ocp_configs
        build_templates
            build_template.yaml
        deploy.groovy
        deploy_templates
            deploymentconfig_template.yml
            route_template.yml
            service_template.yml

## Customization
After the repository was onboarded using the NGDP pipeline, the folliwing changes needs to be done before hte NGDP Pipeline succeed to deploy to dev:

--- Dockerfile
    - Updated the source Docker Image for hte build