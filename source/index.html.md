---
title: Capital Float API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='https://www.capitalfloat.com/'>Capital Float</a>

includes:
  - master_values

search: true
---

# Introduction

Tech Integration involves partner exposing “Get a Loan” option on their platform. Interested agents of the partner click on the option and are exposed to an application form. Fields of the form exposed; can be customised. The applications are then processed internally by CF.

For Partners opting for PayLater product, can do a bunch of other things like creating a drawdown; verifying the tranche etc with integration.

The REST APIs allows you to share application data of your agents and also to perform different actions for PayLater profiles. This page list out all the APIs provided by Capital Float for different use cases like acquiring agent data for loan processing, token sharing for agents onboarded directly by the fleet on street, confirmation/rejection of loan application by CF, creating a block, creating a tranche from block.

# Authentication

> Request:

```shell
# With shell, you can just pass the correct header with each request
curl -H "Content-type: application/json" -X POST <URL>/cf/user/token -d '{"client_id": "<CLIENT_ID>", "client_secret": "<CLIENT_SECRET>"}'
```

> Response:

```json
{
  "access_token": "57ed301af04bf35b40f255feb5ef469ab2f046aff14",
  "expires_in": 7200
}
```

To make a REST API call, you must include request headers including the Authorization header with an access token.

To get an access token, you must get an partner account created with Capital Float, then Capital Float will generate a set of `CLIENT_ID` and `CLIENT_SECRET` for your app for both the sandbox and live environments. Then, you pass the `CLIENT_ID` and `CLIENT_SECRET` in the request body to acquire an access token.

The authorisation server issues an access token in exchange for your `CLIENT_ID` and `CLIENT_SECRET`. You use the access token for authentication when you make REST API requests by passing it in the Authorization Header.

You can manage your credentials in the Dashboard. All API requests must be made over HTTPS. Any requests made over HTTP will fail.

`Authorization: <YOUR_TOKEN>`

<aside class="notice">
You must replace <code>YOUR_TOKEN</code> with your access token.
</aside>

# Acquisition

Coming Soon

## Acquisition

Coming Soon

## APIs

Coming Soon

# Checkout/Register - Acquisition

Coming Soon

## APIs

Coming Soon

## Web Redirection

Coming Soon

## SDKs

Coming Soon

# Token Sharing - Offline

Coming Soon

# Handshake

Coming Soon

## Token Status

Coming Soon

# Agent/Profile activation

Coming Soon

## Disbursal

Coming Soon

## Paylater( PL/IPL/BPL/IBPL)

Coming Soon

### Create a Block

Coming Soon

### Tranche / Charge / Disbursal

Coming Soon

### OTP acceptance

Coming Soon

### Block Balance

Coming Soon

### Remove Block Balance

Coming Soon

### Agent Info

Coming Soon

## Disbursal Notification

Coming Soon

## Tranche rejection notification

Coming Soon

## Disbursal API

Coming Soon

# Repayment

Coming Soon

## Repayments - Partner

Coming Soon

## Repayments - Agent

Coming Soon

## Repayment

Coming Soon

## Repayment Reminder

Coming Soon

## Agent Status Notification - Active/Suspended

Coming Soon
