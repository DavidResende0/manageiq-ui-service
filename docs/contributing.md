# Contributing
Any contribution should observe the convention set fourth in the [Code Tour](code_tour.md).
The following must complete without error prior to making a pull request:

1. `yarn vet`
2. `yarn test`

## Testing
When adding or modifying functionality, unit and integration tests must accompany any changes.
Examples of both state and component tests can be found in `tests/`.
If any notional data is required for the test ensure an appropriately titled folder is created in `tests/mock/`.

If you would like to run unit tests for the project, you can run   
```yarn test ```  

If you would like to run the integration tests locally for the project please be sure to first have a running copy of the frontend and a running backend server.  You can either use a ManageIQ backend or test with our Mock API running locally.  These are the commands to launch the frontend and our mock api
  
``` yarn start ```  (Starts a frontend web server - Port 3001)
```yarn add @manageiq/manageiq-api-mock```
```cd node_modules/@manageiq/manageiq-api-mock/ && node index.js``` (Starts our Mock REST API - Port 3000)

After those are running please ensure you have selenium server installed and running  

- ``` yarn global add protractor ```
- ``` webdriver-manager update ```  
- ``` webdriver-manager start```

Now that your selenium server is running and listening open another terminal window and from the projects root directory, run   
 
```yarn test:e2e ``` (Kicks off tests)

## How To...
* [Add a Functional Zone](./howto.md#Addafunctionalzone)
