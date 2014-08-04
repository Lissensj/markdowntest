####About

This is a page about a thought experiment with as goal the creation of a simplified (Qeo-alike?) API on top of the AllJoyn API.

#####The Prototype

More information on the prototype can be found at following locations:

* [Git repository|http://gitolite.edegem.eu.thmulti.com/cgit/pub/verbeeck/ajnqeo-c-chat.git/]
** */include* contains the API header files
** */lib* contains the API implementation
** */src* contains the simple chat test application
** */gen* contains the (to be) generated code for the application
* [Doxygen documentation|http://isf.edegem.eu.thmulti.com/~verbeeck/ajnqeo-c/]

Note:

Oh yeah... only builds in Eclipse for now :).

######Concept mapping

||Qeo prototype||AllJoyn||
|Service (ajnqeo_service_t)|BusAttachment|
|Interface (ajnqeo_intf_t)|Interface definition|
|Writer (ajnqeo_writer_t)|Caching multi-instance interface implementation (server side)|
|Reader (ajnqeo_reader_t)|Caching multi-instance interface implementation (client side)|
|Instance (ajnqeo_instance_t)|BusObject (server side)\\ \\

ProxyBusObject (client side)|

######Disclaimer

* Session setup between two peers is available.  Session setup between multiple peers is possible using similar code as from the Java prototype (but not implemented).
* No caching has been implemented in the reader or writer.  A mechanism as available in the Java prototype is possible.
* Error handling is mostly done using asserts.  This will cause program abortion if anything goes wrong.  A lot of sanity checks are not in place.
* Currently only string and integer types are supported.  Nested structures are only available as properties (as a proof-of-concept).

#####AllJoyn C API Remarks

######Header file/API issues

* *Session.h* and *TransportMask.h* contain global variables.  Including these files in different sources files triggers linking errors (double symbols).  Should be changed to *#define*s or *extern*s.

* *alljoyn_busobject_signal*, *alljoyn_busattachment_registersignalhandler* and others expect an argument of type *alljoyn_interfacedescription_member* (a structure) which is passed by value.  This causes the structure to be copied on the stack.  Should be changed to an argument which is a pointer to that structure.

* The C++ method *MsgArg::SetOwnershipFlags()* is not available in the C API.  As a result the destruction of complex dynamic data (msgarg) structures requires a lot of recursion.

######Nested structures

In DBus property signatures it is possible to have very complex types (e.g. nested structures).  This is defined as "(...)" where the ellipsis is replaced by the signatures of the individual structure fields.  The problem with this approach is that no names for those fields are available anywhere; i.e. they are anonymous.  It is not possible to map this easily onto a real C structure with named fields.  A more high level interface (or type) description as used in the prototype alleviates this problem (see *ajnqeo_intf_desc_t*).

######Signal and method handlers

When registering a signal handler using *alljoyn_busattachment_registersignalhandler* it is not possible to specify some kind of context (or cookie) that is alter on passed to the actual handler.  This prevents a clean implementation of a more generic mechanism for signal handling.  The current prototype keeps track of the context information in a global variable (only a single is supported).  This makes for more complex management code when multiple signal handlers are needed.

Something similar is true for method handlers.