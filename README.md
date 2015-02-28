Spark-server installation automation
======

This mini DevOps project/exercise aims to fully automate the process of setting up a [spark-server](http://github.com/spark/spark-server) on a Raspberry pi!

The ultimate goal would involve using [QEMU](www.qemu.org) to emulate a Raspberry Pi box on user machines without physically owning one. Having this feature allows testing and automation of the setup without having to manually swap out SD cards and wait for them to boot up each time.

The current installation planning can be found here: [install-specs](install-specs.md)

###First successful attempt on a **Odroid-C1(ARMv7 device)**

![spark-server-docker](/pics/spark-server-in-docker.png)

###Docker container implementation

An initial V0.0.1 version has been pushed to Docker hub that demonstrates the successful installation in a container itself. More information here: [Dockerfile](Dockerfile)


###Future possible add-ons

- self-signed https implementation for API endpoint
- Using [QEMU](www.qemu.org) to automate the entire testing and provisioning setup
- Explore using **chef-solo** or **puppet** to handle the entire installation procedure
- using [Docker](https://www.docker.com) to manage the entire setup and no longer require installation. Pull, run and play!

###Platforms that *should* be supported
- RPi B V1
- RPi B+ V1
- RPI V2
- Hummingboard
- Odroid
