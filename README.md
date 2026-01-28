# base-mini-app-
i am building a base mini app that can allow me transact even when i am offline 
from eth_account import Account
from web3 import Web3

# 1. Setup your detailsd
private_key = "YOUR_PRIVATE_KEY"  # Never share thisbbsf
recipient_address = "0x..."hbssd
amount_eth = 0.001
chain_id = 8453  # Base Mainnet

# 2. Create the raw transactionddddf
# Note: You'll need to know the current 'nonce' for your account. dggssdddd
# In a true data-less setup, you'd track this manually.d
tx = {
    'nonce': 5, 
    'to': recipient_address,
    'value': Web3.to_wei(amount_eth, 'ether'),
    'gas': 21000,
    'gasPrice': Web3.to_wei('0.1', 'gwei'),
    'chainId': chain_id
}

# 3. Sign the transaction
signed_tx = Account.sign_transaction(tx, private_key

# 4. Output the Raw Hex
print("RAW TRANSACTION HEX (Send this via SMS):")
print(signed_tx.raw_transaction.hex())
