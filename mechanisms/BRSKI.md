# Bootstrapping Remote Key Infrastructure (BRSKI)

 * How does device introduce itself to the infrastructure or peer?

A manufacturer certificate and trust anchor is installed in the device at build time.  During onboarding, that information is passed to a join registrar, which adds additional information and passes it to the manufacturer authorized signing authority (MASA), which then returns a voucher.

 * What, if any, proof of possession mechanism is there?

Basic BRSKI requires back-end sales integration to know if a device belongs on a particular network.

 *  What form of credential is installed into the device?

An X.509 certificate that service as a root of trust, via a voucher.

 * Is online access required for onboarding?

Yes.  The MASA is an online service.

 * Could/Is the resulting credential be used for application identity?

Yes.

 * What happens if the box gets reset?

The BRSKI process would have to be rerun.  The MASA service would be required again.

 * How can transfer of ownership occur?

 BRSKI would require that either the device consider the current LDEVID (deployment cert) as an IDEVID (manufacturer cert) or that the transfer of ownership be recorded by the MASA.

