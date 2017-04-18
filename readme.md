# Simple Banking

Simple banking is a lua script that allows you to include a banking system in your server. This system uses
EssentialMod cash, and a seperate bank balance field in the database, to allow the player to seperate 'on-character'
cash from that stored safely away!

##### Requires EssentialMod

### Features
  - Stores bank cash seperately
  - Limit giving cash to nearby player
  - 69 ATM Locations
  - 6 Bank Locations
  - Withdraw cash from ATM
  - Withdraw cash from bank
  - Deposit cash at bank
  - Transfer to another persons bank account
  - Check available balance
  - Customisable Settings


### Install
  - Download simple banking
  - Put 'banking' folder into your servers 'resources' folder
  - Add '- banking' to AutoStartResources in citmp-server.yml
  - Import 'db.sql' into EssentialMod database
  - Change database settings on line 2 of server.lua
  - Start / Restart server

### Usage
##### /checkbalance
Example: /checkbalance
Returns the players current account balance. ***By default can be used anywhere (like using a mobile app)***

##### /withdraw [amount]
Example: /withdraw 50
Withdraws the specified amount from the players bank account. ***By default can only be used at ATMs or
banks.***
##### /deposit [amount]
Example: /deposit 50
Deposits the specified amount from the players bank account. ***By default can only be used inside banks.***
##### /transfer [id] [amount]
Example: /transfer 17 2000
Transfers money from the players bank account to the recipients bank account. ***By default can be used anywhere
(like using a mobile app)***
##### /givecash [id] [amount]
Example: /givecash 17 20
Transfers money from the players ***wallet*** to the recipients wallet. ***By default can be used anywhere
as long as the recipient is within 5 Meters***

### Settings
All settings are customisable in the client.lua file.
##### depositAtATM (Default: false)
Allows the player to deposit cash at ATMs. By default cash can only deposited in store at one of
the six bank locations.
##### giveCashAnywhere (Default: false)
Allows the player to give cash no matter how far away the other player is. By default the recipient
has to be nearby (5 Meters). This behaves similar to the bank transfer but for 'on-character' cash.
##### withdrawAnywhere (Default: false)
Allows the player to withdraw cash no matter where they are. By default the player can only withdraw
cash from ATMs or in Banks.
##### depositAnywhere (Default: false)
Similar to the withdrawAnywhere setting. This option allows players to deposit cash into their bank
account from anywhere. By default the player must be in 1 of the 6 bank stores.

#### Note
This is the initial release, some bugs may still be present. Please report them and I will fix them.
Some ATMs might be missing. If you find one please inform me so I can include it in the next release.


#### Upcoming
  - Ability to Rob Banks
  - Multiple Personal Accounts
  - Savings Accounts (With Interest)
  - Business Accounts
  - Shared Accounts (Couples, Spouses, etc.)
