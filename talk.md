% Remote Network Access 
% https://github.com/STL2600/remote-network-access
% ![Link to Talk](images/qr-code.png) 

VPN/Remote Access Rundown

# SSH

The old standby

## Basic Access

 - Connect to a machine
 - Forward ports
   - From local to remote
   - From remote to local

## Basic Access

 - Pros
   - Dead simple
 - Cons
   - Not very user friendly
   - TCP based connections are slow 

## Advanced Access

Who says you can't teach an old dog new tricks?

## SOCKS Proxy

`ssh -D 1337 -N user@server`

## SOCKS Proxy

 - Pros
   - Almost all network apps support SOCKS
 - Cons
   - Not very user friendly
   - TCP based connections are slow 
   - Have to configure each app to use it

## SSH VPN

Setup your tunnel

`sudo ssh -w 0:0 user@server`

## SSH VPN

 - Pros
   - Nothing to configure per app
 - Cons
   - Not very user friendly
   - TCP based connections are slow 
   - Have to configure each route manually

# Self Hosted VPN

# OpenVPN - Joe

# Wireguard

 - Creates point to point links
 - Configured using keys only
 - Can also be used as a gateway

# Wireguard

 - Pros
   - Ultra simple config, just a file
   - Secure public key based auth and encryption
   - Very fast
   - Low resource usage
   - Client usage is very simple
 - Cons
   - Not very user friendly
   - Server usage can be complicated

# Virtual Networks

## What are they

 - Also called overlay networks
 - Connect multiple machines and sites together
 - Often allows p2p direct connections
 - Designed for highly distributed networks

# Hosted Virtual Networks 

## Tailscale

 - Uses wireguard under the hood
 - Uses SSO providers for auth

## Tailscale

 - Pros
   - Very simple for both users and admins
   - Same security as Wireguard
   - Very fast
   - Low resource usage
   - Generous free tier and affordable paid options
 - Cons
   - DNS solutions are spotty

## ZeroTier

 - Uses its own encryption / auth standard, but has been reviewed
 - Supports SSO, but also usernames and passwords

## ZeroTier

 - Pros
   - Very simple for both users and admins
   - Very fast
   - Low resource usage
   - Ultra configurable
   - Self-hostable
 - Cons
   - DNS solutions are spotty
   - Free tier is less generous than others

Twingate - Joe
Pritunl - Joe
Enclave.io - Joe

# Self Hosted Virtual Network

Nebula - Joe

## Zerotier

 - Technically supported as self hosted, but does not seem to be popular

## Headscale

 - A black-box implementation of the tailscale control server
 - Must use patched clients
 - Once set up is fairly user friendly
