# IBM IoT simulation

# Requirements
IBM account id
IoT Resource


This is a description of how the IBM IoT platform can be used to create an application in the internet of things domain.  An IoT can be started out of a cloud platform, however, the cloud advantage is that IoT is a managed service which means that the management activities like applying patches is executed by the cloud/platform provider.  Of course, the owner of the application is responsible for maintaining the devices and the application and the resources cost money depending on usage.

The basic communication in this example is to simulate a device (data producer) and an application (data consumer) using a couple of python programs and some data to simulate a device generating data and an application consiming it.  The flow of the data in the form of messages can be described by the following diagram

![image](https://user-images.githubusercontent.com/98497219/168705745-2437c987-f531-47cb-8e04-f954982ea0e7.png)

The producer and consumer can be a variety of entities as long as they support the IoT communication protocol which in this case MQTT is being used.  A couple of programs written in python are added to this project that can generate and receive data; however, the organization and credentials used during execution are not visble for security purposes.

**Description of the producer**
- Import libraries
- Define connection via a client id
- Connect to IoT device
- Generate and send data
- Disconnect from device

**Description of the consumer**
- Import libraries
- Define connection via an application id
- Connect to IoT resource
- Subscribe to a device topic
- Receive data
- Disconnect from topic

The used programs plot the data to visually check that sent and received data looks similar

## Additional info to replicate the example
The following are the high level steps to duplicate the IoT example:
- Sign in or create an IBM cloud account
- Create an IoT resource:  This can be looked in the search spot and then create the resource
- Work with an existing IoT resource or use the one created in previous step
- Sign in using the IBM id
- Select organization
- Add devices that support IoT communication 
- Generate keys for application authentication 

**Screenshots**
Sign in or create an account
![image](https://user-images.githubusercontent.com/98497219/168708408-817a6e94-7ecc-4c09-b435-0986edc58b8b.png)

Create an IoT resource:  This can be looked in the search spot and then create the resource
![image](https://user-images.githubusercontent.com/98497219/168708437-0e5d5287-28c5-48eb-8602-7326fa1c1cac.png)

Work with an existing IoT resource or use the one created in previous step
![image](https://user-images.githubusercontent.com/98497219/168708485-bbf69b03-e4fb-4ecf-8c08-c2aa71d6fa08.png)

Sign in using the IBM id
![image](https://user-images.githubusercontent.com/98497219/168708524-a4caff87-1d47-4296-bce0-39b557fdbb58.png)

Select organization
![image](https://user-images.githubusercontent.com/98497219/168708557-adc4b550-7964-4c17-a239-e32deb1c4d4d.png)

Add devices that support IoT communication protocols or use an existing one.  During this process a device id, device type an authentication token are created for device connections.
![image](https://user-images.githubusercontent.com/98497219/168708593-6539f086-3250-4677-b7d7-35166418c49f.png)

There is one section to generate keys for application authentication and connection as data consumers.
![image](https://user-images.githubusercontent.com/98497219/168708621-b04a2559-fd84-43c4-8d73-25c8bed960ca.png)

Create a key: This step generates an access key equivalent to the user/pw combination.
![image](https://user-images.githubusercontent.com/98497219/168708683-1ead26cb-ae48-4a2c-ab5c-e7987ac77e70.png)

