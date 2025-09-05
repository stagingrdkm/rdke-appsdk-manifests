# rdk-appsdk-manifests
This repo is staging area and first stop for new AppSDK, exact name TBD, also tentatively named  new Firebolt native App SDK, DAC2.0 SDK.

This repository contains several repo manifests with applications and runtimes that can be build with App SDK 
Their build output, their binaries should be able to run on any Firebolt2 compliant RDK7+/RDK8 devices with AppInfra2.0  

A particular manifests typically points to :  
   -the meta-layers of the App SDK (that include the base layer in binary or source).
   -the meta-layer for the particular app or runtime. 
   -together it allows to successfully build the particular app or runtime layer with the Yocto App SDK.

The meta-layer of the App SDK are :  
https://github.com/stagingrdkm/meta-rdke-appsdk-base-dev (source version of base layer)  
https://github.com/stagingrdkm/meta-rdke-appsdk-base-rel (binary release version of base layer, not created yet)  
https://github.com/stagingrdkm/meta-rdke-appsdk-distro  

/app/ contain manifests for apps per appname and associated company, organisation maintaining them.

/runtime/{runtimename}/rel will contain official release versions of "RDK runtimes" maintained and released by RDK-M team. 
   It also allows and encourgages other companies to share their version or updates of existing RDK runtimes or share new runtimes.
   Allowing exact build replication and auto-publishing in Appstore for Video Accelerators

/base/rel/ will contain official release versions of "base-layer" source manifest. Version and content is controlled by RDK Native App Working Group.  
  The AppSDK will come with prebuild profiles of this base-layer version and SDK toolchain export in /sdk-export.  
  This versioned manifest allows exact replication of that binary version from sources with the AppSDK
  The base.dev.xml is the "next" version that is still under development, not garanteed to be fixed versioned. 

For directory and file naming convention see https://github.com/stagingrdkm/rdke-appsdk-manifests/blob/develop/sdk-naming-conventions.txt

