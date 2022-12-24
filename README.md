# SIMPLE_CONTRACT_MULTISIGN
 Simple abstract contract that allows to implement multising easily

## Usage example:

function openTrade(bool _open) external multiSignReq {   
&emsp;&emsp;if(!multiSign()) return;  
&emsp;&emsp;isTradeOpened = _open;  
}  

## How it works:
multiSignReq modifier checks at the start if you are owner and at the end checks if multiSign was executed  
multiSign() stores the transaction if not previously stored and adds the owner sign  

Once the required number of owners confirm the transaction multSign returns true
