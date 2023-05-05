# Application Setup

![Alt text](App-components.png)
</br>
 
This folder consists of the source code in compressed zip format for the different components of the website:-

</br>

### **FRONTEND** 
---
 This component has the source code for Websites main page written in simple HTML, CSS, Javascript.

 The main functionality of this component is to present the end user with Web interface to interact with the web page.

- Click [_here_](./frontend) for    the source code.

The frontend component talks with the backend components through API calls for carrying out actions on database and execute different functions of the website.

</br>

### **BACKEND** 
---
The backend components implement the actual code necessary to perform different funtionality of website

The following backend components are:-

1. **Catalogue** - This component consists of NodeJS API backend code used to interact with MongoDB database and fetch Catalogue data to present to end user.

    - Click [_here_](./catalogue) for the source code.
 
    </br>

3. **User** - This component is a NodeJS API backend code used to interact with MongoDB database and fetch User information.

    - Click [_here_](./user) for the source code.

    </br>

4. **Cart** - This component is a NodeJS API backend code used to interact with Redis server and implememt the cart section of website.

    - Click [_here_](./cart) for the source code.

    </br>

5. **Shipping** - This component is a Java based API backend code used to interact with MySQL database and create shipping section of the website.

    - Click [_here_](./shipping) for the source code.

    </br>

6. **Payment** - This component is a Python based API backend code used to interact with RabbitMQ server and process payments.

    - Click [_here_](./payment) for the source code.
 
    </br>

5. **Dispatch** - This component is a Golang based API backend code used to interact with RabbitMQ server and process dispatch.

    - Click [_here_](./dispatch) for the source code.

     </br>


### **DATABASES/CACHING**
---
The site makes use of the following databases and cache servers.

- **_Mongodb_** -- for storing catalogue, user crendentials

- **_MySql_** -- for storing shipping information

- **_RabbitMQ_** -- for sending payment notification

- **_Redis_** -- for caching user data

These components are configured as a part of final helm chart/manifest files. Refer [Helm manifast files repo](https://github.com/sai-harsha-dev/DevOps_Project_HelmChart.git) 

 
## Next Stage
---
Click [_here_](../Build) for build instruction for each component of the website.

   