# AllJoyn Onboarding

 * How does device introduce itself to the infrastructure or peer?

The device starts as a SoftAP, and so advertises WiFi beacons, using an SSID that either starts with AJ\_
or ends with \_AJ.

 * What, if any, proof of possession mechanism is there?

A QR code can be used to provide proof of possession of the device.

 * Is access to other IP-based devices required in order to fully onboard the device?

No.

 * What form of credential is installed into the device?

Such information minimally includes L2 credentials
(WiFi SSID and key), and typically ownership transfer is done at the same time, before a
device is put on the regular WiFi network, such that the device is provisioned with the
owner's cert and a certificate of owner-allowed device capabilities.

 * Is full Internet access required for onboarding?

No.

 * Who becomes the root of trust at the end of onboarding (if any)

The new owner's certificate becomes the root of trust.

 * Could/Is the resulting credential be used for application identity?

The question is bad because "the" assumes that onboarding only provisions one thing.
Application identity can be provisioned along with L2 credentials, which may be different.

 * What happens if the box gets reset?

A factory reset will typically remove all credentials, leaving the device ready to be
onboarded again.

 * How can transfer of ownership occur?

Ownership transfer is described in 
[AllJoyn Security 2.0](https://web.archive.org/web/20170730231028/http://allseenalliance.org/framework/documentation/learn/core/security2_0/hld).
In general, before the device is put onto the network, the new owner's certificate
is provisioned into the device so that by the time the device gets access to the
regular network, it is already fully configured with all security credentials.

 * How can transfer to a different cloud service (if applicable) occur?

Not applicable (not tied to a cloud service).

 * What sort of manufacturing requirements are there?

The QR code must be printed somewhere.

 * What sort of crypto requirements are there?

Uses X.509 certificates.
Uses ECDHE\_ECDSA, or ECDHE\_PSK, or ECDHE\_NULL for key exchange.

 * Reference link

[AllJoyn Onboarding Framework Interface Definition](https://web.archive.org/web/20170924015202/https://allseenalliance.org/framework/documentation/learn/base-services/onboarding/interface)

[AllJoyn Security 2.0](https://web.archive.org/web/20170730231028/http://allseenalliance.org/framework/documentation/learn/core/security2_0/hld)
