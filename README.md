

# siptowhatsapp
SIP To WhatsApp Gateway for Converting SIP (session initiation protocol) Voice Protocol RTP Audio to WhatsApp Voice Call Protocol,
This also converting WhatsApp Voice Call to SIP Extension / Openpbx (which called "forwarding inbound" external gateway to openpbx extension), for SIP to Whatsapp process we called that "forwarding outbound".

I made presentation for the project in 2020, for possibly some company invest this, and 2022 has come yet.

[![Presentation Sip2Wa 2020](https://img.youtube.com/vi/_dznZM47sLs/0.jpg)](https://www.youtube.com/watch?v=_dznZM47sLs)
(click for see the presentation in youtube)

What we are doing is showing that this is possible, and possibility for other messaging/voice call platform too like Viber and Telegram.

Please be noted that this project not allowed to modify the WhatsApp Application Messaging (apk), so you must able to do converting data via Android Framework AOSP side, which is fully open source.

# Interconnection With Your SIP Server ( READ THIS !!!! before you have idea of something )
For inter connecting sip2wa to your ip pbx server or someone called it softswitch, this is what you need :
a. IP PBX Server on the Internet with public IP. someone else with softphone or IP Phone that use random ip /4g internet or/and behind nat can connect As Extension (using user/pass) example 101 can dial to 102, no signaling issue, no audio issue. (What is softphone example: Microsip/LinPhone)
b. When you dial to Person-A number whatsapp, Person-A will see calling from DEMO-B number, A wont have see call from President of USA number or any number you expected to be. DEMO-B number is WhatsApp number you register as Account in Sip2Wa app.
c. You have IP PBX Server that capable someone with microsip or Linphone connect to your server as Extension. Using User and Password. You hear the audio coming from this extension, inbound/outbound.
d. You cannot use trunk style ip to ip connection, sip2wa are an extension that use random ip.
e. You have tested this demo below and its working in your environment.


Stay tuned we will open a demo using public sip sample like sip.linphone.org and sip2sip.info, sip.antisip.com, we are looking people who want to invest this product to interconnect the existing openpbx service to add more interconnectivity like whatsapp.

**The demo is ready, if you get busy signal means the single line of demo is still being used by other user. Please wait. You will get a message reply saying that the line busy, this is a sample for hunting like inbound system. Receive inbound altough already online-call. **

Demo sip2wa using Public Sip Server, with common used codec that used by all this free sip server, which is G.711, as example as below :

![Codec-PCMU](https://user-images.githubusercontent.com/551532/172825437-55db476f-3f6c-4be2-b882-32101d9bc4dc.png)



# sip2sip.info

You can register here http://www.sip2sip.info for Sip account and use SIP phone app like Linphone to dial "sip2wa" extension/number to try Sip to WhatsApp gateway.

![sip2sip_sip2wa_dial](https://user-images.githubusercontent.com/551532/172806138-b3708740-50b1-4db7-ad48-b2e7508e66ce.png)

and what about destination number of whatsapp account ? 
there is 2 way to call destination number :

a. Put your destination number of whatsapp you want to call to Display name / Caller Id of your accounts. Eg: "628979993336" as A caller id/ display name, as example see this below picture. 

![sip2sip_accountcli](https://user-images.githubusercontent.com/551532/172806660-4220fdb5-1d0a-44b0-8d0d-90c9b49cb4ea.png)

for example in Linphone software, the destination number is set on SIP Address as above, with inside quote.

b. After introduction you will be asked to put destination number via dial pad (Sending DTMF tones), then press # to finish input the number and dial the destination whatsapp number. Press the dialpad after introduction finished, not in ongoing introduction. Use international format with country code, and without "+" prefix, example: 628979993336, 62 is indonesian country code.

![sip2sip_dialpad](https://user-images.githubusercontent.com/551532/172807341-98538408-9ff8-4001-b42c-6047481f5206.png)


both way will dial the whatsapp destination number, until you hang up the call (in your sip session call) or destination whatsapp account hang up first.


# sip.linphone.org

You can register here https://www.linphone.org/freesip/home for sip free account,
The destination of call of whatsapp number is the same method as above, to put in Display name or Caller ID, or dial via DTMF tones while on call. You can dial account "sip2wa" as picture sample below, to start testing our Sip to WhatsApp gateway.

![linphone_sip2wa_dial](https://user-images.githubusercontent.com/551532/172809395-e875c9ab-c364-433a-9be4-7b061e93c4df.png)


# sip.antisip.com

You can register here https://sip.antisip.com/service/ for sip free account,
The destination of call of whatsapp number is the same as above, to put in Display name or Caller ID, or dial via DTMF tones while on call. You can dial account "sip2wa" as picture sample below, to start testing our Sip to WhatsApp gateway.

![antisip_sip2wa_dial](https://user-images.githubusercontent.com/551532/172822728-898d5fbd-3aff-4b22-9cc7-68946fcab15c.png)

# Voice Inbound testing

You can dial our whatsapp number account +62 858 8131 3764 for testing our inbound routing, we will auto accept the call and will be forwarded to our Openpbx Dial plan for voice testing auto reply, this is a prof that we can use inbound too for showing voice reply and further action can be defined, example: forwarding to predefined extension on PBX system.

Our whatsapp inbound will be alive from now on, until we say otherwise


# Messaging Inbound testing

For messaging inbound, we forward the private's message this number (as message inbound) to the first group its registered to, to that it will notice all member of group (eg. one department) there is incoming new message inbound to this number, so that member can follow up with quoted message or dial up from sip2whatsapp gateway pabx. You can message our whatsapp number for a test as a guest/customer, +62 858 8131 3764 





# Conclusion

all the demo is using free sip server, if you have own server you can have dial plan as easy as possibe example, to specify easier international number or use prefix as dialplan pattern when calling to whatsapp number, contact us to have demo to your own server, and possibly own deployment.

This is a sample how things work and logs of the process.

[![Presentation Sip2Wa 2020](https://img.youtube.com/vi/k79D6ZYYMzg/0.jpg)](https://www.youtube.com/watch?v=k79D6ZYYMzg)
(click for see the presentation in youtube)


# F.A.Q.

**a. Sound Quality not as good as usually ?**

this is demo is limited to use G711, which most free sip server capable and only use 8k bit sample rate, which is not HD Audio. so WhatsApp call audio quality is somehow degraded on the way. If not using free sip server, we use G722 codec which is HD Audio, seem much better.

**b. I always got busy signal when trying to dial the demo ?**

this is demo is limited to single line, by free sip server and by our equipment as well. So please wait until our line is idle or available.

**c. Is it possible to have our deployment in our office ?**

Possibe, contact us for deployment with special good price. It need lots of requirement, including on-site deployment, devices set-up, and many more.

**d. Do you have free testing 1 week or 2 week, just to make sure this is what we need ?**

Yes, you can test our dedicated service using your own whatsapp account, we host it here. Then you can connect as sip trunk to your IP Pbx, as a test inbound/outbound.

**e. Do you have non-cli solution perminute for outbound call only ?**

We provide non-cli solution per minute, as SIP Trunk, price varies per country. Contact us for pricing.

**f. What is the limitation for Dedicated Services (unlimited call inbound/outbound).**

We provide the dedicated services means the whatsapp number account is from the customer it self, it commonly used for inbound/outbound PABX. So customer responsible for the outgoing call number that will affect the account life. Example customer can put limitation only allow outgoing call to X after has minimal once, inbound call or message from X previously. If people report the whatsapp account number as it receiving call without previously saved the number, its affect its account lifecycle.

Downtime, when our internet connection is down, we also will experience the same service downtime. No Exception, best server for IP PBX Server nearby is Singapore. Keep it in mind.



# on going

on going process .. is adding SIP to GSM Gateway from inside android (4G Lte), everything is there on AOSP just need little bit tweaking :) similar to this : https://www.pure-voip.com/ . sooner or later 2g/3g will be dead, and 4g still long ..

investment, etc .. 

