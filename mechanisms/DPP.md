# Device Provisioning Protocol (DPP)
 * How does device introduce itself to the infrastructure or peer?
 
There are multiple approaches for trusted introduction, but in the first instance, DPP makes use of a *configurator*, a device that is proximate to the device to be onboarded, and contacts the peer with an 802.11 action frame.

The Configurator is the nominal "owner" of the network. It has created the policy for the
network, and it is assumed that (in the non-legacy case) the Configurator has first provisioned
the Access Point (AP) using DPP. Once the AP is provisioned it establishes the DPP network
and from then on the Configurator does DPP with clients. 
 
 * What, if any, proof of possession mechanism is there?
 
A "bootstrapping method" is used to obtain trust in a device's public key.
Different bootstrapping methods provided different levels of trust. Defined
bootstrapping methods are: QR code (good for devices that do not have a UI),
PKEX (use a shared symmetric code/key to parlay into a trusted public key,
good for devices that have at least some limited UI), NFC.

 * What form of credential is installed into the device?
 
A signed EC public key appropriate for DPP authentication (a new AKM). Also,
for support of legacy (non-DPP) networks a PSK/password/passphrase can be
provisioned.

 * Is online access required for onboarding?
 
No.

 * Who becomes the root of trust at the end of onboarding (if any)

The Configurator.

 * Could/Is the resulting credential be used for application identity?

Not directly, and not without some work/hacking. It is a DPP-network specific credential.

 * What happens if the box gets reset?

The provisioned DPP data, including the credential, are wiped. The device goes back into
a pre-provisioned state and will take part in bootstrapping again.

THis is the "Resurrecting Duckling" trust model

 * How can transfer of ownership occur?
 
Let another Configurator proceed through bootstrapping-authentication-provisioning
with the device.

 * What sort of manufacturing requirements are there?
 
Device must be have a public key generated/installed at manufacturing time. Depending
on the device the public key may have to be encoded in a QR code which is either
slapped on the backside of the device or provided in packing materials.

 * What sort of crypto requirements are there?

ECC only.

 * Reference link

[Device Provisioning Protocol Specification](https://www.wi-fi.org/downloads-registered-guest/Device_Provisioning_Protocol_Specification_v1.0.pdf/35330)
