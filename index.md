1. [About](#About)
2. [Get Data](#Get_Data)
3. [Email Lists](#Email_Lists)
4. [Developers](#Developers)

<a name="About"></a>
# 1. About

The Heliophysics Data Application Programmer's Interface (HAPI) specification is a time series download and streaming format specification.

When data are available from a HAPI server, there is no need to download data files and write custom file reader programs. Using a HAPI client library, data can be loaded into an array using a single command in IDL, MATLAB, and Python.

A list of HAPI-compliant data servers is available at [http://hapi-server.org/servers/](http://hapi-server.org/servers/).

The GitHub project [hapi-server](http://github.com/hapi-server/) contains a collection of HAPI-related software and documentation, including client and server libraries and code for verifying and testing a HAPI server.

<a name="Get_Data"></a>
# 2. Get Data

Use the interface at [http://hapi-server.org/servers](http://hapi-server.org/servers/) to download data from your browser, generate \~10-line IDL/MATLAB/Python scripts to download data, and create preview plots.

<a name="Email_Lists"></a>
# 3. Email Lists

* [Annoucements about HAPI-related software](http://lists.igpp.ucla.edu/mailman/listinfo/hapi-news)
* [Discussion of the specification and telecon annoucements](http://lists.igpp.ucla.edu/mailman/listinfo/hapi-dev)

<a name="Developers"></a>
# 4. Developers

<a name="API_and_Metadata_Specification"></a>
## 4.1 API and Metadata Specification

The HAPI specification describes a minimum set of capabilities needed for a server to allow access to the time series data values within one or more data collections.

* Current version (2.1.1): [PDF](https://github.com/hapi-server/data-specification/raw/master/hapi-2.1.0/HAPI-data-access-spec-2.1.0.pdf) | [HTML](https://github.com/hapi-server/data-specification/blob/master/hapi-2.1.0/HAPI-data-access-spec-2.1.0.md)
* [Draft 3.0 version](https://github.com/hapi-server/data-specification/blob/master/hapi-dev/HAPI-data-access-spec-dev.md)

<a name="Client_Software"></a>
## 4.2 Client Software

Data from any [HAPI-compliant server](http://hapi-server.org/servers/) can be easily accessed using IDL, Java, MATLAB, Python, and other languages. The repositories for HAPI libraries in these languages is available [at GitHub](https://github.com/hapi-server?q=client-).

<a name="Server_Software"></a>
## 4.3 Server Software

Prior to writing server-side software, we suggest trying [the generic stand-alone HAPI server](https://github.com/hapi-server/server-nodejs). If you can generate [HAPI ASCII](https://github.com/hapi-server/data-specification/blob/master/hapi-2.1.0/HAPI-data-access-spec-2.1.0.md#data-stream-content#data-with-header) of your datasets with a command line program, you can use this server to quickly get a HAPI-compliant server running on your site.

User-contributed source code for servers in various languages is available at [at GitHub](https://github.com/hapi-server?q=server-). This contributed code is typically not up-to-date or generalized but it may be useful for getting started.

See the [server-ui](https://github.com/hapi-server/server-ui) repoistory for a basic server entry/overview page template for a HAPI server. Code is also available for a web interface for generating URLs to download data, plotting data from a HAPI server, and generating scripts that read and plot the selected parameter (the code used by [http://hapi-server.org/servers/](http://hapi-server.org/servers/)).

Server developers can test their server for HAPI-compliance using [the HAPI server verification service](http://hapi-server.org/verify).
