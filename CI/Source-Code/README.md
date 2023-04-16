# Application Setup

![Alt text](App-components.png)

# Application Components

The application used for the CI-CD demonstration consists of the following components :-

1. **FRONTEND** - This component has the source code for generating User Interface that is presented over the web for end user interaction.

    - Click [_here_](./frontend) for the source code.
    
    </br>

2. **MongoDB** - This component is used to store the User and Catalogue information used by the website.
 
    - Click [_here_](../CD) for build instruction

    </br>

3. **Catalogue** - This component consists of NodeJS API code used to interact with MongoDB component and fetch Catalogue data to present to end user.

    - Click [_here_](./catalogue) for the source code.
 
    - Click [_here_](../CD) for build instruction

    </br>

4. **Redis** - This component is a Redis cache server used to cache Cart and User information.

    - Click [_here_](../CD) for build instruction

    </br>

5. **User** - This component is a NodeJS API code used to interact with MongoDB server and fetch User information

    - Click [_here_](./user) for the source code.
 
    - Click [_here_](../CD) for build instruction

    </br>

5. **Cart** - This component is a NodeJS API code used to interact with Redis server and fetch items put in cart.

    - Click [_here_](./cart) for the source code.
 
    - Click [_here_](../CD) for build instruction

    </br>


2. **MySQL** - This component is used to store the Shipping information used by the website.
 
    - Click [_here_](../CD) for build instruction

    </br>

5. **Shipping** - This component is a Java based API code used to interact with MySQL server and create shipping of the iteams in cart.

    - Click [_here_](./shipping) for the source code.
 
    - Click [_here_](../CD) for build instruction

    </br>

2. **RabbitMQ** - This component is used to store the Payment information used by the website and send notification to user's after payment completion using message queue service.
 
    - Click [_here_](../CD) for build instruction

    </br>

5. **Payment** - This component is a Python based API code used to interact with RabbitMQ server and process payments.

    - Click [_here_](./payment) for the source code.
 
    - Click [_here_](../CD) for build instruction

    </br>

5. **Dispatch** - This component is a Golang based API code used to interact with RabbitMQ server and process dispatch.

    - Click [_here_](./dispatch) for the source code.
 
    - Click [_here_](../CD) for build instruction

    </br>