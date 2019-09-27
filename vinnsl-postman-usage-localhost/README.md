
## Usage

To Create a new Neural Network you have to send the vinnsl data to the vinnsl-service container.
You can use Postman to send the requests. https://www.getpostman.com

###
You have to import vinnsl collection into postman. See [vinnsl postman collection](/vinnsl-postman-usage-localhost/collections)
1. Import collection ![Postman](img/ImportPostman.png)

   Choose vinnsl collection from [vinnsl-postman-collection folder](/vinnsl-postman-usage-localhost/collections)

2. You need to send a post request to localhost:8080/vinnsl with the description of the neural network. Copy our vinnsl-description into the body section of the request.
![Postman](img/2.png)

3. Now you can see that a new neural network was created
![UI](img/3.png)

4. Copy the id of the neural network and send a put request with the vinnsl definition to: localhost/vinnsl/id/definition
(Please replace id with the id of your neural network as shown in the picture)
![Postman](img/4.png)
  
5. Now you can start the training
![UI](img/5.png)
