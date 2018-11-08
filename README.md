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


## DPP

## WPA2-PSK

## Hotspot 2.0 OSU

## EAP-NOOB


## Basic BRSKI
### How does device introduce itself to the infrastructure or peer?

A manufacturer certificate and trust anchor is installed in the device at build time.  During onboarding, that information is passed to a join registrar, which adds additional information and passes it to the manufacturer authorized signing authority (MASA), which then returns a voucher.

### What, if any, proof of possession mechanism is there?

Basic BRSKI requires back-end sales integration to know if a device belongs on a particular network.

### What form of credential is returned?

An X.509 certificate via a voucher.

### Is online access required for onboarding?

Yes.  The MASA is an online service.

### Could/Is the resulting credential be used for application identity?

Yes.

### What happens if the box gets reset?

The BRSKI process would have to be rerun.  The MASA service would be required again.

### How can transfer of ownership occur?

 BRSKI would require that either the device consider the current LDEVID (deployment cert) as an IDEVID (manufacturer cert) or that the transfer of ownership be recorded by the MASA.


## Zigbee

## Bluetooth
