Kafka CLI
=============================================================

[![Build Status](https://travis-ci.org/fhussonnois/kafkacli.svg?branch=master)](https://travis-ci.org/fhussonnois/kafkacli)
[![GoDoc](https://img.shields.io/badge/docs-GoDoc-blue.svg)](https://godoc.org/github.com/fhussonnois/kafkacli)

[Apache Kafka](http://kafka.apache.org/) is a high-throughput, distributed, publish-subscribe messaging system.

## Kafka Connect CLI

A simple Command line interface (CLI) to manage connectors through the Kafka Connect REST Interface.

### Install and build packages
```bash
go get github.com/fhussonnois/kafkacli/cmd/kafkaconnectcli
```

or...

```bash
./release.sh
```

### Run command
```bash
./bin/kafka-connect-cli
```

### Usage

```bash
A simple Command line interface (CLI) to manage connectors through the Kafka Connect REST Interface.

Usage of ./bin/kafka-connect-cli: command [arguments] 
The commands are : 

    list            Listing active connectors on a worker.
    config          Getting connector configuration.
    create          Creating a new connector.
    delete          Deleting a connector.
    delete-all      Deleting all connectors.
    pause           Pausing a connector (useful if downtime is needed for the system the connector interacts with).
    plugins         Listing installed connectors plugins.
    resume          Restarting a connector.
    restart-failed  Restarting failed tasks for a connector.
    status          Getting connector status.
    tasks           Getting tasks for a connector.
    scale           Scaling up the number of tasks for a connector.
    update          Updating connector configuration.
    version         Getting a connect worker version.

Use "kafka-connect-cli help [command]" for more information about that command.

```

### Create new connector instance

A new connector configuration can be passed through either json or properties file.

```
Usage of create: Creating a new connector.
The arguments are :
  -config string
    	The connector configuration json string. (Required)
  -config.json string
    	<file> The connector configuration json file. (Required)
  -config.props string
    	<file> The connector configuration properties file. (Required)
  -host string
    	The connector worker host address. (Required) (default "localhost")
  -port int
    	The connector worker port. (Required) (default 8083)
  -pretty
    	Pretty print json output.
```

## Confluent Schema registry

A simple Command line interface (CLI) to manage [Confluent](http://docs.confluent.io/current/schema-registry/docs/api.html) Schema Registry.

### Install and build packages
```bash
go get github.com/fhussonnois/kafkacli/cmd/schemaregistrycli
```

### Run command
```bash
./bin/schema-registry-cli
```

### Usage

```bash
A simple Command line interface (CLI) to manage Confluent Schema Registry.

Usage of ./bin/schemaregistrycli: command [arguments] 
The commands are : 

	global-compatibility	Getting the global compatibility level.
	compatibility		Getting subject compatibility level for a subject.
	schema			Getting a specific version of the schema registered under this subject
	register		Registering a new schema under the specified subject.
	subjects		Getting the list of registered subjects.
	test			Testing schemas for compatibility against specific versions of a subject’s schema.
	set-compatibility	Setting a new compatibility level.
	versions		Getting a list of versions registered under the specified subject.

Use "schema-registry-cli help [command]" for more information about that command.
```

## Contributions
Any contribution is welcome

## Licence
Licensed to the Apache Software Foundation (ASF) under one or more contributor license agreements. See the NOTICE file distributed with this work for additional information regarding copyright ownership. The ASF licenses this file to you under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License