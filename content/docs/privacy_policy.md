---
title: Privacy Policy
type: docs
weight: 5
---

THIS DOCUMENT IS CURRENTLY IN DRAFT.

## 1 Introduction

Because of the nature of the app, Digital Carrot handles a lot of sensitive information.
This includes health data, to-do lists, calendar events, app and browser usage metrics,
API keys, login credentials to other services and more. Because of this, protecting your
data is of the utmost importance to us. As a result we commit to:

- Never sell or share any of your information with third parties.
- Never use any of your information for advertising or marketing purposes.
- Always handle your data in a responsible manner. This following industry standard security
  best practices such as end to end encryption.

All data that you provide to the Digital Carrot app will be fully private and will not be
accessible to anyone else.

With that said, Digital carrot may collect some personal information, but will only do so
for your benefit and with your direct consent. Any data collection that we do will be fully
optional, will not affect the app's functionality and will be opt-in by default. We currently
will only collect information in the following scenarios:

- For users who wish to opt-in to optional scientific studies.
- For use in customer support cases where user's information may be required for debugging.

For more information on these scenarios, see section 4.

Digital Carrot may also collect some anonymous metrics pertaining to app usage. This includes
information such as the number of times a plugin was downloaded, but will never include
any personal information. For more details, see section 5.

To summarize:

- We will NEVER collect any personal information without your EXPLICIT consent to do so.
  Any personal information you do consent to share will either be anonymized and aggregated
  in the form of optional, opt-in scientific studies OR will be on a case by case basis for
  customer support.
- We MAY collect some anonymous data pertaining to app usage. This will never include any
  personal information.
- We will NEVER share or sell your data with third parties such as advertisers and data brokers.
- We will follow industry best practices such as end to end encrypt any time that your data
  is stored on our servers.

## 2 Scope

This privacy policy applies to all software pertaining to the Digital Carrot apps across all
platforms that are either written by or certified by Digital Carrot LLC. This includes the
Digital Carrot mobile and desktop apps, any website owned by Digital Carrot LLC, online services
maintained by Digital Carrot, plugins written by Digital Carrot LLC and open source
plugins which are distributed through any of the Digital Carrot software repositories.

This policy does not apply to any third party plugins that users wish to install in the Digital
Carrot app. We are not liable for any damages caused by third party plugins.

With that said, we will take the following steps to protect users against potentially malicious
plugins.

- Third party plugins will not have access to any internal APIs for collecting any information
  from devices that are running the Digital Carrot App. This includes:

  - Apple Health and Google Health Connect
  - Apple Event Kit
  - GPS location
  - App and Website usage information from Apple and Google's mobile APIs

- Plugins will be able to make network API calls, however all plugins must declare what domains
  they wish to connect to so that users know what services their plugins are contacting.

- Plugins are fully sandboxed by default with no ability to interact with the outside world.
  Users will be able to see any time a plugin requests permission to read their data from any
  source or modify their system.

- Users must explicitly opt in to download and use third party extensions in the app.

## 3 How do we handle your data?

Your data can reside in one of two places in the Digital Carrot ecosystem:

- Locally on your devices
- In the cloud on our servers

By default your data is stored locally and won't leave your device unless you enable the
app's sync functionality. If the app's sync functionality is enabled, your data will be
encrypted on device and send to the cloud so that it can be shared with the rest of your
devices.

### 3.1 Local Data

Local data is stored in un-encrypted form, with the exception of API keys, passwords and
other secrets. It is up to the user to ensure that any data on their device is protected
by using strong system passwords and disk encryption.

### 3.2 Data Stored on the Digital Carrot Cloud

All non-anonymous user data sent to the Digital Carrot Cloud is end to end encrypted.
This encryption is applied using a secret key that will never leave your device in
un-encrypted form. This ensures that we will never be able to read data synced through
our servers and that all of your data will remain secure in the event of a data breach.

Digital Carrot uses AES 256 encryption or greater to encrypt your data on the cloud.

#### 3.2.1 Data Retention Policy

Data that is not updated frequently will be removed from our servers after a certain
period of time. This includes point-in-time information such has how far someone walked
on a specific day, but will not include data such as app configurations which need to be
constantly synced between devices. Data removed from our servers will still be available
on your device, but won't be backed up.

#### 3.2.2 Data Deletion Policy

All users will be able to request that their data is immediately deleted from our servers
at any point no questions asked. We're happy to do this for you! After all, your data is
encrypted and of no use to us and only serves to increase our cloud storage bill.

### 3.3 Data Export

Users will have the ability to export all their data from the app. For the other nerds
out there, your data will be exported in JSON format so that you can analyze it to
your hearts content!

## 4 Opt in Data Collection

Users may choose to share some information with us for the purpose of scientific
studies or to help with customer support cases.

### 4.1 Scientific Studies

Digital Carrot LLC may conduct scientific studies using user data in the future. In all cases
we will:

- Request express consent for participation in any studies.

- Outline exactly what data will be collected for the study.

  - Before users consent to participate in any study they will be able to see exactly what information
    we are collecting.
  - At the end of every study users will be able to request a report showing exactly what information
    was collected from them for the study.

- Users will be informed about the duration of the study before consenting. All studies will be timeboxed
  to a reasonable time window.

- The results of any studies will be shared with anyone who participates in them.

- All data collected will be fully anonymized before being sent to our servers.

### 4.2 Customer Support

Digital Carrot relies heavily on user provided data to function. Users may
encounter bugs that are specific to the data which they have provided to the
system. In cases such as this, Digital Carrot customer service agents might
request that users share data could be related to bugs and other defects.

Personal information will not be automatically collected for customer support
cases. Customer support representatives will always request this directly
from the user on a case by case basis.

Any customer information relating to bugs and support tickets will be stored
internally and will never be posted on public issue trackers.


## 5 Collection of Anonymous Metrics

Digital Carrot reserves the right to collect some anonymous metrics that will allow us
to determine the health of the application. This includes, but is not limited to,
information such as:

- The number of times a plugin was downloaded.
- What versions of the app are currently in use.
- What operating systems the app is installed on.

This does NOT include any personal information such as health or location data.
