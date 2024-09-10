# payToSay
A nexscript contract for a group chat behind a paywall, you pay the owner of the group chat.

## How it works
The contract requires payments to accept messages, then the owner of the contract can withdraw funds recieved by the contract.

## Incentive structure
The owner could be an influencer, a website, a dao, an x-account, anything with a digital reach. The user would pay to get his message across, the user would probably pay more for better or more acirate reach.

## Functions
    function say(bytes alias, bytes message)
    
this function takes inn the message from the user and the perferred alias, it checks that eough payment is added to the transaction.

    function payday(sig ownerSig)

this function lets the owner of the contract withdraw funds gatheres from the messages.

both the minimum payment price and the contract owner is decided in the constructor of the contract.

    contract PayToSay(int paymentRequirement, pubkey owner)

## Notes
It is possible to pay the miner of the block instead of the owner of the contract, I have not decided if this is a feature or a bug.

I got a lot of inspiration from the superhacker dagur: https://gitlab.com/dagurval/nexa-superchat/-/tree/master?ref_type=heads
