# Simple Structure
Do not have a well defined structure. They are simple, small and limited
## MS DOS
- The interfaces and levels of functionality are not separated
- Application programs are able to access basic I/O routines causing system to crash if user programs crash


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.18 - 22.15pm.drawing",
	"width": 596,
	"aspectRatio": 1.1640625
}
```
## Traditional UNIX OS
- Consists of kernel and system programs
- Kernel separated into series of interfaces and device drivers
- Kernel provides file system, cpu scheduling, memory management, etc through system calls
# Layered approach
- OS is broken into multiple layers or levels. Layer 0 is hardware layer N is the user interface

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.18 - 22.51pm.drawing",
	"width": 650,
	"aspectRatio": 1
}
```
- Simplicity of construction and debugging
- Each level is implemented only with the operation of lower level
- Difficulty in defining the various layers
- not as efficient
# Microkernels
- Non essential components removed from kernel level
- Makes extending the OS easier

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.18 - 23.00pm.drawing",
	"width": 1066,
	"aspectRatio": 1.591044776119403
}
```

# Modules
- eg solaris
# Hybrid Systems
