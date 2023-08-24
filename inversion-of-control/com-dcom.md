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

### The Problem
The most fundamental problem that COM solves is: How can a system be designed so that binary executables from different vendors, written in different parts of the world and at different times, are able to interoperate? To solve this problem, we must first find answers to these four questions:

- **Basic interoperability** How can developers create their own unique binary components, yet be assured that these binary components will interoperate with other binary components built by different developers?

- **Versioning** How can one system component be upgraded without requiring all the system components to be upgraded?

- **Language independence** How can components written in different languages communicate?

- **Transparent cross-process interoperability** How can we give developers the flexibility to write components to run in-process or cross-process, and even cross-network, using one simple programming model?

High performance is vital for component architecture. While cross-process/network transparency is valuable, in a binary component marketplace, components within the same address space must efficiently use each other's services to ensure scalability for small software pieces like C++ classes or GUI controls.

### History
One of the pioneering interprocess communication methods in Windows was **Dynamic Data Exchange (DDE)**, introduced in 1987. It enabled applications to engage in message-based "conversations." Notably, **Antony Williams**, a contributor to the creation of the COM architecture, shared key internal documents within Microsoft that laid the groundwork for software components:

- *"Object Architecture: Dealing with Unknowns, or Type Safety, in Dynamically Extensible Class Libraries,"* 1988
- *On Inheritance: The Meaning and Use of Inheritance,* 1990

These documents underpinned many concepts in COM. **Object Linking and Embedding (OLE)**, Microsoft's inaugural object-based framework, was constructed atop DDE. OLE catered specifically to compound documents, premiering in Word for Windows and Excel in 1991, eventually becoming part of Windows 3.1 in 1992.

An example of a compound document is a spreadsheet embedded within a Word for Windows document. Changes made to the spreadsheet in Excel seamlessly reflect within the Word document. In 1991, **Microsoft introduced Visual Basic Extensions (VBX)** with Visual Basic 1.0. VBX, packaged as dynamic-link libraries (DLLs), facilitated graphical arrangement and manipulation of objects using properties and methods. These were later adapted for use in languages like Visual C++.

Upon the 1992 release of Windows 3.1, Microsoft introduced **OLE 2** along with its core object model. The **COM Application Binary Interface (ABI)**, akin to the MAPI ABI (released in 1992), was built on MSRPC and, eventually, the Open Group's DCE/RPC. While OLE 1 concentrated on compound documents, COM and OLE 2 aimed to encompass software components at large.

Textual conversations and Windows messages proved too inflexible for sharing application functionality robustly and extensibly. Consequently, COM emerged as the new foundation, leading to the replacement of OLE with **OLE2**.

In 1994, **OLE Custom Controls (OCX)** succeeded VBX controls. Simultaneously, Microsoft designated OLE 2 as simply "OLE," denoting it as the collective term for all the company's component technologies. By early 1996, Microsoft expanded the utility of OLE custom controls, bolstered web browser content display, labeled Internet-related OLE components as **"ActiveX,"** and gradually rebranded its OLE technology as ActiveX.

Microsoft Office extensively employed ActiveX. In the same year, **COM was extended to network scenarios with DCOM**.


