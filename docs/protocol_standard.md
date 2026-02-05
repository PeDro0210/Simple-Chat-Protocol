# Chat Protocol (ADT)

## Data Structure:
- proto-buffer (read the docs if u need them)

## Quick Overview:
- Kinda of the point for using proto-buffering is to have pretty simple data structures, that's why for each different 'method', we'll use a different 'protos' for each one of them.

- Will send the ips and the usernames, the servers will get in charge of managing them


## Unique types
  StatusEnum:
    Active = 0
    DoNotDisturb = 1
    Invisble = 2


## Simple desc


- Client sided (from client to server)
  - Message general:
    - Message: string
    - Status: StatusEnum
    - Username-origin: string
  - Registration:
    - Username: string
  - Message dm:
    - Message: string
    - Status: StatusEnum
    - Username-des: string
  - Quit:
    - Quit: 0-1

![NOTE]: Protos from the client side will always carry there IP in them, for having notion of which are they

- Server sided (from server to client)
  - All-Users:
    - Usernames: strings []
    - Status: StatusEnum []
  - For-dm:
    - Username-des: string
    - Message: string

#TODO: make protos
