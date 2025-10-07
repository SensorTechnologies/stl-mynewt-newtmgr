<!--
#
# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
#  KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.
#
-->

<a href="https://github.com/apache/mynewt-newtmgr/actions/workflows/build.yml">
  <img src="https://github.com/apache/mynewt-newtmgr/actions/workflows/build.yml/badge.svg">
<a/>

# STL Newtmgr176
Newtmgr176 is a customised version of Newtmgr for the Sensor Technologies Sureline Relay Bluetooth Controller.
It uses a reduced image upload chunk size of 176 bytes instead of the default 512 bytes. This is required
because the commands are sent via an SPI link with maximum message length of 255 bytes and some Newtmgr message
overhead is required.

# Newtmgr

Newt Manager (newtmgr) is the application tool that enables a user to communicate with and manage
remote devices running the Mynewt OS. It uses a connection profile to establish a connection with
a device and sends command requests to the device.
The newtmgr tool documentation can be found under [/docs](/docs) which are
published at http://mynewt.apache.org/latest/os/modules/devmgmt/newtmgr.html

### Building

Build the newtmgr176 tool as follows:

1. Clone this repository
2. In the repository directory, cd newtmgr
3. `GO111MODULE=on go build`
4. `mv newtmgr newtmgr176'
