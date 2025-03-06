# Single Source Single Application

The deployment is for a very simple use case, like a dedicated Rasberry Pi having a Camera with a single application driving the camera.

The Assumptions are listed below

1. Only one user application is driving the camera and receiving content (image or video) from camera source.

2. The user application is running in an execution environment, likely to be Non Secure World or in Rich OS execution Environment.

3. It is likley that the Claim Generator which creates Assertions and Claims pertaining to an Asset is in the same execution, i.e. Rich OS Environment.

4. It is expected that the Claim Signer Key is part of a protected Environment like a TEE.

Full Block Diagram for (A) depicts the case where the Claim Generator is in the same environment as user application (example Rich OS) while the diagram on the right depicts the case where the Claim Generator is running in the higher previlege execution environments like a TEE

![Singl Source Single Application](images/BasicModel.svg)
