### What is COM?
Microsoft's component program architecture, COM (Component Object Model), was mainly designed for Windows. It is the basis upon which OLE and ActiveX are built, and it allows code to be reused without being recompiled. A component in COM is a platform-specific binary file that conforming apps and other components can use.

Instead of having access to a component's underlying data structure, programmes that use its services include pointers to its standardised interface. As a result, components can communicate with one another regardless of how they work or what language they're written in.

COM programmers use COM-aware components to create their applications. Class IDs (CLSIDs), which are Globally Unique Identifiers, are used to identify different component kinds (GUIDs). Each COM component has one or more interfaces that expose its capabilities. Interface IDs (IIDs), also GUIDs, are used to distinguish between the many interfaces supported by a component.

### What is DCOM?
DCOM is a programming technique that allows a computer to run programmes on a remote computer as if they were running locally. The Distributed Component Object Model (DCOM) is an acronym for Distributed Component Object Model. It is a software component that enables COM objects to communicate over the network.

DCOM is an extension of COM that addresses a few issues with the COM model to make it more beneficial over a network −

**Marshalling** − Marshalling solves the problem of delivering data from one COM object instance to another on a different machine; in programming words, this is referred to as "passing arguments."

**Distributed Garbage Collection** − Designed to scale DCOM to handle high-volume internet traffic, Distributed Garbage Collection also includes a mechanism for deleting and reclaiming completed or abandoned DCOM objects, preventing web server memory from being blown up. It then communicates with the other servers in the transaction chain, informing them that the transaction's objects are available for deletion.

**DCE/RPC is used as the underlying RPC mechanism** − Microsoft built DCE/RPC as the underlying technology for DCOM – where the D in DCOM comes from – to achieve the goals mentioned earlier attempt to scale to support a significant volume of web traffic.
