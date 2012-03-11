Splunk Storm Cookbook
=================
Enables a server to ship logs to Splunk Storm (currently in beta) for storage an analysis

Requirements
============
A Splunk Storm beta account

Attributes
============

Usage
============

Configure Splunk Storm to auto-authenticate for 15 minutes
----------------------------------------------------------
1. Log in to Splunk Storm
2. From your *Projects dashboard* select *Inputs*
3. Select *Send data through the network*
4. Select *Automatic authentication*
5. Copy the address provided to the attributes e.g. to your environment
```ruby
   "splunk-storm" => {
	  "log_host" => {
	    "address" => "logs3.splunkstorm.com",
	    "port" => "20380"
	  }
	},
```
6. Upload your environment file
    knife environment from file environments/prod.rb
7. Run `chef-client` to get your node to authenticate with Splunk Storm.
8. Send some test data
    logger "my little pony"
9. On the Splunk Storm dashboard confirm that your host has been authenticated and then turn off auto-authentication.


License and Author
==================

Author:: Edward Sargisson (<edward@trailhunger.com>)

Copyright 2012, TrailHunger.com Trail Data Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.



