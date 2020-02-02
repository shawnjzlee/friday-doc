# Nickname

### Set nickname

Set nickname - address mapping and enable readable nickname

```bash
clif nickname set <nickname> --address|--wallet <owner>
```

```bash
clif nickname set princesselsa --address friday1y2dx0evs5k6hxuhfrfdmm7wcwsrqr073htghpv
clif nickname set princesselsa --wallet walletelsa

{
  "chain_id": "testnet",
  "account_number": "5",
  "sequence": "0",
  "fee": {
    "amount": [],
    "gas": "200000"
  },
  "msgs": [
    {
      "type": "readablename/SetNick",
      "value": {
        "nickname": {
          "H": "507369347",
          "L": "0"
        },
        "address": "friday15evpva2u57vv6l5czehyk69s0wnq9hrkqulwfz"
      }
    }
  ],
  "memo": ""
}

confirm transaction before signing and broadcasting [y/N]: Y
```

After confirmation, you can use nickname instead of typing full address.

### Change address of nickname

Change address of the given nickname.

```bash
clif nickname change-to <nickname> <new_address> --wallet|-address <old_one>
```

```bash
clif nickname change-to princesselsa friday15evpva2u57vv6l5czehyk69s0wnq9hrkqulwfz --wallet walletanna
clif nickname change-to princesselsa friday15evpva2u57vv6l5czehyk69s0wnq9hrkqulwfz --address friday1y2dx0evs5k6hxuhfrfdmm7wcwsrqr073htghpv

{
  "chain_id": "testnet",
  "account_number": "5",
  "sequence": "0",
  "fee": {
    "amount": [],
    "gas": "200000"
  },
  "msgs": [
    {
      "type": "readablename/ChangeKey",
      "value": {
        "nickname": "bryan",
        "old_address": "friday15evpva2u57vv6l5czehyk69s0wnq9hrkqulwfz",
        "new_address": "friday1y2dx0evs5k6hxuhfrfdmm7wcwsrqr073htghpv"
      }
    }
  ],
  "memo": ""
}

confirm transaction before signing and broadcasting [y/N]: Y
```

After confirmation, you may use changed address by current nickname.

### Get address

Get mapped address of current nickname

```bash
clif nickname get-address <nickname>
```

```bash
clif nickname get-address bryan

{
  "nickname": "bryan",
  "address": "friday15evpva2u57vv6l5czehyk69s0wnq9hrkqulwfz"
}
```
