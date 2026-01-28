# base-mini-app-
i am building a base mini app that can allow me transact even when i am offline 
from eth_account import Account
from web3 import Web3fff

# 1. Setup your detailsdff
private_key = "YOUR_PRIVATE_KEY"  # Never share thisbbsfyddgg
recipient_address = "0x..."hbssdffffggg
amount_eth = 0.001
chain_id = 8453  # Base Mainnetydgfffgg
uddee
# 2. Create the raw transactionddddfuuedcggeeeggff
# Note: You'll need to know the current 'nonce' for your account. dggssddddifddbbb
# In a true data-less setup, you'd track this manually.dggscfgg
tx = {uuggg
    'nonce': 5, ss
    'to': recipient_addrefss,fgggg
    'value': Web3.to_wei(amountbb_eth, 'ether'),ffbb
    'gas': 21000,ddss
    'gasPrice': Web3.to_wei('0.1', 'gwei'),dfffffgg
    'chainId': chain_idgggg
}

# 3. Sign the transaction
signed_tx = Account.sign_transaction(tx, private_key
f
# 4. Output the Raw Hex
print("RAW TRANSACTION HEX (Send this via SMS):")
print(signed_tx.raw_transaction.hex())
