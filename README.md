# packet-simplemessage

## Overview

This is a Wireshark Lua dissector for the ROS Industrial SimpleMessage 
protocol. For more information on the protocol, see [simple_message][]. The 
current version of the dissector supports only the 'groovy' version of 
SimpleMessage.

Packet types dissected:

 * Ping
 * Joint Position
 * Joint Trajectory Point
 * Joint Trajectory Point Full
 * Status
 * Joint Feedback
 * Motoman Motion Control
 * Motoman Motion Reply

Tested on Wireshark 1.9.0-SVN-46273 on Windows, but should work on other 
version and OS as well.


## Installation

Make sure the version of Wireshark you have installed was compiled with Lua 
support (see [wireshark.org/Lua][]).

### Linux (per user)

    cd $PACKET_SIMPLEMESSAGE
    mkdir -p ~/.wireshark/plugins
    cp packet-simplemessage.lua ~/.wireshark/plugins

### Windows (per user)

Open `%USERPROFILE%\AppData\Roaming` (Win7) or `%USERPROFILE%\Application Data` 
(WinXP) and open the `Wireshark\plugins` folder (if it doesn't exist, create 
it). Now copy `packet-simplemessage.lua` to the `plugins` folder.


## Bugs, feature requests, etc

Please use the [GitHub issue tracker][].



[simple_message]: http://ros.org/wiki/simple_message
[wireshark.org/Lua]: http://wiki.wireshark.org/Lua
[GitHub issue tracker]: https://github.com/gavanderhoorn/packet-simplemessage/issues