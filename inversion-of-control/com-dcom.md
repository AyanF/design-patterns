### What is COM?
Microsoft's component program architecture, COM (Component Object Model), was mainly designed for Windows. It is the basis upon which OLE and ActiveX are built, and it allows code to be reused without being recompiled. A component in COM is a platform-specific binary file that conforming apps and other components can use.

Instead of having access to a component's underlying data structure, programmes that use its services include pointers to its standardised interface. As a result, components can communicate with one another regardless of how they work or what language they're written in.

COM programmers use COM-aware components to create their applications. Class IDs (CLSIDs), which are Globally Unique Identifiers, are used to identify different component kinds (GUIDs). Each COM component has one or more interfaces that expose its capabilities. Interface IDs (IIDs), also GUIDs, are used to distinguish between the many interfaces supported by a component.


