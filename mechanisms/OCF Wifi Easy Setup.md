# OCF WiFi Easy Setup

 * How does device introduce itself to the infrastructure or peer?

The device starts as a SoftAP, and so advertises WiFi beacons.

 * What, if any, proof of possession mechanism is there?

Physical proximity can be established using a random PIN based mechanism, where the PIN
is communicated over an out-of-band channel (e.g., displayed to a human).  See 
Section 7.3.5 of the 
[OCF Security Specification](https://openconnectivity.org/specs/OCF_Security_Specification_v1.3.0.pdf).

 * Is access to other IP-based devices required in order to fully onboard the device?

No.

 * What form of credential is returned?

Such information includes L2 credentials
(e.g., WiFi SSID and key), as well as the owner's cert, and optionally a cloud service
URI and credentials needed to sign into it.

 * Is full Internet access required for onboarding?

No, onboarding happens prior to getting IP connectivity.
Onboarding can thus be used to provision credentials needed to get network access.

 * Who becomes the root of trust at the end of onboarding (if any)

The new owner's certificate becomes the root of trust.

 * Could/Is the resulting credential be used for application identity?

The question is bad because "the" assumes that onboarding only provisions one thing.
Application identity can be provisioned along with L2 credentials, which may be different.

 * What happens if the box gets reset?

A factory reset will typically remove all credentials, leaving the device ready to be
onboarded again.

 * How can transfer of ownership occur?

There are multiple mechanisms specified in Section 7.3 of the 
[OCF Security Specification](https://openconnectivity.org/specs/OCF_Security_Specification_v1.3.0.pdf)).
In general, before the device is put onto the network, the new owner's certificate
is provisioned into the device so that by the time the device gets access to the
regular network, it is already fully configured with all security credentials.

 * How can transfer to a different cloud service (if applicable) occur?

Subsequent ownership transfer can happen either by doing a factory reset and starting from scratch,
or by following an ownership transfer mechanism that is not part of onboarding,
and hence outside the scope of this survey.

 * What sort of manufacturing requirements are there?

The manufacturer is responsible for adding code complying with the specification.
Optionally, the manufacturer can also provision a manufacturer's certificate
of device authenticity (see Section 7.3.6 of the 
[OCF Security Specification](https://openconnectivity.org/specs/OCF_Security_Specification_v1.3.0.pdf))

 * What sort of crypto requirements are there?

Several different mechanisms are defined, with varying levels of crypto requirements,
so that the WiFi Easy Setup can be used by a wide variety of devices.

 * Reference link

[OCF WiFi Easy Setup](https://openconnectivity.org/specs/OCF_Core_Specification_Extension_Wi-Fi_Easy_Setup_v1.3.0.pdf)

[OCF Security Specification](https://openconnectivity.org/specs/OCF_Security_Specification_v1.3.0.pdf)

