# Catalog of Onboarding Mechanisms for IoT Devices

When considering each of these technologies, provide one or two sentences on what problem each sets out to solve, a few sentences on how it solves that problem, and then talk about constraints.  Keep in mind our goal for seeking common architectural components.  Some leading questions to help:

 * How does device introduce itself to the infrastructure or peer?
 * What, if any, proof of possession mechanism is there?
 * What form of credential is returned?
 * Is online access required for onboarding?
 * Who becomes the root of trust at the end of onboarding (if any)
 * Could/Is the resulting credential be used for application identity?
 * What happens if the box gets reset?
 * How can transfer of ownership occur?
 * What sort of manufacturing requirements are there?
 * What sort of crypto requirements are there?
 * Reference link

Feel free to add or vary the questions.


## Device Provisioning Protocol (DPP)
 * How does device introduce itself to the infrastructure or peer?
 
There are multiple approaches for trusted introduction, but in the first instance, DPP makes use of a *configurator*, a device that is proximate to the device to be onboarded, and contacts the peer with an action frame /* Dan to check this */
 
 * What, if any, proof of possession mechanism is there?
 
An asymmetric key that is provided, at least initially, with a QR code.

 * What form of credential is returned?
 
A key appropriate for DPP authentication (a new AKM).

 * Is online access required for onboarding?
 
No.

 * Who becomes the root of trust at the end of onboarding (if any)

The device leverages the QR code as proof of trust.  This binds the device to the network for onboarding, but that is the full extent of it.

 * Could/Is the resulting credential be used for application identity?

Probably not.

 * What happens if the box gets reset?

The owner can use the configurator again, so long as either it has stored the original QR code *or* the original QR code is available on a label.

 * How can transfer of ownership occur?
 
Provide the QR code to the new owner.

 * What sort of manufacturing requirements are there?
 
Device must be aware of its private key, and the QR code must be printed somewhere.

 * What sort of crypto requirements are there?


 * Reference link

https://www.wi-fi.org/downloads-registered-guest/Device_Provisioning_Protocol_Specification_v1.0.pdf/35330

## WPA2-PSK

## Hotspot 2.0 OSU

## EAP-NOOB

## BRSKI-CoAP-EST

## Template-Based Reprovisioning

### Template Re-Provisioning via EAP

## Basic CMP (RFC 4210)

## Basic BRSKI

 * How does device introduce itself to the infrastructure or peer?

A manufacturer certificate and trust anchor is installed in the device at build time.  During onboarding, that information is passed to a join registrar, which adds additional information and passes it to the manufacturer authorized signing authority (MASA), which then returns a voucher.

 * What, if any, proof of possession mechanism is there?

Basic BRSKI requires back-end sales integration to know if a device belongs on a particular network.

 *  What form of credential is returned?

An X.509 certificate via a voucher.

 * Is online access required for onboarding?

Yes.  The MASA is an online service.

 * Could/Is the resulting credential be used for application identity?

Yes.

 * What happens if the box gets reset?

The BRSKI process would have to be rerun.  The MASA service would be required again.

 * How can transfer of ownership occur?

 BRSKI would require that either the device consider the current LDEVID (deployment cert) as an IDEVID (manufacturer cert) or that the transfer of ownership be recorded by the MASA.

## Wi-SUN (version 1)

 * How does device introduce itself to the infrastructure or peer?
 
 EAP-TLS
 
 * What, if any, proof of possession mechanism is there?
 
 
 
 * What form of credential is returned?
 
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
 
 /* need answer */
 
 * What sort of manufacturing requirements are there?
 
 Certificate/trust anchor installation.
 
 * What sort of crypto requirements are there?
 
/* Need answer: RSA or ECC */
 
 * Reference link

Spec not publsihed but see https://tools.ietf.org/id/draft-heile-lpwan-wisun-overview-00.html.
## Zigbee

## Bluetooth
