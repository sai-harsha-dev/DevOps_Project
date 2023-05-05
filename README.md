# DevOps_Project
This is a sample website with multiple components used to demonstrate the different stages of CI/CD pipeline.

## Setup Workflow
---
![CI-CD Workflow](DevOps_Project_Flowchart_image.png)

The above image illustrates the CI-CD workflow and component enabling each stage of the CI-CD workflow used in this project.

## Setup Components
---
The complete setup consists of following component's elaborated below :- 

1.  **Source Code** :- The source code includes 

    - Web Components Code - Includes the necessary code files for all the website's components. For more details refer [_Source-Code_](./CI/Source-Code) folder
      
    - Helm Manifests Code - Containes the final helm chart, the necessary manifest files needed to deploy all the website's components. For more details refer [_Helm-chart-repo_](https://github.com/sai-harsha-dev/DevOps_Project_HelmChart.git)

    - Infrastructure Code - Includes the necessary code files to configure Infrastructure components. For more details refer [_Infra_](./Infra/) folder

2. **CI Server** - Elaborated as Continues integration Server, for more details of the configuration refer [_CD_](./CD/) and functionalitiy refer [_Build_](./CI/Build) folder.

3. **Code Analysis** - This component is used to test the quality of the source code, for more details of the configuration refer  [_CD_](./CD/) and functionality refer [_Build_](./CI/Build) folder.

4. **Build Tools** - This components consists of the necessary software components used to build the final artifacts from source code, for more details of the configuration [_CD_](./CD/) and functions refer [_Build_](./CI/Build) folder.

5. **Containerization Platform** - This component is used for building container images from the source code, for more details of the configuration [_CD_](./CD/) and for functionality refer [_Build_](./CI/Build) folder.

6. **Artifact Repository** - This components is used for centralised hosting of the final artifacts/Images of the website components, for more details of the configuration refer [_CD_](./CD/) and for functionality refer [_Build_](./CI/Build) folder.

7. **CD Tool** - Elaborated as Continues deployment tool is used for deployment of build artifacts to deployment platform/environment, for more details of the configuration and functionality refer [_CD_](./CD/) folder.

8. **Container Orchestrator** - This component is used to build the platform/environment where the final application is deployed, for more details of the configuration and functionality refer [_CD_](./CD/) folder.
  
9. **Monitoring** - This component is used to monitor the health of deployed application,   for more details of the configuration and functionality refer [_CD_](./CD/) folder.


## Setup Stages 
---
The whole setup involves the following stages to be performed, elaborated below :-

#### \*\* NOTE :- _The sequence of steps followed is indicated in the [_Setup Workflow_](#setup-workflow) with a numbered circle icon besides the flow arrow symbol_ \*\* 

</br>

1. **Hosting source code in GIT repository** - Refer [_Source-Code_](./CI/Source-Code) for set up.

2. **Build Application Artifacts** - Refer [_Build_](./CI/Build) for set up.

3. **Store Built artifacts in Artifacts Repository** - Refer [_Build_](./CI/Build) for set up.

4. **Built container Images from built artifacts** - Refer [_Build_](./CI/Build) for set up.

6. **Store the built Image in Artifact repository** - Refer [_Build_](./CI/Build) for set up.

7. **Update the [Helm manifast files repo](https://github.com/sai-harsha-dev/DevOps_Project_HelmChart.git)** - Refer [_Build_](./CI/Build) for set up.

8. **Setup Continues Deployment of chart in [Helm manifast files repo](https://github.com/sai-harsha-dev/DevOps_Project_HelmChart.git)** - Refer [_CD_](./CD/) for set up.

9. **Setup the deployment environment and run application containers in Kubernetes** - Refer [_CD_](./CD/) for set up.

10. **Monitor application health in Kubernetes** - Refer [_CD_](./CD/) for set up.


  
  

