
#JeroMQ

Java POJO zeromq (http://zeromq.org) implementation

## Features

* based on zeromq-3
* tcp:// protocol and inproc:// is compatible with zeromq
* not too bad performance compared to zeromq
 * 2M messages (100B) per sec
 * [Performance](https://github.com/miniway/jeromq/wiki/Perfomance) 
* exactly same develope experience with zeromq

## Not supported Features
* ipc:// protocol. Java doesn't support UNIX domain socket.
* pgm:// protocol. Cannot find a pgm Java implementation

## Extended Features
* build your own StreamEngine's Decoder/Encoder
 * [TestProxyTcp](https://github.com/miniway/jeromq/blob/master/src/test/java/zmq/TestProxyTcp.java) 
 * [Proxy](https://github.com/miniway/jeromq/blob/master/src/main/java/org/jeromq/codec/Proxy.java)
* ZLog - ZMQ persistence (Under Construction)
 * Inspired by Apache [Kafka](http://incubator.apache.org/kafka/)
 * Store your ZMQ message as-is
 * Comsune the stored messagee through Zero Copy

## Usage

Add it to your Maven project's `pom.xml`:

    <dependency>
      <groupId>org.jeromq</groupId>
      <artifactId>jeromq</artifactId>
      <version>0.1.0-SNAPSHOT</version>
    </dependency>

