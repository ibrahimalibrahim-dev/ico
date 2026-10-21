UCD Production – JVM Proxy Configuration for Entra ID OIDC Authentication

Business Justification
Address the outstanding Entra ID authentication gap identified through Security assessment by configuring UCD to use the corporate proxy for OIDC communication. This change aims to restore Entra ID authentication and close the identified security gap.


Generic Description
Update the UCD production JVM proxy configuration to enable connectivity to Microsoft Entra ID for OIDC authentication. The change requires a controlled service restart, followed by authentication and deployment pipeline validation.


Pre-Release Plan
- Notify stakeholders and confirm the approved maintenance window.
- Verify UCD database backup and take a VMware snapshot.
- Back up the existing JVM configuration and record current service health.
- Confirm no active deployments are in progress.

Deployment Plan
1. Stop the UCD service.
2. Apply the agreed JVM proxy configuration.
3. Test connectivity to the Entra ID endpoint through the corporate proxy.
4. Start UCD and verify service health.
5. Test Entra ID OIDC login and validate UCD agents and representative deployment pipelines.

Rollback Plan
- If UCD fails to start, OIDC authentication remains unsuccessful, or critical functionality is impacted, restore the original JVM configuration.
- Restart UCD and verify service health and connectivity.
- If configuration rollback is unsuccessful, follow the approved recovery procedure using the available backups/snapshot.

