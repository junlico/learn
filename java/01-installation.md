# Install [AdoptOpenJDK](https://adoptopenjdk.net/installation.html#)

## Ubuntu 20.04

- ### Import the official AdoptOpenJDK GPG key

  ```sh
  $ wget -qO - https://adoptopenjdk.jfrog.io/adoptopenjdk/api/gpg/key/public | sudo apt-key add -
  ```

- ### Import the AdoptOpenJDK DEB repository

  ```sh
  $ sudo add-apt-repository --yes https://adoptopenjdk.jfrog.io/adoptopenjdk/deb/
  ```

  If shows `command not found` error, then

  ```sh
  $ sudo apt update
  $ sudo apt install -y software-properties-common
  ```

- ### Install AdoptOpenJDK package, as of this writing, choose JDK version `OpenJDK 11 (LTS)` with the `HotSpot` JVM

  ```sh
  $ sudo apt update
  $ sudo apt install adoptopenjdk-11-hotspot

  $ java -version
  openjdk version "11.0.7" 2020-04-14
  OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.7+10)
  OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.7+10, mixed mode)
  ```

  ```sh
  $ sudo update-alternatives --config java
  There is only one alternative in link group java (providing /usr/bin/java): /usr/lib/jvm/adoptopenjdk-11-hotspot-amd64/bin/java
  Nothing to configure.
  ```

  <!-- Copy the path of Java, `/usr/lib/jvm/adoptopenjdk-11-hotspot-amd64`, <b>DO NOT</b> include the `/bin` portion of the path

  ```sh
  JAVA_HOME=/usr/lib/jvm/adoptopenjdk-11-hotspot-amd64
  PATH=$PATH:$JAVA_HOME/bin
  ``` -->
