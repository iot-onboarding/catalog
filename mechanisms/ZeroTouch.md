# SZTP

  * How does device introduce itself to the infrastructure or peer? 

    The device can use a variety of mechanisms to find a source of bootstrapping
    information, including: multicast DNS, unicast DNS, DHCP, well-known Internet
    service, and removable storage.  The ultimate goal is for the to reach out to
    these potential sources of bootstrapping information until it finds one that
    it can use to locate a bootstrap server.

  * What, if any, proof of possession mechanism is there?

    SLAs within the bootstrap server and/or voucher issuance can attest to the
    level back-end sales integration. Also, the device can prompt the installer
    to enter a code in addition to or instead of using client certificate
    based authentication.

 * Is access to other IP-based devices required in order to fully onboard the device?

    Required, no.  Possible, yes.

 *  What form of credential is installed into the device?

    Devices SHOULD have an X.509 certificate (ideally an IDevID).  Devices MAY
    alternatively (or in addition to) prompt for HTTP auth credentials.

 * Is full Internet access required for onboarding?

   No, vouchers may be obtained offline.  In the most extreme case, the entire
   bootstrapping process can transpire off of a removable storage device (flash
   drive) without any network activity at all.

 * Who becomes the root of trust at the end of onboarding (if any)

   Up to the bootstrapping process, but generally, the idea is to transfer
   ownership of the device to its rightful owner.

 * Could/Is the resulting credential be used for application identity?

   Yes.

 * What happens if the box gets reset?

   Simply rebooting does not necessitate rerunning the bootstrapping protocol
   (unless the device is designed require such).  Resetting the device to factory
   default would, of course, necessitate rerunning the bootstrapping protocol.

 * How can transfer of ownership occur?

   Up to the policies put in place by the MASA.  Some MASA's may require the
   previous owner "release" possession before assigning ownership to another
   entity, or perhaps insist on backend-sales integration.  Other MASAs (e.g.,
   for less secure devices), may have less demanding requirements.  

   FWIW, SZTP is more concerned with the protocol touching the device than
   any backend processes, leaving these open to definition by others over
   time.

 * How can transfer to a different cloud service (if applicable) occur?

   SZTP defines an explicit "redirect" message to allow for such transfers.

 * What sort of manufacturing requirements are there?

   Depends entirely on what bootstrapping strategies the device supports
   and how secure it wishes to be.  Please see Section 5.1 in
   draft-ietf-netconf-zerotouch for details.

 * What sort of crypto requirements are there?

   Depends entirely on what bootstrapping strategies the device supports
   and how secure it wishes to be.  Please see Section 5.1 in
   draft-ietf-netconf-zerotouch for details.


 * Reference link

   https://tools.ietf.org/html/draft-ietf-netconf-zerotouch
