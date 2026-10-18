**Status:** Tenable Nessus agent installation and service status have been verified. Pending Security team configuration to initiate the vulnerability scan, as they are the technical owners of Tenable.



**Swift Package Manager Proxy – Status Update**

Nexus Repository 3.95.0-07 has been configured with a Swift proxy to GitHub, and connectivity from the Mac build environment has been confirmed.

Testing has identified a dependency-resolution incompatibility: Tuist is attempting to clone dependencies using Git over HTTP, whereas the Nexus Swift proxy is intended for registry-based package resolution. I am validating the appropriate Tuist/SwiftPM configuration to route dependency resolution through Nexus.

**Next step:** Confirm the supported registry configuration and validate the build end-to-end through Nexus.
