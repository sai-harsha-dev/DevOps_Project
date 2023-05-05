# Mongodb

These are steps to be followed to configure and build mongodb database.

</br>


- **_STEP 1_** 
    </br>
    Setup the ArgoCD server refer [_here_](./CD/)
    

- **_STEP 2_** 
    </br>

    The necessary helm manifest files are present [_here_](https://github.com/sai-harsha-dev/DevOps_Project_HelmChart.git) under **templates/mongodb** folder. Make sure to update them to the git repository tracked by the ArgoCD server.

    </br>

    [ **Note:** _You need not seperately copy paste the **templates/mongodb** folder to the repo tracked by the ArgoCD server, its enough to clone the whole repository to your repo tracked by ArgoCD_ ]
