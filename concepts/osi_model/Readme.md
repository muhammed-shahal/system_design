# What is OSI Model?

The OSI (Open Systems Interconnection) Model is a set of rules that explains how different computer systems communicate over a network. OSI Model was developed by the International Organization for Standardization (ISO). The OSI Model consists of 7 layers and each layer has specific functions and responsibilities. This layered approach makes it easier for different devices and technologies to work together.

Go to
Go to
* [Physical Layer](#layer-1-physical-layer)
* [Data Link Layer](#layer-2-data-link-layer-dll)
* [Network Layer](#layer-3-network-layer)
* [Transport Layer](#layer-4-transport-layer)
* [Session Layer](#layer-5-session-layer)
* [Presentation Layer](#layer-6-presentation-layer)
* [Application Layer](#layer-7-application-layer)

## Layer 1: Physical Layer

The lowest layer of the OSI reference model is the Physical Layer. It is responsible for the actual physical connection between the devices. The physical layer contains information in the form of bits.

* Physical Layer is responsible for transmitting individual bits from one node to the next.
* When receiving data, this layer will get the signal received and convert it into 0s and 1s and send them to the Data Link layer, which will put the frame back together.
* Common physical layer devices are Hub, Repeater, Modem, and Cables.

## Layer 2: Data Link Layer (DLL)

The data link layer is responsible for the node-to-node delivery of the message. The main function of this layer is to make sure data transfer is error-free from one node to another, over the physical layer.

* When a packet arrives in a network, it is the responsibility of the DLL to transmit it to the Host using its MAC address.
* Packet in the Data Link layer is referred to as Frame. Switches and Bridges are common Data Link Layer devices.
* The packet received from the Network layer is further divided into frames depending on the frame size of the NIC (Network Interface Card). DLL also encapsulates Sender and Receiver’s MAC address in the header.
* The Receiver’s MAC address is obtained by placing an ARP (Address Resolution Protocol) request onto the wire asking, "Who has that IP address?" and the destination host will reply with its MAC address.

## Layer 3: Network Layer

The Network Layer works for the transmission of data from one host to the other located in different networks. It also takes care of packet routing i.e. selection of the shortest path to transmit the packet, from the number of routes available.

* The sender and receiver's IP address are placed in the header by the network layer. Segment in the Network layer is referred to as Packet.
* Network layer is implemented by networking devices such as routers and switches.

## Layer 4: Transport Layer

The Transport Layer provides services to the application layer and takes services from the network layer. The data in the transport layer is referred to as Segments. It is responsible for the end-to-end delivery of the complete message.

* The transport layer also provides the acknowledgment of the successful data transmission and re-transmits the data if an error is found.
* Protocols used in Transport Layer are TCP, UDP NetBIOS, PPTP.
* At the sender's side, the transport layer receives the formatted data from the upper layers, performs Segmentation, and also implements Flow and error control to ensure proper data transmission.
* It also adds Source and Destination port number in its header and forwards the segmented data to the Network Layer.

## Layer 5: Session Layer

Session Layer in the OSI Model is responsible for the establishment of connections, management of connections, terminations of sessions between two devices. It also provides authentication and security. 

* Protocols used in the Session Layer are NetBIOS, PPTP.

## Layer 6: Presentation Layer

ThePresentation Layer is also called the Translation layer. The data from the application layer is extracted here and manipulated as per the required format to transmit over the network. Protocols used in the Presentation Layer are TLS/SSL (Transport Layer Security / Secure Sockets Layer).JPEG, MPEG, GIF, are standards or formats used for encoding data, which is part of the presentation layer’s role.

## Layer 7: Application Layer

At the very top of the OSI Reference Model stack of layers, we find the Application Layer which is implemented by the network applications. These applications produce the data to be transferred over the network.

* This layer also serves as a window for the application services to access the network and for displaying the received information to the user.
* Protocols used in the Application layer are SMTP, FTP, DNS, etc.

## How Data Flows in the OSI Model?
When we transfer information from one device to another, it travels through 7 layers of OSI model. First data travels down through 7 layers from the sender's end and then climbs back 7 layers on the receiver's end. Data flows through the OSI model in a step-by-step process:

- Application Layer: Applications create the data.
- Presentation Layer: Data is formatted and encrypted.
- Session Layer: Connections are established and managed.
- Transport Layer: Data is broken into segments for reliable delivery.
- Network Layer: Segments are packaged into packets and routed.
- Data Link Layer: Packets are framed and sent to the next device.
- Physical Layer: Frames are converted into bits and transmitted physically.