# Wi-SUN (version 1)

 * How does device introduce itself to the infrastructure or peer?
 
 EAP-TLS
 
 * What, if any, proof of possession mechanism is there?
 
 Infra is expected to have list of registered devices.
 
 * What form of credential is installed into the device?
 
 Devices run off of manufacturer certs.
 
 * Is online access required for onboarding?
 
 No
 
 * Who becomes the root of trust at the end of onboarding (if any)
 
 Trust is manually configured.
 
 * Could/Is the resulting credential be used for application identity?
 
 Yes (but it is the manufacturer certificate).
 
 * What happens if the box gets reset?
 
 You still use the manufacgturer certificate.
 
 * How can transfer of ownership occur?
 
Not specified in standard.  In v1, device accepts cert.
 
 * What sort of manufacturing requirements are there?
 
 Certificate/trust anchor installation.
 
 * What sort of crypto requirements are there?
 
 TLS\_ECDHE\_ECDSA\_WITH\_AES\_128\_CCM\_8 as MTI.
 
 * Reference link

Spec not publsihed but see https://tools.ietf.org/id/draft-heile-lpwan-wisun-overview-00.html.
