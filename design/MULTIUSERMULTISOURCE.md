# Multiple Source Multiple Applications

The most common case for modern devices to have multiple sources generating content. For example, a camera source which takes signal from external world, which is then fed to a Inferencing Engine to modify or alter the content.

The Assumptions are listed below

1. Multiple user applications are driving the camera and receiving content (image or video) from camera source.

2. User Application may feed the camera generated content to an Inferencing Engine which further alters the image.

3. It is requirement to gather assertion from orginal camera capture image.

4. It is a requirement to capture ML Model generated modifications as provenance data

5. Hence the store might have Ingredient Assertions (from Camera) OR alternatively two Manifest the Camera content Manifest and a second Ingredient Manifest for the Content modified by the ML Model

6. The user applications are running in an execution environment, likely to be Non Secure World or in Rich OS execution Environment.

7. It is likley that the Claim Generator which creates Assertions and Claims pertaining to an Asset is in the same execution, i.e. Rich OS Environment. However for the sake of abstraction it is shown running in a seperate context in the diagram below.

8. It is expected that the Claim Signer Key is stored as part of a protected Environment like a TEE or running in a completely 
isolated secure element.

9. It is important to highlight that the Storage indicated below, is a shared storage for saving the Assertions, Claims which are created by the User Applications and Claim Generator respectively. In addition it also saves the Manifests post the signing operations are complete.
The Claim stored in the data store is read by the Claim Generator and sent to the Claim Signing service running in the seperate context. The signed Claim (i.e. the Claim and its signature) are stored as Manifests in the Store.


It is TBD to discuss the security of the storage which is essential for overall security of the architecture.

Full Block Diagram of the deployment is indicated below.

![Multiple Source Multiple Applications](images/MultiUserMultiInput.svg)