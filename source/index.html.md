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

Tech Integration involves partner exposing “Get a Loan” option on their platform. Interested agents of the partner click on the option and are exposed to an application form. Fields of the form exposed; can be customised. The applications are then processed internally by CF.

For Partners opting for PayLater product, can do a bunch of other things like creating a drawdown; verifying the tranche etc with integration.

The REST APIs allows you to share application data of your agents and also to perform different actions for PayLater profiles. This page list out all the APIs provided by Capital Float for different use cases like acquiring agent data for loan processing, token sharing for agents onboarded directly by the fleet on street, confirmation/rejection of loan application by CF, creating a block, creating a tranche from block.
