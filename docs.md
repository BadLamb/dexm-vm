# Dexm-VM

## The Dexm object

### dexm.blockInfo(index)
dexm.blockInfo returns a dictionary containing information about the block at index. If there isn't a block with *index* it return an empty dictionary.

### dexm.pay(reciver, amnt, includesFee)
dexm.pay takes a string of the wallet as the first argument, the second arg is an amount recived from dexm.convert, includesFee is a boolean. If it's true then the fees wil be subtracted from the amount, otherwise the amount + the fees will be subtracted from the contract balance.
Returns 0 if the transaction failed, otherwise it returns a non zero error code.

### dexm.convert(amnt, unit)
dexm.convert returns an encoded integer representing the amount and the unit of mesure.

### dexm.parse(convertedInteger, optionalUnit)
dexm.parse returns a dictionary containing a float representing the encoded amount and the unit of mesure. Pass an empty string to optionalUnit to have it just return whatever it was encoded as. Returns an empty dictionary on error
