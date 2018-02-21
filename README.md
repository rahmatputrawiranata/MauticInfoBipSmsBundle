## Synopsis

This plugin allows to send SMS messages through http://sms-notifikasi.com/ service provider API not infobip anymore. It is based on the current version of and Twilio plugin available in the default Mautic install package, and also on [Infobip](https://github.com/mjlogan/MauticInfoBipSmsBundle "Infobip Repo") plugin for previous Mautic versions written by @abreuleonel and @mjlogan .

## Motivation

The lack a of an updated version of the original Infobip plugin as well as the absence of an alternative to Twilio API was what motivated the creation of this.

## Installation

- Copy the MauticInfoBipSmsBundle to the plugins folder.
- Go to the Configuration -> Plugins Settings, in Mautic web interface.
- Click on Install/Upgrade Plugins.
- The plugin should now be available for configuration.

## Tests

After configure the plugin.
- 1 - Go to Channels -> Text Messages.
- 2 - Create a text message with any content.
- 3 - Go to Components -> Form.
- 4 - Create a new Form (New Campaign Form).
- 5 - Create the form with a email or mobile number field.
- 6 - Go to Campaigns.
- 7 - Create a new campaign: Contact Sources: Campaign Form.
- 8 - Choose the form you created early.
- 9 - In the next step, select Action.
- 10 - In the select box, chose InfoBip Send text messages.
- 11 - In the box of InfoBip Send text messages, put a name and choose the form message - that you created early.
- 12 - Save your campaign.
- 13 - Go to Contacts.
- 14 - Create a contact with a valid mobile number.
- 15 - Go to Components -> Form.
- 16 - Click in Preview in the form that you created.
- 17 - Send this form with the contact information.
- 18 - Execute the command php console mautic:campaigns:trigger. 
- 19 - The contact used to fill the form, will receive the text message.

## Contributors

@abreuleonel @mjlogan @nurcahyopujo
