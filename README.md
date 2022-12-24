# SIMPLE_CONTRACT_MULTISIGN
 Simple abstract contract that allows to implement multising easily

## Usage example:

#### function openTrade(bool _open) external multiSignReq { 
####    if(!multiSign()) return;
####    
####    isTradeOpened = _open;
#### }

### multiSignReq modifier checks at the start if you are owner and at the end checks if multiSign was executed
### multiSign() stores the transaction if not previously stored and adds the owner sign

### Once the required number of owners confirm the transaction multSign returns true