---
id: Network Models
aliases: []
tags: []
---

# Layered Tasks

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.21 - 21.24pm.drawing",
	"width": 1110,
	"aspectRatio": 1.5948275862068966
}
```

# OSI model
- Open Systems Interconnections
- Introduced in 1970s

## Layers
1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application
### Exchange using OSI model

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.21 - 23.40pm.drawing",
	"width": 1204,
	"aspectRatio": 1.4956521739130435
}
```

- Physical Layer send the bits
- Data link moves frame from one node to another
	- Frames contain | MAC1 | MAC2 | IP1 IP2 | Segment | Tail|
	- IP1 IP2 and Segment comes from physical layer
- Network layer is responsible for delivery of individual packets
- Transport layer is responsible for delivery of message from one process to another
- Session layer is responsible for dialog control and sync
- Presentation layer is responsible for translation, compression and encryption
- Application layer responsible for providing service to the user
## Adresses
- Physical -> Data Link and Physical
- Logical -> Network
- Port -> Transport
- Specific -> Application