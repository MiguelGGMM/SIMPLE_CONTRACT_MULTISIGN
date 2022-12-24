# SIMPLE_CONTRACT_MULTISIGN
 Simple abstract contract that allows to implement multising easily

## Usage example:

function openTrade(bool _open) external multiSignReq {   
&emsp;&emsp;if(!multiSign()) return;  
&emsp;&emsp;isTradeOpened = _open;  
}  

## How it works:
<b>multiSignReq</b> modifier that ensures that you are an owner and multiSign() was executed  
<b>multiSign()</b> stores the transaction if not previously stored and adds the owner sign  

Once the required number of owners confirm the transaction multSign returns true
