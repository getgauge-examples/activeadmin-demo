# The Active Admin Store

This is a test application to demo Active Admin. Gauge examples use this as a sample System Under Test.

## To run this app locally
```
git checkout local_run
bundle install
bundle exec rake db:drop db:create db:migrate db:seed
bundle exec rails s
```

## To run this app on Docker

Run the following commands and navigate to localhost:8000
```
docker build -t gauge-demo-app .
docker run -p 8000:8000 gauge-demo-app
```

If you are using VirtualBox to manage docker machines, ensure you have enabled port forwarding.
  * Open VirtualBox. Go to Network Settings of the docker machine.
  * Click port forwarding
  * Add a new rule with the following details
    * Name: `Gauge`
    * Protocol: `TCP`
    * Host IP: `127.0.0.1`
    * Host Port: `8000`
    * Guest IP: `127.0.0.1`
    * Guest Port: `8000`

## Building WAR
The application can be packaged using JRuby + Warbler and generate an executable `war`. You can download the `activeadmin-demo.war` file from [here](https://github.com/getgauge-examples/activeadmin-demo/releases/tag/untagged-f0befd5494efa4baabd2).

### Prerequisites

- Install JDK
- Install JRuby (can use rvm or just install JRuby directly). Tested with Ruby 2.3.1, JRuby 9.1.7
- run `rake war`, this should generate `activeadmin-demo.war`

### Using the Artifact

- The `activeadmin-demo.war` generated is an executable war, and comes with an embedded Jetty instance. This is to facilitate self hosting.
- Run `java -jar activeadmin-demo.war`.

# Running the tests

Refer to one or more of the examples

- [Gauge-example-java](https://github.com/getgauge/gauge-example-java)
- [Gauge-example-ruby](https://github.com/getgauge/gauge-example-ruby)
- [Gauge-example-sahi](https://github.com/getgauge/gauge-example-sahi)
- [Gauge-example-csharp](https://github.com/getgauge/gauge-example-csharp)

