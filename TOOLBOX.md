# Toolbox
This is a list of tools I use and is comfortable with. The idea with keeping track of which tools I use is so that I can keep using the same tools and ultimately master them.

The difference between the toolbox and list of skills is that here can can list more granular libraries, for example Kryo is in the toolbox but is not necessarily considered a "skill". I don't need to know everything about each tool in the box, just enough for my use cases. We should strive to accomplish most task with the least amount of tools.

An unordered list of tools.

### Servers
Used to write backends, API's and such.

- Vert.x
- Node.js
- aiohttp/asyncio
- Netty (The API's are kind of convoluted so maybe not use it directly.)
- Undertow (Only if we absolutely NEED it.)

### Frontend
Used for any client, mobile web or desktop.

- Polymer
- Android
- Pug/Jade
- Pixi.js
- Chromecast application framework
- Web Components
- HTML5 / CSS3
- Skeleton CSS (Like, super lightweight and looks good.)
- Bootstrap (Avoid, it's heavy and outdated*.)
- JavaFX (For java desktops.)
- VCL/LCL (for Delphi desktop)

Outdated as in "not popular" anymore, it's still actively maintained etc. 

There's also JQuery but we are trying to migrate
away from it. Because it is not strictly necessary, an additional dependency and a quite big one. We prefer to #usetheplatform and web components.

### Persistence
Used to store data, important for most projects.

| Storage | Use cases|
| :------------- | :------------- |
| ElasticSearch  | ElasticSearch is dynamite for search and indexing truckloads of megabytes.  |
| Hazelcast  | Gold for anything in-memory and clustered, it can be used for literally ANY distributed data structure.  |
| CQEngine | For local, non clustered data CQEngine is super easy to get going with and fast,  |
| MongoDB  | MongoDB is easy to get started with, plain document DB here. Perfect when we need multiple writers and sharding.  |
| RealmDB  | Encrypted and very user friendly, similar to CQEngine but with an even easier query API, use for Android rather than SQLite. |
| MySQL  | MySQL really only used when a relational DB is required or not migrated from.  |

CQEngine supports bundling as it's written entirely in Java, it's recommended where we have a single writer. Which is often
the case when designing data layout for microservices.

### Serializers
For transferring data across the network or persisting to disk.

- Kryo
- Jackson
- JAXB
- ReflectASM

### Scripting
For including scripting support in a non-scripted language.

- JSR233
- JEXL
- Nashorn

### Languages
All projects needs a language, these are some good ones.

- Java
- Python
- Vyper (EVM contracts)
- Kotlin
- JavaScript
- Delphi
- C

Vyper will be great on the EVM, solidity is too complex and much harder to audit.

Kotlin can be a good complement to Java, we'll probably only use it for Android.

Maybe we should replace Delphi/C with something more recent? That comes with proper package management and a decent IDE.

### Testing
To make sure it works, am I right.

- JUnit
- Mocha

### Security
Any tools used in a security context.

- NMap
- Wireshark
- OWASP Zap
- OWASP Dependency scanner
- Metasploit
- Argon2

### Terminal
Used to write terminal applications or perform tasks in an environment without a desktop environment.

| Name | Description
| ---  | --- |
| JAnsi | x-platform terminal apps in Java |
| Curses | GNU/Linux python terminal apps |
| Vim | for working with files on a server |
| find | find files, easy to use. |
| grep | find stuff within files. |
| xargs | pass output from one command as arguments to another.|

### Blockchain
For interacting with _the_ blockchain.

- Web3j
- Infura
- Coinbase commerce
- geth

### Data processing/visualization
Miscellaneous data utils.

- Kibana
- Apache POI

### Data formats
The format of our data.

- JSON
- YAML
- XML
- CSV
- XLSX/XLS

JSON is preferred for networking, YAML is preferred for configuration.

We should add a binary protocol. 

### Build tools
Anything related to the build process

- Git (with GitHub, yay!)
- Gradle
- Maven
- JetBrains IDE's.
- Travis CI / Jenkins / Zapperfly ASM

### Animation and graphics
- Spine?
- Photoshop?

# What's missing? 
Here we describe any features that we are lacking and could potentially consider using a framework for.

- Serialization for a binary protocol. 'protobuf' etc.
- Turn most list options into links so we can credit properly.
- More native, but we don't do to much native :(
- Maybe we can add Rust/Go etc? or replace Delphi/C with those.