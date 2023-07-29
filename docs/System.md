# System Help

Get system metrics.<br/><br/>Most commands work on all OSes or omit certian information.<br/>See the help for individual commands for detailed limitations.

# systeminfo
 - Usage: `?systeminfo `



# system
 - Usage: `?system `

Get information about your system metrics.<br/><br/>Most commands work on all OSes or omit certian information.<br/>See the help for individual commands for detailed limitations.

## system processes
 - Usage: `?system processes `
 - Aliases: `proc`

Get an overview of the status of currently running processes.<br/><br/>Platforms: Windows, Linux, Mac OS

## system cpu
 - Usage: `?system cpu `

Get metrics about the CPU.<br/><br/>This will show the CPU usage as a percent for each core, and frequency depending on<br/>platform.<br/>It will also show the time spent idle, user and system as well as uptime.<br/><br/>Platforms: Windows, Linux, Mac OS<br/>Note: CPU frequency is nominal and overall on Windows and Mac OS,<br/>on Linux it's current and per-core.

## system all
 - Usage: `?system all `
 - Aliases: `overview and top`

Get an overview of the current system metrics, similar to `top`.<br/><br/>This will show CPU utilisation, RAM usage and uptime as well as<br/>active processes.<br/><br/>Platforms: Windows, Linux, Mac OS<br/>Note: This command appears to be very slow in Windows.

## system uptime
 - Usage: `?system uptime `
 - Aliases: `up`

Get the system boot time and how long ago it was.<br/><br/>Platforms: Windows, Linux, Mac OS

## system mem
 - Usage: `?system mem `
 - Aliases: `memory and ram`

Get infomation about memory usage.<br/><br/>This will show memory available as a percent, memory used and available as well<br/>as the total amount. Data is provided for both physical and SWAP RAM.<br/><br/>Platforms: Windows, Linux, Mac OS

## system users
 - Usage: `?system users `

Get information about logged in users.<br/><br/>This will show the user name, what terminal they're logged in at,<br/>and when they logged in.<br/><br/>Platforms: Windows, Linux, Mac OS<br/>Note: PID is not available on Windows. Terminal is usually `Unknown`

## system network
 - Usage: `?system network `
 - Aliases: `net`

Get network stats. They may have overflowed and reset at some point.<br/><br/>Platforms: Windows, Linux, Mac OS

## system red
 - Usage: `?system red `

See what resources JuiceBot is using.<br/><br/>Platforms: Windows, Linux, Mac OS<br/>Note: SWAP memory information is only available on Linux.

## system disk
 - Usage: `?system disk [ignore_loop=True] `
 - Aliases: `df`

Get infomation about disks connected to the system.<br/><br/>This will show the space used, total space, filesystem and<br/>mount point (if you're on Linux make sure it's not potentially<br/>sensitive if running the command a public space).<br/><br/>If `ignore_loop` is set to `True`, this will ignore any loop (fake) devices on Linux.<br/><br/>Platforms: Windows, Linux, Mac OS<br/>Note: Mount point is basically useless on Windows as it's the<br/>same as the drive name, though it's still shown.

## system sensors
 - Usage: `?system sensors [fahrenheit=False] `
 - Aliases: `temp, temperature, fan, and fans`

Get sensor metrics.<br/><br/>This will return any data about temperature and fan sensors it can find.<br/>If there is no name for an individual sensor, it will use the name of the<br/>group instead.<br/><br/>Platforms: Linux

