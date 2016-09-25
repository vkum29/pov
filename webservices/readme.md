# Web services

<del> is a service which just handles a request and response via a specific language JSON/XML. </del>

Web services are the services provided by an electronic device to another electronic device. Which enables their communication over WWW.
<del>This is enabled by using HTTP service which was originally used for machine to human communication and transfer of data via XML or JSON.</del>
The data transfer in form of RSS, POX(Plain old XML), JSON, etc.

Web services are implemented in various ways(like SOAP or RESTFUL API or oDATA) and with various protocols (FTP, SMTP, HTTP).

## SOAP - Simple Object Access Protocol

Soap relied on POX or other XMLs for its implementation.
Requires WSDL (Web Service Description Language - an XML describing the data structure of SOAP API request and response).
This is used by consumer to understand the implementation need for consuming this web service.

Typically  a client gets WSDL creates its functions to access properties and methods provided by API and passes the required data/params.

Server on other hand receives this request and returns the data in either XML or JSON as requested.
