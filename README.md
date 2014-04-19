Neo4j 2.0.0 test database
=======================================

This is a Neo4j 2.0.0 community edition graph database, with Micheal Hunger's
[neo4j-in-memory-server](https://github.com/jexp/neo4j-in-memory-server)
installed and the configuration modified to start the rest server on port
7373 and the https version on port 7272.

This means that

1. Tests should run faster, since the graph is only stored in memory.
2. The test server will use more memory than the ordinary server would for the same data set.
3. Data is lost when the server is stopped.
4. Your test server can be kept running alongside an out-of-the-box neo4j dev server.

Quick Start
-----------

    git clone https://github.com/loop-recur/neo4j-test-server.git
    neo4j-test-server/bin/neo4j start

Then connect to your test db at `localhost:7373` in your test suite.

In the box
----------

Neo4j runs as a server application, exposing a Web-based management
interface and RESTful endpoints for data access.

Here in the installation directory, you'll find:

* bin - scripts and other executables
* conf - server configuration
* data - database, log, and other variable files
* doc - more light reading
* lib - core libraries
* plugins - user extensions
* system - super-secret server stuff

Make it go
----------

For full instructions, see http://docs.neo4j.org/chunked/2.0.0/deployment.html

To get started with Neo4j, let's start the server and take a
look at the web interface ...

1. Open a console and navigate to the install directory.
2. Start the server:
   * Windows: use bin\Neo4j.bat
   * Linux/Mac: use ./bin/neo4j console
3. In a browser, open http://localhost:7373/
4. From any REST client or browser, open http://localhost:7373/db/data
   in order to get a REST starting point, e.g.
   curl -v http://localhost:7373/db/data
5. Shutdown the server by typing Ctrl-C in the console.

Learn more
----------

Out on the internets, you'll find:

* Neo4j Home: http://www.neo4j.org/
* Getting Started: http://docs.neo4j.org/chunked/2.0.0/introduction.html
* The Neo4j Manual (online): http://docs.neo4j.org/chunked/2.0.0/

License(s)
----------
Various licenses apply. Please refer to the LICENSE and NOTICE files for more
detailed information.

