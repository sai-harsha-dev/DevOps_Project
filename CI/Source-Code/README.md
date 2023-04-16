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