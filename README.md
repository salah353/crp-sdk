 # CRP SDK — Chain Relay Protocol (Sui)

CRP SDK is an open-source SDK for **secure local signing and lifecycle management of Sui transactions**.
It helps wallet and fintech developers integrate stablecoin transfers without exposing private keys.

## Mainnet Proof (Sui)

USDT transfer executed on Sui mainnet:

- **Tx Hash:** `3NR4hymfrypfVK2iF6oZziXjYsC3XvZ9BGgwtBnRKdMh`
- **Explorer:** https://suiscan.xyz/mainnet/tx/3NR4hymfrypfVK2iF6oZziXjYsC3XvZ9BGgwtBnRKdMh

---

## 10-Minute Quickstart (Sui)

### 1) Install

```bash
dart pub add crp_sdk
````

### 2) Send USDT on Sui (local signing)

```dart
final result = await sdk.sendTransfer(
  chain: Chain.sui,
  token: Token.usdt,
  fromPrivateKey: "<SUI_PRIVATE_KEY>",
  to: "<RECIPIENT_SUI_ADDRESS>",
  amount: "1",
  clientIdempotencyKey: DateTime.now().millisecondsSinceEpoch.toString(),
);

print("Tx Hash: ${result.txHash}");
```

### Notes

* Use a unique `clientIdempotencyKey` per request
* Never hardcode private keys in production (use secure storage)

---

## License

MIT

```

**ONE concrete task:** Paste this into `crp-sdk/README.md` and commit it, then reply **“SDK README updated”**.
```
