---
title: Capital Float API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:

  - <h2>Contact us:</h2>
  - <p>cfdevelopment@capitalfloat.com</p>

includes:
  - authentication
  - acquisition
  - application
  - documents
  - token_sharing
  - disbursal
  - repayment
  - checkout
  - master_values



search: true
---

# Introduction

Tech Integration involves the partner exposing the “Get a Loan” option on their platform. Interested agents of the partner can click on the option, and will be exposed to an application form. Exposed fields of the form can be customized. The applications are then processed internally by CF.

Partners opting for a PayLater product can do a bunch of other things like creating a drawdown or verifying the tranche, etc, with the integration.

The REST APIs allows you to share your agents’ application data and also to perform different actions for PayLater profiles. This page lists out all of the APIs provided by Capital Float, for different use cases like acquiring agent data for loan processing, token sharing for agents onboarded directly by the fleet on street, confirmation/rejection of loan application by CF, creating a block and creating a tranche from block etc.
