# Single Source Multiple Applications

The deployment is for a very simple use case, like a dedicated Rasberry Pi having a Camera with a multiple applications driving the camera to generate content. 

The Assumptions are listed below

1. Multiple user applications are driving the camera and receiving content (image or video) from camera source.

2. The user applications are running in an execution environment, likely to be Non Secure World or in Rich OS execution Environment.

3. It is likley that the Claim Generator which creates Assertions and Claims pertaining to an Asset is in the same execution, i.e. Rich OS Environment. However for the sake of abstraction it is shown running in a seperate context in the diagram below.

4. It is expected that the Claim Signer Key is stored as part of a protected Environment like a TEE or running in a completely 
isolated secure element.

5. It is important to highlight that the Storage indicated below, is a shared storage for saving the Assertions, Claims which are created by the User Applications and Claim Generator respectively.
The Claim stored in the data store is read by the Claim Generator and sent to the Claim Signing service running in the seperate context.

It is TBD to discuss the security of the storage which is essential for overall security of the architecture.

Full Block Diagram of the deployment is indicated below.

![Single Source Multiple Applications](images/MultiUserSingleSource.svg)
