# GC Infrastructure Lab Architecture

## Management Plane

OPNsense provides routing and firewall services for the lab.

The managment network is:

- Network: 10.10.10.0/24
- Gateway: 10.10.10.1
- Hyper-V switch: GC-Lab-MGMT

gc-mgmt01 is the management and automation server.

## Target Management Access

gc-mgmt is temporarily connected ot the home network for bootstrap access.

The target design is:

WSL -> VPN -> OPNsense -> GC-Lab-MGMT -> gc-mgmt01

After VPN access is validated, the external NIC will be removed from gc-mgmt01.
