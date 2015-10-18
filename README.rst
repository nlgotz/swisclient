SwisClient
==========

SwisClient is a Python class that allows the end user to interact with the SolarWinds API (SWIS). The base of this code is used from the SolarWinds Orion SDK sample (https://github.com/solarwinds/OrionSDK), with only the class implemented so that developers can further extend it.

Install
-------
SwisClient should work with both Python2 and Python3

Python2 Install from pip::

    pip install swisclient

Python3 Install from pip3::

    pip3 install swisclient

Or you can run build this locally::

    git clone https://github.com/nlgotz/swisclient.git
    python setup.py install



How to Use
----------

Example::

    import swisclient

    # Create connection to SolarWinds Orion Server
    swis = swisclient.SwisClient("server", "username", "password")

    # Add current node to NCM
    try:
        ncm = swis.invoke("Cirrus.Nodes", "AddNodetoNCM", 1)
    except Exception as e:
        print e


License
-------

    This software is licensed under the Apache License, version 2 ("ALv2"), quoted below.

    Copyright © 2015 SolarWinds Worldwide, LLC.  All rights reserved.

    Licensed under the Apache License, Version 2.0 (the "License"); you may not
    use this file except in compliance with the License. You may obtain a copy of
    the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
    WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
    License for the specific language governing permissions and limitations under
    the License.
