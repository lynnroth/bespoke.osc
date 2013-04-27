Created by [Paul Varcholik](http://www.bespokesoftware.org/)

# Overview

"Open Sound Control (Osc) is an open, transport-independent, message-based protocol developed for communication among computers, sound synthesizers, and other multimedia devices." (from [http://opensoundcontrol.org/spec-1_0](http://opensoundcontrol.org/spec-1_0))

There are a number of Osc implementations, including [another in C#](http://opensoundcontrol.org/implementation/osc-net-v1-2), but I decided to roll my own and make it freely available. This implementation sits atop the .NET 4.5 Framework and uses TCP or UDP as the transport protocol. It includes support for Osc Messages and Bundles, and supports the following payload data types:

* Int32
* Int64
* Float
* Double
* String
* Blob (byte array)
* Osc TimeTag
* ASCII character
* boolean
* Nil
* Infinitum
* RGBA color

The [OscServer](http://www.bespokesoftware.org/OSC/2.0/doc/html/c2be67f6-fc7a-4621-70aa-4045be8a977d.htm) class is at the heart of the system, and includes support for unicast, broadcast, and multicast. As Osc packets, bundles, and messages are received corresponding events are fired. Additionally, the system will (optionally) filter Osc address patterns that the user registers.

The package includes simple client and server examples in both C# and Visual Basic.NET.

# Documentation

[Online Documentation](http://www.bespokesoftware.org/OSC/2.0/doc)

# License

[Microsoft Public License (MS-PL)](http://www.opensource.org/licenses/ms-pl.html)