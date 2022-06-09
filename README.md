# siptowhatsapp
SIP To WhatsApp Gateway for Converting SIP (session initiation protocol) Voice Protocol RTP Audio to WhatsApp Voice Call Protocol,
This also converting WhatsApp Voice Call to SIP Extension / Openpbx (which called "forwarding inbound" external gateway to openpbx extension), for SIP to Whatsapp process we called that "forwarding outbound".

What we are doing is showing that this is possible, and possibility for other messaging/voice call platform too like Viber and Telegram.

Please be noted that this project not allowed to modify the WhatsApp Application Messaging (apk), so you must able to do converting data via Android Framework AOSP side, which is fully open source.

Stay tuned we will open a demo using public sip sample like sip.linphone.org and sip2sip.info, we are looking people who want to invest this product to interconnect the existing openpbx service to add more interconnectivity like whatsapp.

Demo sip2wa using Public Sip Server.

1. sip2sip.info

You can register here http://www.sip2sip.info for Sip account and use SIP phone app like Linphone to dial "sip2wa" extension/number to try Sip to WhatsApp gateway.

![sip2sip_sip2wa_dial](https://user-images.githubusercontent.com/551532/172806138-b3708740-50b1-4db7-ad48-b2e7508e66ce.png)

and what about destination number of whatsapp account ? 
there is 2 way :

a. Put your destination number of whatsapp you want to call to Display name / Caller Id of your accounts. Eg: "628979993336" as A caller id/ display name.

![sip2sip_accountcli](https://user-images.githubusercontent.com/551532/172806660-4220fdb5-1d0a-44b0-8d0d-90c9b49cb4ea.png)

b. After introduction you will be asked to put destination number via dial pad (Sending DTMF tones), then press # to finish input the number and dial the destination whatsapp number.

![sip2sip_dialpad](https://user-images.githubusercontent.com/551532/172807341-98538408-9ff8-4001-b42c-6047481f5206.png)


both way will dial the whatsapp destination number, until you hang up the call or destination whatsapp number hang up first.



2. sip.linphone.org




![Screenshot-Linphone](https://user-images.githubusercontent.com/551532/172606292-0527cf80-a52d-4ac9-a661-aba0e269fc29.png)


