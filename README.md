# SIPP-Scenarios - Live FAL
SIPP Scenarios used on the FAL's LIVE on youtube about sipp.

## How to use
This scenario will make a call to an UAS specified as a parameter on command line when you start using sipp. 
When you start the sipp, the following things will happen:

* Start a call to a predefined UAS
* Optionally expect a SIP 100 Trying or 183 Session Progress
* Expect a SIP 200 OK answering the call
* Play an pcap audio in g711a format of lenght about 8 seconds
* Send a RFC 2833 DTMF digit 1
* Hangup the call

## Starting sipp
Start sipp using this scenario with the following command line:
- sipp -sf uac_dtmf_rtp.xml -m 500 -l 100 -s 1000 UAS_IP_ADDR:5060

The meaning of parameters:
* -m specifies how many calls sipp will accept before stop the test.
* -l how many calls per seconds (CPS) send to UAS
* -s the extension or request uri for UAS

You need to authorize the IP from where your sipp is sending calls on you UAS.
