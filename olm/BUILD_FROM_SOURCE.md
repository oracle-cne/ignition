# Build from source changes
The upstream spec file is not included in the CoreOS Ignition Github repository. It is separately maintained here: https://src.fedoraproject.org/rpms/ignition. Because it is a separate entity, the spec file refers to the Ignition source code at an HTTP endpoint, so we modify the spec file to use the source in this repository.

There is also an ignition-edge source tar that is referenced via an HTTP endpoint. We download the tar file and check it into source control, and then modify the spec file "Source" to reference the local file.

We also add two patch files for adding OCI support to Ignition, as well as copy SECURITY.md and THIRD_PARTY_LICENSES.txt to the RPM.