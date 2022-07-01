Table of Contents

1. [About](#About)
2. [Get Data](#Get_Data)
3. [Email Lists and Other Forums](#Email_Lists)
4. [Developers](#Developers)


<a name="About"></a>
# 1. About

The Heliophysics Data Application Programmer's Interface (HAPI) specification is a time series download and streaming format specification. A 1-page summary is given in [HAPI_OnePager.pdf](docs/HAPI_OnePager_v4.pdf). A more detailed overview is given in the JGR article [Weigel et al., 2021](docs/Weigel_2021_HAPI-An_API_Standard_for_Accessing_Heliophysics_Time_Series_Data.pdf) and the presentation by Vandegriff et al. ([pdf](docs/HAPI_overview.pdf)\|[YouTube video](https://youtu.be/EIMIyXfpbxI)).

The HAPI specification was [recommended by COSPAR](docs/2021_COSPAR.pdf) in 2018 as the common data access API for space science and space weather data.

When data are available from a HAPI server, there is no need to download data files and write custom file reader programs. Using a HAPI client library, data can be loaded into an array using a single command using HAPI [IDL](https://github.com/hapi-server/client-idl), [Javascript](https://github.com/hapi-server/client-javascript), [Java](https://github.com/hapi-server/client-java), [MATLAB](https://github.com/hapi-server/client-matlab), and [Python](https://github.com/hapi-server/client-python) clients. Data from HAPI servers is also accessible to users of [Autoplot](http://autoplot.org/), [PySPEDAS](https://github.com/spedas/pyspedas), and [IDL SPEDAS](http://spedas.org/wiki/index.php?title=Heliophysics_Application_Programmer%E2%80%99s_Interface). Sample scripts and containing instructions for accessing data using the above--listed clients may be found by selecting a server, dataset, and time range at the web interface [http://hapi-server.org/servers/](http://hapi-server.org/servers/). 

A list of HAPI-compliant data servers is available at [http://hapi-server.org/servers/](http://hapi-server.org/servers/).

The [hapi-server GitHub project](https://github.com/hapi-server?type=all&language=&sort=name) contains a collection of repositories for HAPI--related software and documentation, including client and server libraries and code for verifying and testing a HAPI server.

<a name="Get_Data"></a>
# 2. Get Data

Use the interface at [http://hapi-server.org/servers/](http://hapi-server.org/servers/) to download data from your browser, generate \~10-line wget/curl/IDL/MATLAB/Python scripts to download data, or create preview plots.

A demonstration of using 5 different clients to access data from a HAPI server is shown in a [YouTube video](https://www.youtube.com/watch?v=dBV2yxoHkDU).

<a name="Email_Lists"></a>
# 3. Email Lists and Other Forums

* [Announcements about HAPI-related software](https://groups.io/g/hapi-news)
* [Discussion of the specification and telecon announcements](https://groups.io/g/hapi-dev)
* [Email Forum for general HAPI-related issues and questions](https://groups.io/g/hapi-help/) 
* [Github Discussions for general HAPI-related issues and questions](https://github.com/hapi-server/data-specification/discussions)

<a name="Developers"></a>
# 4. Developers

All software related to the HAPI specification is available from its [GitHub project page](https://github.com/hapi-server/). Software includes clients, servers, and a server verifier/validator.

<a name="API_and_Metadata_Specification"></a>
## 4.1 API and Metadata Specification

The HAPI specification describes a minimum set of capabilities needed for a server to allow access to the time series data values within one or more data collections.

* Current version (3.0.0): [PDF](https://github.com/hapi-server/data-specification/raw/master/hapi-3.0.0/HAPI-data-access-spec-3.0.0.pdf) \| [HTML](https://github.com/hapi-server/data-specification/blob/master/hapi-3.0.0/HAPI-data-access-spec-3.0.0.md)
* [Draft 3.1 version](https://github.com/hapi-server/data-specification/blob/master/hapi-dev/HAPI-data-access-spec-dev.md)

<a name="Client_Software"></a>
## 4.2 Client Software

Data from any [HAPI-compliant server](http://hapi-server.org/servers/) can be easily accessed using IDL, Java, MATLAB, Python, and other languages. The repositories for HAPI libraries in these languages is available [at GitHub](https://github.com/hapi-server?q=client-).

<a name="Server_Software"></a>
## 4.3 Server Software

Prior to writing server-side software, we suggest trying [the generic stand-alone HAPI server](https://github.com/hapi-server/server-nodejs). If you can generate [HAPI ASCII](https://github.com/hapi-server/data-specification/blob/master/hapi-3.0.0/HAPI-data-access-spec-3.0.0.md#data-stream-content#data-with-header) of your datasets with a command line program, you can use this server to quickly get a HAPI-compliant server running on your site.

User-contributed source code for servers in various languages is available at [at GitHub](https://github.com/hapi-server?q=server-). This contributed code is typically not up-to-date or generalized but it may be useful for getting started.

See the [server-ui](https://github.com/hapi-server/server-ui) repository for a basic server entry/overview page template for a HAPI server. Code is also available for a web interface for generating URLs to download data, plotting data from a HAPI server, and generating scripts that read and plot the selected parameter (the code used by [http://hapi-server.org/servers/](http://hapi-server.org/servers/)).

Server developers can test their server for HAPI-compliance using [the HAPI server verification service](http://hapi-server.org/verify).

<a name="Server_Developers"></a>
## 4.4 Server Developers  

If you have developed a HAPI server and it is ready for production and would like to make it automatically visible to existing software in the HAPI ecosystem, see https://github.com/hapi-server/servers