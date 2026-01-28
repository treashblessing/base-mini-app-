# base-mini-app-
i am building a base mini app that can allow me transact even when i am offline 
from eth_account import Account
from web3 import Web3f

# 1. Setup your detailsd
private_key = "YOUR_PRIVATE_KEY"  # Never share thisbbsfydd
recipient_address = "0x..."hbssdff
amount_eth = 0.001
chain_id = 8453  # Base Mainnetydg
u
# 2. Create the raw transactionddddfuuedcgg
# Note: You'll need to know the current 'nonce' for your account. dggssddddif
# In a true data-less setup, you'd track this manually.dggsc
tx = {uu
    'nonce': 5, ss
    'to': recipient_addrefss,f
    'value': Web3.to_wei(amount_eth, 'ether'),
    'gas': 21000,ddss
    'gasPrice': Web3.to_wei('0.1', 'gwei'),dff
    'chainId': chain_id
}

# 3. Sign the transaction
signed_tx = Account.sign_transaction(tx, private_key
f
# 4. Output the Raw Hex
print("RAW TRANSACTION HEX (Send this via SMS):")
print(signed_tx.raw_transaction.hex())
