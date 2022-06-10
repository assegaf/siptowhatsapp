# siptowhatsapp
SIP To WhatsApp Gateway for Converting SIP (session initiation protocol) Voice Protocol RTP Audio to WhatsApp Voice Call Protocol,
This also converting WhatsApp Voice Call to SIP Extension / Openpbx (which called "forwarding inbound" external gateway to openpbx extension), for SIP to Whatsapp process we called that "forwarding outbound".

What we are doing is showing that this is possible, and possibility for other messaging/voice call platform too like Viber and Telegram.

Please be noted that this project not allowed to modify the WhatsApp Application Messaging (apk), so you must able to do converting data via Android Framework AOSP side, which is fully open source.

Stay tuned we will open a demo using public sip sample like sip.linphone.org and sip2sip.info, we are looking people who want to invest this product to interconnect the existing openpbx service to add more interconnectivity like whatsapp.

**The demo is ready, if you get busy signal means the single line of demo is still being used by other user. Please wait.**

Demo sip2wa using Public Sip Server, with common used codec that used by all this free sip server, which is G.711, as example as below :

![Codec-PCMU](https://user-images.githubusercontent.com/551532/172825437-55db476f-3f6c-4be2-b882-32101d9bc4dc.png)



# sip2sip.info

You can register here http://www.sip2sip.info for Sip account and use SIP phone app like Linphone to dial "sip2wa" extension/number to try Sip to WhatsApp gateway.

![sip2sip_sip2wa_dial](https://user-images.githubusercontent.com/551532/172806138-b3708740-50b1-4db7-ad48-b2e7508e66ce.png)

and what about destination number of whatsapp account ? 
there is 2 way :

a. Put your destination number of whatsapp you want to call to Display name / Caller Id of your accounts. Eg: "628979993336" as A caller id/ display name, as example see this below picture.

![sip2sip_accountcli](https://user-images.githubusercontent.com/551532/172806660-4220fdb5-1d0a-44b0-8d0d-90c9b49cb4ea.png)

b. After introduction you will be asked to put destination number via dial pad (Sending DTMF tones), then press # to finish input the number and dial the destination whatsapp number. Press the dialpad after introduction finished.

![sip2sip_dialpad](https://user-images.githubusercontent.com/551532/172807341-98538408-9ff8-4001-b42c-6047481f5206.png)


both way will dial the whatsapp destination number, until you hang up the call or destination whatsapp number hang up first.


# sip.linphone.org

You can register here https://www.linphone.org/freesip/home for sip free account,
The destination of call of whatsapp number is the same as sip2sip.info, to put in Display name or Caller ID, or dial via DTMF tones while on call. You can dial account "sip2wa" as picture sample below, to start testing our Sip to WhatsApp gateway.

![linphone_sip2wa_dial](https://user-images.githubusercontent.com/551532/172809395-e875c9ab-c364-433a-9be4-7b061e93c4df.png)


# sip.antisip.com

You can register here https://sip.antisip.com/service/ for sip free account,
The destination of call of whatsapp number is the same as sip2sip.info, to put in Display name or Caller ID, or dial via DTMF tones while on call. You can dial account "sip2wa" as picture sample below, to start testing our Sip to WhatsApp gateway.

![antisip_sip2wa_dial](https://user-images.githubusercontent.com/551532/172822728-898d5fbd-3aff-4b22-9cc7-68946fcab15c.png)


# Conclusion

all the demo is using free sip server, if you have own server you can have dial plan as easy as possibe example, to specific international number and, contact us to have demo to your own server, and possibly own deployment.

