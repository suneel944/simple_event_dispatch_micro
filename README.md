# Simple event dispatch micro
A simple event dispatcher and receiver to mimicking realtime development repo CI/CD pipeline

# How does it work?
Basically, whenever a application changes are pushed to main, and it is successfully completed,
 - A trigger event is sent to the test repo to start testing
 - The test repo starts testing as per the given instructions in the workflow file and once completed, triggers back an event to development repo, to trigger the releasing of the application to prod
 - Once the development repo receives the trigger event to release the app to prod, it starts working on the workflow file which is responsible for cutting a new release branch and then deploying the application in any cloud or self hosted servers

****
