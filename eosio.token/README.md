eosio.token
-----------

This eosio contract allows users to create, issue, and manage tokens on
eosio based blockchains.

We add a blacklist to the token, which is used to limit people to transfer to suspicious or specified account(but does not limit the account transfer to normal account).

You can add an account to blacklist with `cleos`:

    cleos push action yourowntoken addblacklist '["wrongaccount", "4,YOURSYM"]' -p tokenissuer

and if you want to remove the account from the blacklist, simply use:

    cleos push action yourowntoken rmblacklist '["wrongaccount", "4,YOURSYM"]' -p tokenissuer

e.g. you can replace
    
    yourowntoken->whaleextoken
    tokenissuer->whaleextoken
    4,YOURSYM->3,WAL
