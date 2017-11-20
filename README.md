# fcrepo3-jetty

This is a copy of jetty with fcrepo3 installed

* [Fedora repository](https://github.com/fcrepo3/fcrepo)

## Included Versions

* jetty: 8.1.16
* fedora: 3.8

## Usage

### Dependencies

* [Java 7 (JRE)](https://java.com/en/download/index.jsp)

### Manual

    git clone https://github.com/sul-dlss/fcrepo3-jetty
    cd fcrepo3-jetty
    java -Xmx256m -XX:MaxPermSize=256m -jar start.jar

You can also change the port jetty starts on by editing the file etc/jetty.xml and changing this line to indicate a different port number:

    <Set name="port"><SystemProperty name="jetty.port" default="8983"/></Set>

### Using jettywrapper

For use within your Hydra application's Rails directory.

    rake jetty:install
    rake jetty:start

See [jettywrapper](https://github.com/projecthydra/jettywrapper) for more information regarding configuration and usage.
Port numbers and other java options maybe configured via the gem.

### Interaction

When jetty is finished initializing itself, Fedora is available in two copies,
one for developement

* [http://localhost:8983/fedora/](http://localhost:8983/fedora/)

and an additional copy for testing:

* [http://localhost:8983/fedora-test/](http://localhost:8983/fedora-test/)

You can see a list of all installed applications at

* [http://localhost:8983](http://localhost:8983)
